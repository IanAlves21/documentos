# Documento de Requisitos

Equipe:

  - Luiz Osmar
  - Ian Alves
  - Danilo Frazao
  - Carlos
  - Daniel Chen 

## Introdução

Este documento especifica os requisitos do “sistema para compartilhamento
de soluções de questões para maratonas de programação”, fornecendo aos
projetistas e desenvolvedores as informações necessárias para o projeto e
implementação de programas, assim como para a realização dos testes e
sua homologação.


### Visão geral do documento

Além desta Seção introdutória, as seções seguintes estão organizadas como
descrito abaixo.

  - Seção 2 - Descrição geral do sistema: apresenta uma visão geral do
sistema,
caracterizando qual é o seu escopo e descrevendo seus
usuários.
  - Seção 3 - Requisitos funcionais (casos de uso): especifica brevemente os
casos de uso do sistema.
  - Seção 4 - Requisitos não funcionais: cita e explica os requisitos não funcionais
do sistema.
  - Seção 5 - Arquitetura do sistema: apresenta uma visão geral de alto nível
da
arquitetura prevista no sistema, mostrando a distribuição das funções
nos módulos do sistema.
  - Seção 6 - Especificação de requisitos do sistema: descreve requisitos
funcionais e não funcionais mais detalhadamente. No caso de requisitos
funcionais, descreve os fluxos de eventos, prioridades, atores, entradas e
saídas de cada caso de uso a ser implementado.
  - Seção 7 - Glossário: Apresenta definições de termos técnicos e relevantes.

### Convenções, termos e abreviações

A correta interpretação deste documento exige o conhecimento de algumas
convenções e termos específicos, que são descritos a seguir.

#### Identificação dos requisitos

Por convenção, a referência aos requisitos é feita através do nome da subseção
onde eles estão descritos seguidos do identificador do requisito, de acordo com a
especificação a seguir: [nome da subseção. Identificador do requisito]
Por exemplo, o requisito funcional [Incluir Usuário] deve estar descrito em uma
subseção chamada “Incluir Usuário”, em um bloco identificado pelo seu respectivo
número. Já o requisito não funcional [Confiabilidade] deve estar descrito na seção de
requisitos não funcionais de Confiabilidade, em um bloco identificado por seu número.
Os requisitos devem ser identificados com um identificador único. A numeração inicia
com o identificador [RF001] ou [NF001] e prossegue sendo incrementada à medida
que forem surgindo novos requisitos.

#### Propriedades dos requisitos

Para estabelecer a prioridade dos requisitos, nas seções 4 e 5, foram adotadas as
denominações "essencial", "importante" e "desejável".

  - **Essencial** é o requisito sem o qual o sistema não entra em funcionamento. Requisitos essenciais são requisitos imprescindíveis, que têm que ser implementados impreterivelmente.
  - **Importante** é o requisito sem o qual o sistema entra em funcionamento, mas de forma não satisfatória. Requisitos importantes devem ser implementados, mas, se não forem, o sistema poderá ser implantado e usado mesmo assim.
  - **Desejável** é o requisito que não compromete as funcionalidades básicas do sistema, isto é, o sistema pode funcionar de forma satisfatória sem ele. Requisitos desejáveis podem ser deixados para versões posteriores do sistema, caso não haja tempo hábil para implementá-los na versão que está sendo especificada.


## Descrição geral do sistema

O sistema proposto tem por objetivo ajudar a disseminação dos conteúdos
voltados para maratonas de programação, tais como: compartilhamento de questões
resolvidas, pedido de ajuda em algum problema especifico, compartilhar questões
sobre conteúdo específico. E também possibilitar a criação de um ambiente de troca
de informações de forma saldável entre os competidores das famosas maratonas de
programação.

## Requisitos funcionais (casos de uso)

### [RF001] Cadastrar usuário

Prioridade: **Essencial**

O sistema deve permitir que o usuário efetue o seu próprio cadastro no
sistema a partir de informações como login e senha.


### [RF002] Realizar postagem de conteúdo

Prioridade: **Essencial**

O sistema deve permitir a um usuário efetuar a postagem de conteúdo
sobre algum problema ou solução de questão de maratona.


### [RF003] Realizar comentário

Prioridade: **Essencial**

O sistema deve permitir ao usuário selecionar uma postagem e assim
fazer um comentário sobre tal postagem.


### [RF004] Realizar login

Prioridade: **Essencial**

O sistema deve permitir ao usuário realizar login no sistema


### [RF005] Anexar foto

Prioridade: **Essencial**

sistema deve permitir ao usuário anexar uma foto, provinda da galeria
ou da câmera sobre seu problema em especifico.


### [RF006] realizar logout

Prioridade: **Essencial**

O sistema deve permitir que o usuário efetue o logout da aplicação.


## Requisitos não funcionais

### [NF001] Segurança

O sistema deve fornecer mecanismos de segurança e autenticação alinhados
com os requisitos de proteção mínimos.


### [NF002] Desempenho

O sistema deve ter um tempo de resposta baixo para o envio e recebimento
de atualizações de postagens ais recentes.


### [NF003] Versatilidade

O sistema deve ter compatibilidade entre as versões *web* e *mobile*.


### [NF004] Compatibilidade

A versão *web* deve ser compatível com as últimas versões dos navegadores
mais populares.

A versão *mobile* deve ser compatível com as últimas versões do Android.


## Modelagem do sistema

O sistema será desenvolvido com dois *front-ends* diferentes, sendo eles:

  - Versão *Mobile*
  - Versão *Web*

A partir disso o sistema em sua versão *mobile* terá como arquitetura de
desenvolvimento o ambiente **react-native** que permite a liberação de versão de
produção tanto em **Android** quanto em **iOS** possibilitando assim uma maior
versatilidade. O mesmo terá a subdivisão em 3 telas para manuseio do usuario e
seus módulos terão uma estrutura de FEED, POSTAGEM, PERFIL algo nesse estilo
estrutural.

## Especificação de requisitos do sistema

|         RS001 | Cadastrar usuário                                            |
| ------------: | :----------------------------------------------------------- |
|    Referência | RF001, RF007                                                 |
|       Sumário | O caso de uso é responsável por logar um usuário no sistema  |
| Pré-condições | Ter um login e senha com critérios de segurança mínima como o uso de caracteres especiais e também numeros |
|        Atores | Usuário                                                      |
|     Descrição | 1. O usuário faz login no app<br/>2. O usuário tem acesso ao sistema |

|         RS002 | Fazer publicação                                             |
| ------------: | :----------------------------------------------------------- |
|    Referência | RF002                                                        |
|       Sumário | O caso de uso é responsável por permitir que o usuário logado faça publicação em seu perfil pessoal |
| Pré-condições | Ter um login e senha com critérios de segurança mínima como o uso de caracteres especiais e também números |
|        Atores | Usuário                                                      |
|     Descrição | 1. O usuário faz login no app.<br/>2. O tem acesso a interface do sistema<br/>3. Navega até a aba de postagem<br/>4. Escolhe a foto para publicação<br/>5.Adiciona um comentário inicial<br/>6. Posta a publicação para os outros usuários terem acesso |

|         RS003 | Fazer comentário                                             |
| ------------: | :----------------------------------------------------------- |
|    Referência | RF002                                                        |
|       Sumário | O caso de uso é responsável por permitir que o usuário logado faça publicação de comentário em determinadas postagens em seu perfil pessoal |
| Pré-condições | Ter um login e senha com critérios de segurança mínima como o uso de caracteres especiais e também números |
|        Atores | Usuário                                                      |
|     Descrição | 1. O usuário faz login no app.<br/>2. O tem acesso a interface do sistema<br/>3. Navega até a aba de postagem<br/>4. Seleciona a postagem desejada<br/>5. Abre o ícone de comentário<br/>6. Digita o comentário<br/>7. Posta o comentario |

# Sistema de Gestão de Datasets com CKAN

Este repositório contém a documentação e os arquivos de configuração para a implementação de um portal de dados para o CPPS/UNESP e IPPR/UNESP, utilizando a plataforma [CKAN (Comprehensive Knowledge Archive Network)](https://ckan.org/).

O objetivo principal é substituir a atual planilha de controle de datasets por um sistema centralizado, robusto e que facilite a busca, o compartilhamento e a reutilização de dados de pesquisa.

## 🚀 Instalação e Ambiente de Desenvolvimento

Para executar e desenvolver neste projeto, é necessário ter o Docker e o Docker Compose instalados em sua máquina.

#### ETAPA 01: Clonar o repositório

Utilize o método de sua preferência para clonar o projeto.

```bash
# Via SSH (Recomendado)
git clone git@github.com:colabhd/dataset-management.git
 
# Via HTTPS
git clone https://github.com/colabhd/dataset-management.git
```

## Estrutura geral do CKAN

## ESTRUTURA ORGANIZACIONAL DO CKAN 

### COMO OS DADOS CHEGAM AO CKAN:
Os dados   presentes no CKAN foram depositados pela interface disponibilizada pelo sistema ou por API (Application Programming Interface)

### COMO OS DADOS SÃO ORGANIZADOS PELO CKAN? 
* __Datasets__: As unidades informacionais do CKAN  são chamadas de "Datasets", recursos compostos por metadatos e que possuem relações de dependencia variadas. 
* __Organizações__: Tendo em vista o fato de que o CKAN foi pensado para ser utilizado por várias instituições é natural que os datasets sejam agrupados e atribuidos ao que são chamadas aqui de organizações, que podem ser organizadas de acordo com a preferência do usuário (pode ser usada a criação de grupos temáticos, por exemplo).
* __Grupos__: Os grupos são onde voce pode armezenar os conjuntos de dados (ou dataset) que podem possuir ou não relaçãoe de depêndencia entre si.

## TEMPLATE DO CKAN: 
O template do CKAN é desenhado para facilitar a compreensão das informações e instruções presentes no site, então  elementos como cabeçalho (parte superior da tela), área de trabalho (entre o rodapé e o cabeçalho) e rodapé (parte inferior da tela, onde o usuário pode inserir informações sobre as instituições que mantém o site) possuem linguagem clara e simples. É possivel encontrar também na plataforma a área de noticias ( onde o usuário pode inserir noticias ou descrição do site, torno-o assim mais personalisável), ferramenta de busca (a ferramenta de busca que fica na área de trabalho e aparece apenas na página inicial serve para que o usuário possa "recuperar as bases de dados com base em suas descrições")

 ## CADASTRO E LOGIN NO CKAN
Apesar de fazer parte do uso da ferramenta para depósito de dados, não é necessário que os usuários que estejam apenas realizando buscas possuam um login dentro do CKAN.
## Tipos de usuário dentro do CKAN: 
 * ANÔNIMO:Não possui cadastro e pode apenas visualizar e realizar buscas de conjuntos de dados presentes na plataforma.
* IDENTIFICADO:Pode criar organizações, grupos e conjuntos de dados, desde que esteja vinculado a uma instituição e essas configurações estejam habilitadas.
* ADMNISTRADOR: Tem acesso a funções relacionadas à administração do sistema, pode criar e excluir conteúdos além  de excluir outros usuários e realizar customizações no sistema.

## Como realizar oo registro:
 O link para o registro de usuários fica disponivel na interface do ckan (no cabeçalho), e, para completar o cadastro na plataforma é necessário informar o nome de usuáqrio ( que deve ter apenas letras, números e caracteres),  o nome completo, o endereço de email e uma senha. Nota-se que caso haja algum problema com o login é possivel solicitar a recuperação de senha( link : https://ckan.org/accounts/password/reset/).

# GERENCIAMENTO DE CONTEÚDO NO CKAN
As ferramentas do CKAN podem ser utilizadas para que você realize adição, exclusão e alterações de conjuntos de dados (datasets)

# TUTORIAL: 

## A adição do conjunto de dados: 

A adição dos dados requer a descrição e a carga do arquivo, ao selecionar a opção de adicionar novos conjuntos de dados o usuário deve descreve-los para que assim aja a recuperação e organização, em seguida, carrega os dados presentes no arquivo, criando assim novos conjuntos de dados que ficarão presentes no  CKAN. 
* __Observação:__ Algumas instalações do CKAN requerem a participação de uma organização, através da versão demo (https://demo.ckan.org/) é possível adicionar conjuntos de dados sem fazer parte de uma organização.

### Passo a passo:

* Selecionar a opção "adicionar novos conjuntos de dados" 
* Em seguida, utilizar o formulário fornecido pelo CKAN para descrever seu conjunto de dados : Acrescentar  o __título__ que será único em todo o CKAN, a __descrição__ que pode incluir informações sobre a origem do dado e fatos gerais sobre eles, as __etiquetas__ recurso importante para ajudar os usuários a encontrar os dados, a __licença__ que é necessária para  que as pessoas possam usar os dados coretamente, a __organização__ que poderá deter o direito sobre esses dados, a __visibilidade__, ou seja, a escolha de tornar os dados públicos ou não ( os conjuntos de dados privados só podem ser vistos pelos membros da organização), a __fonte__ dos dados, a __versão__ dos dados ( que pode ser alterada posteriormente), o __autor__ (pessoa ou organização responsável pela produção dos dados), o __email do autor__, nome e email do __mantenedor__ se julgar necessário e os __campos personalizados__ contendo informações relevantes para o criador do conjunto de dados. __Observação:__ O único campo obrigatório do formulário aqwui mencionado é o título, entretanto é recomendado que os outros também sejam preenchidos.Nota-se também que a maioria das informações colocadas aqui podem ser alteradas depois.
*  __Próximo: adicionar dados__
*  Para carregar os arquivos de dados é necessário a  solicitação  de __recursos__ para a solicitação de carregamento de dados, onde O __NOME__, __descrição__ e __formato__ (XLS, JSON, PDF, etc) do arquivo precisam ser exclarecedos, é importante mencionar que o recurso não precisa ser único, isto é, um conjunto de dados (_dataset_) pode ter mais de um recurso. É possivel realizar o upload de arquivos ou links com os dados no ckan.

* __Como alterar um conjunto de dados?__ 

   É possivel alterar qualquer conjunto de dados pertencente à mesma organização,e caso o _dataset_ não pertença a nenhuma organização qualquer usuário cadastrado pode altera-lo. 

   * __Aterando um conjunto de dados__: 

        1. Acesse a página do conjunto de dados desejado
        2. Clique no campo  "gerenciar" que vai aparecer do lado direito do conjunto de dados.
        3. Preencher o formulário de alteração, excluindomou adicionando informações no seu _dataset_
        4. Clicar em “Atualizar conjunto de dados”

    
* __Alterar, escluir e adicionar recursos__:

    Devido ao fato de um único _dataset_ poder ser constituido por varios tipos de dados, é possivel acrescentar mais de um tipo de recurso assim como altera-los e exclui-los.



   *    __Gerenciando seus recursos__: 

        1.  Abrir a página do conjunto de dados 
        2. Entrar no modo de edição do conjunto de dados
        3. Clicar na aba de edição de recursos
        4. Selecionar o recurso desejado (Alterar informações)
        5. Caso o objetivo seja acrescentar um novo recurso é necessário clicar  em “Adicionando um conjunto de dados”
        6. Para alterar informações ou excluir recursos é preciso acessar a página do recurso desejado. 



* __Como excluir um conjunto de dados:__

O CKAN fornece ferramentas para que seja feita a exclusão de conjuntos de dados, entretante, esse proceso é irreversivel e requer muito cuidado. Já na página do conjunto de dados deve-se entrar na edição e então clicar no botão "excluir" em seguida, deve-se confirmar a ação.

* __As organizações:__ 

     As organizações são responsaveis pela maior parte dos conjuntos de dados , onde  seus membros fazem a manutenção e gerenciamento dos _datasets_. As permissões concedidas aos usuários membros são definidas pelo encarregado da organização, e, cada organização possui sua página onde são encontradas informações gerais como histórico de busca e edições, para que as organizações possam obter maior controle sobre seus dados

     * __Criando uma organização:__ 

     1. Clicar no ícone "organizações na parte superior da página
     2. Caso tenha permissão o botão "adicionar uma organização" acima da caixa de pesquisa.
     3. Preencher o formulário de descrição da organização (descrição, url e imagem como elementos opcionais)
     4. Alterar permissões: Depois que a organização foi criada é necessário direcionar os previlégios aos usuários responsáveis.

     * __Administrando sua organização:__
     
     O usuário que cria uma organização torna-se automaticamente seu administrador, e assim, detentor de todos os previlágios dentro dela, esse usuário é o único capaz de gerenciar a organização, ou delegar essa permissão para outra pessoa.

     __Como gerenciar sua organização:__

     1. __Edição:__ É posivel editar as informações fornecidas durante a criação da organização a qualquer momento.(título, descrição, imagem e campos personalizados)
     2. __Conjuntos de dados:__  O administrador pode gerenciar os conjuntos de dados (ou _datasets_) pertencentes à organizaçãp
     3. __Membresia__: É possível também adicionar, remover e atribuir funções aos membros da organização.
     

* __Criação de *grupos*:__      
             
        
  A criação de um grupo é uma maneira de agrupar  conjuntos de dados (_datasets_) de diferentes organizações, em um grupo é possível separar os _datasets_ de acordo com diferentes categorias ( tipo, temática e assunto).É importante mencionar que os grupos, assim como as organizações possuem usuários encarregados de sua administração, a diferença é que os membros dos grupos não possuem permissão para editar os conjuntos de dados, aqueles que fazem parte de um grupo podem apenas acrescentar ou remover _datasets_ do seu grupo, aquele qe for __administrador__ do grupo pode ainda, editar suas informações.

  * __Como gerenciar um grupo?__
  O administrador do grupo é sempre o usuário que o criou, sendo aasim, apenas esse usuário e aqule que tiver sua permissão podem alterar as informações e usufruir dos previlégios de gerenciamento.

* __Como recuperar um conjunto de dados?__

     A recuperação de dados é uma das principais funções do CKAN, afinal, os dados são depositados e organizados em grupos para que os ussuários possam acessá-los.
     
     * __Como fazer a busca:__ 
      
          A busca pe feita por meio de termos, 






































































































































        
#### ETAPA 02: Iniciar os serviços com Docker

Após clonar, acesse a pasta raiz do projeto e execute o comando abaixo para construir e iniciar todos os containers necessários (CKAN, PostgreSQL, Solr, Redis).

```bash
cd dataset-management
docker-compose up -d
```

-   O comando `docker-compose up` irá baixar as imagens e iniciar os serviços.
-   A flag `-d` (detached mode) executa os containers em segundo plano.

Após a conclusão, a instância do CKAN estará disponível em `http://localhost:5000`.

## 🔄 Versionamento

Abaixo estão as instruções para realizar o versionamento de suas contribuições de forma padronizada.

### ETAPA 01: Gravando mudanças

Utilize o seguinte comando para adicionar e registrar todas as modificações feitas nos arquivos:

```bash
git add . && git commit -m 'insira uma mensagem clara e descritiva'
```

**Onde:**

-   `git add .` adiciona todas as mudanças (novos arquivos, modificações) à "área de preparação" (staging area), marcando-as para serem incluídas no próximo commit.
-   `&&` é um operador que encadeia comandos, executando o segundo apenas se o primeiro for bem-sucedido.
-   `git commit -m 'mensagem'` grava permanentemente as mudanças que estão na staging area no histórico do repositório local, associadas à mensagem descritiva que você fornecer.

### ETAPA 02: Sincronizando com o repositório remoto

As mudanças feitas com `git commit` são salvas apenas na sua máquina local. É fundamental sincronizá-las com o repositório central no GitHub.

```bash
git pull origin main && git push origin main
```

**Onde:**

-   `git pull origin main` busca e integra as mudanças mais recentes do branch `main` do repositório remoto (`origin`) ao seu repositório local. **É crucial executar isso antes do `push` para evitar conflitos.**
-   `git push origin main` envia os seus commits locais para o branch `main` do repositório remoto, tornando suas contribuições visíveis para a equipe.

## 🧠 Entendimento da Plataforma (CKAN)

Esta seção documenta o estudo realizado sobre a arquitetura e os conceitos fundamentais do CKAN, que guiam o desenvolvimento deste projeto.

### Arquitetura Geral

A plataforma é modular e organizada em camadas distintas que se comunicam entre si.

```
+--------------------------------+
|     Frontend (Interface Web)   |  <-- Camada de Apresentação (Templates Jinja2)
+--------------------------------+
                | (Comunicação via API)
+--------------------------------+
|      Backend (CKAN Core)       |  <-- Camada de Lógica (Python)
| - API de Ações e Lógica        |
| - Modelo de Domínio e Permissões|
+--------------------------------+
                | (Persistência e Indexação)
+--------------------------------+       +--------------------------------+
|   Banco de Dados (PostgreSQL)  | ----> |   Motor de Busca (Solr)        |
+--------------------------------+       +--------------------------------+
```

### Conceitos Chave

-   **`Dataset`**: A unidade principal de informação. É um contêiner para metadados (título, descrição, fonte, tags) que descreve um conjunto de dados, como "Resultados Eleitorais de 2022".
-   **`Resource`**: Os dados propriamente ditos, vinculados a um `Dataset`. Pode ser um arquivo (CSV, Shapefile) ou um link para uma API. Um `Dataset` pode conter múltiplos `Resources`.
-   **`Organization`**: Agrupa datasets que pertencem a uma mesma entidade (ex: "CPPS", "IPPR"). É a principal forma de controlar permissões de edição.
-   **`Group`**: Usado para criar coleções temáticas de datasets, que podem pertencer a diferentes organizações (ex: "Dados sobre Educação").

### Níveis de Usuário e Permissões

-   **Anônimo:** Usuário não logado. Pode apenas visualizar e buscar datasets públicos.
-   **Identificado (Membro):** Usuário com cadastro. Pode criar, editar e excluir datasets dentro das `Organizations` das quais é membro.
-   **Administrador:** Tem controle total sobre a instância, podendo gerenciar usuários, organizações, extensões e customizações do sistema.

## 📁 Estrutura do Projeto

A estrutura de pastas foi planejada para manter o projeto organizado e escalável.

```
dataset-management/
 ├── ckan/              # Configuração da instância CKAN (ckan.ini, etc.)
 ├── ckanext-cpps/      # Diretório para a extensão customizada do CPPS (futuro)
 ├── scripts/           # Scripts auxiliares (ex: migração, automação)
 │    └── migration/    # Scripts para migrar dados da planilha para o CKAN
 ├── docker-compose.yml # Arquivo de orquestração dos serviços Docker
 └── README.md          # Esta documentação
```

## ✅ Próximos Passos e Issues Futuras

-   **[Fase 2] Configuração do Ambiente:** Validar o `docker-compose.yml` e garantir que toda a equipe consiga executar a instância localmente sem problemas.
-   **[Fase 2] Definição do Esquema de Metadados:** Criar o arquivo de schema para a extensão `ckanext-scheming`, detalhando todos os campos customizados necessários para os datasets do CPPS/IPPR.
-   **[Fase 2] Prova de Conceito (PoC) da Migração:** Desenvolver um script em Python (`scripts/migration/migrate.py`) para ler 10-20 linhas da planilha e inseri-las na instância de desenvolvimento via API do CKAN, para validar o mapeamento de campos.
-   **[Fase 3] Integração com Recoll:** Estudar e planejar a integração para permitir a busca de texto completo dentro do conteúdo dos arquivos (PDFs, DOCs) anexados como recursos.
```

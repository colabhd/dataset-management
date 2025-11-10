
# Sistema de Gestão de Datasets


O sistema tem como objetivo centralizar, documentar e gerenciar todas as bases de dados mantidas, em conjunto, pelo Centro de Pesquisa POlítica e Social (CPPS/UNESP) e pelo Laboratório Multiusuário do Instituto de Políticas Públicas e Relações Internacionais (IPPR/UNESP). 


## Funcionalidades

- Inclusão, atualização, exclusão e descrição padronizada
- Cada conjunto de dados passa a ter metadados completos 
- Pode ser atualizado tanto manualmente pela interface web quanto automaticamente via API.

## Tecnologias Utilizadas

- CKAN

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
## Tipos de usuário dentro do CKAN : 
 * ANÔNIMO:Não possui cadastro e pode apenas visualizar e realizar buscas de conjuntos de dados presentes na plataforma.
* IDENTIFICADO:Pode criar organizações, grupos e conjuntos de dados, desde que esteja vinculado a uma instituição e essas configurações estejam habilitadas.
* ADMNISTRADOR: Tem acesso a funções relacionadas à administração do sistema, pode criar e excluir conteúdos além  de excluir outros usuários e realizar customizações no sistema.

## Como realizar oo registro :
 O link para o registro de usuários fica disponivel na interface do ckan (no cabeçalho), e, para completar o cadastro na plataforma é necessário informar o nome de usuáqrio ( que deve ter apenas letras, números e caracteres),  o nome completo, o endereço de email e uma senha. Nota-se que caso haja algum problema com o login é possivel solicitar a recuperação de senha( link : https://ckan.org/accounts/password/reset/).

# GERENCIAMENTO DE CONTEÚDO NO CKAN
As ferramentas do CKAN podem ser utilizadas para que você realize adição, exclusão e alterações de conjuntos de dados (datasets)

# TUTORIAL : 

## A adição do conjunto de dados : 

A adição dos dados requer a descrição e a carga do arquivo, ao selecionar a opção de adicionar novos conjuntos de dados o usuário deve descreve-los para que assim aja a recuperação e organização, em seguida, carrega os dados presentes no arquivo, criando assim novos conjuntos de dados que ficarão presentes no  CKAN. 
* __Observação:__ Algumas instalações do CKAN requerem a participação de uma organização, através da versão demo (https://demo.ckan.org/) é possível adicionar conjuntos de dados sem fazer parte de uma organização.

### Passo - a - passo : 

* Selecionar a opção "adicionar novos conjuntos de dados" 
* Em seguida, utilizar o formulário fornecido pelo CKAN para descrever seu conjunto de dados : Acrescentar  o __título__ que será único em todo o CKAN, a __descrição__ que pode incluir informações sobre a origem do dado e fatos gerais sobre eles, as __etiquetas__ recurso importante para ajudar os usuários a encontrar os dados, a __licença__ que é necessária para  que as pessoas possam usar os dados coretamente, a __organização__ que poderá deter o direito sobre esses dados, a __visibilidade__, ou seja, a escolha de tornar os dados públicos ou não ( os conjuntos de dados privados só podem ser vistos pelos membros da organização), a __fonte__ dos dados, a __versão__ dos dados ( que pode ser alterada posteriormente), o __autor__ (pessoa ou organização responsável pela produção dos dados), o __email do autor__, nome e email do __mantenedor__ se julgar necessário e os __campos personalizados__ contendo informações relevantes para o criador do conjunto de dados. __Observação:__ O único campo obrigatório do formulário aqwui mencionado é o título, entretanto é recomendado que os outros também sejam preenchidos.Nota-se também que a maioria das informações colocadas aqui podem ser alteradas depois.
*  __Próximo : adicionar dados__
*  Para carregar os arquivos de dados é necessário a  solicitação  de __recursos__ para a solicitação de carregamento de dados, onde O __NOME__, __descrição__ e __formato__ do arquivo precisam ser exclarecedos, é importante mencionar que o recurso não precisa ser único, isto é, um conjunto de dados (_dataset_) pode ter mais de um recurso.











        

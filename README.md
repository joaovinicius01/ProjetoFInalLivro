## Aplicativo de Livraria
Descrição
Este é um aplicativo de livraria desenvolvido com Kotlin, utilizando Jetpack Compose e Firebase. O objetivo principal do app é permitir aos usuários visualizar, adicionar, editar e excluir livros de uma biblioteca virtual, além de organizar a exibição de livros por diferentes categorias, como nome e ano de publicação. O app oferece uma interface intuitiva e moderna para facilitar a interação do usuário.
Funcionalidades Principais
Tela de Login
Permite que os usuários façam login para acessar o catálogo de livros e realizar ações de gerenciamento.
Tela de Menu
A tela de menu oferece opções para navegar entre as principais funcionalidades do aplicativo:
Catálogo de Livros: Exibe uma lista de livros cadastrados.
Configurações: Permite o gerenciamento de configurações do app.
Ajuda: Oferece informações de suporte ao usuário.
Catálogo de Livros
Exibe uma lista de livros cadastrados.
Cada livro é exibido com seu nome e ano de publicação.
Ícones de edição ao lado de cada livro permitem que o usuário edite ou exclua livros.
O catálogo pode ser atualizado para exibir livros em ordem crescente de ano de publicação.
Adicionar e Editar Livros
O usuário pode adicionar um novo livro informando o nome e ano de publicação.
Caso o livro já exista, ele pode ser editado, permitindo alterar o nome e ano de publicação.
Exclusão de Livros
O aplicativo permite excluir livros da lista de forma simples através de um ícone de lixeira ao lado de cada livro.


## Decisões de Design

Interface do Usuário
Jetpack Compose foi utilizado para criar a interface, proporcionando um design moderno e fluido.
A navegação entre as telas é realizada usando o NavController do Jetpack Compose, garantindo uma transição suave entre as telas.
A BottomAppBar foi adotada para exibir botões de navegação, proporcionando fácil acesso às principais funcionalidades.
O uso de OutlinedTextField e Button foi escolhido para garantir uma interface limpa e intuitiva na adição e edição de livros.
## Estrutura de Dados

Cada livro é representado por uma classe de dados (Livro), que contém informações como nome, ano e id (utilizado como identificador único no Firebase).
A persistência de dados é realizada usando o Firestore do Firebase, que armazena e gerencia as informações dos livros. O repositório (LivroRepository) abstrai as operações de CRUD (Criar, Ler, Atualizar e Deletar) para os livros.
Gerenciamento de Estado
O estado dos livros é gerido usando o Jetpack Compose remember e mutableStateOf, permitindo que o aplicativo reaja de forma reativa às alterações, como a adição de novos livros.
LaunchedEffect e coroutines são usados para gerenciar chamadas assíncronas para o Firestore sem bloquear a interface do usuário.
Firestore e Persistência de Dados
O Firebase Firestore foi escolhido como banco de dados para persistir as informações dos livros. Ele foi integrado de forma eficiente para armazenar e recuperar livros sem a necessidade de configuração de um banco de dados local.
A sincronização dos livros com o Firestore é realizada de forma assíncrona, garantindo que a interface do usuário continue fluida mesmo com operações de rede.
Decisões de Arquitetura
A arquitetura do aplicativo segue o padrão MVVM (Model-View-ViewModel), separando a lógica de negócios da interface de usuário. Isso garante uma estrutura limpa e fácil de manter.
Repository Pattern foi adotado para acessar o Firestore e gerenciar os dados dos livros de forma centralizada e desacoplada da camada de UI.
## Tecnologias Utilizadas

Kotlin: Linguagem principal para o desenvolvimento.
Jetpack Compose: Framework de UI para criar interfaces declarativas e reativas.
Firebase Firestore: Banco de dados em tempo real para persistir os dados dos livros.
Coroutines: Gerenciamento assíncrono de tarefas para evitar bloqueio da UI.
Material3: Componentes de UI baseados no design do Material para garantir uma interface moderna e acessível.


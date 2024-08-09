<h1 align="center"> Sistema de Cadastro de Usuario </h1>

 ## Descrição:
O projeto é uma aplicação web simples que valida os campos preenchidos de entrada de um formulário de cadastro. Ele garante que o usuário preencha todos os campos obrigatórios e consiga salvar seu nome e poder editar caso tenha escrevido errado ou excluir caso não queira ter o nome na lista.

### VALIDAÇÃO DE PREECHIMENTO

<img src="Li.png" alt="Texto Alternativo">

### let loginEmail = document.getElementById('loginEmail').value;

Obtém o valor do campo de entrada (input) com o id loginEmail e o armazena na variável loginEmail.

### let loginSenha = document.getElementById('loginSenha').value;

Obtém o valor do campo de entrada (input) com o id loginSenha e o armazena na variável loginSenha.

### if(!loginEmail || !loginSenha)

Verifica se qualquer um dos valores (loginEmail ou loginSenha) está vazio ou undefined. Se um dos valores for falso (ou seja, vazio), a condição é verdadeira.

### alert("Por favor preencher todos os campos");

Se a condição do if for verdadeira (ou seja, algum campo estiver vazio), exibe um alerta com a mensagem "Por favor preencher todos os campos".

### window.location.href = 'cadastro.html';

Se ambos os campos estiverem preenchidos, o navegador será redirecionado para a página cadastro.html.

### Função criador de Arrey para armazenamento de nomes

<img src="ar.png">

### var dadosLista = [];

Inicia como um array vazio. Este array será usado para armazenar os nomes inseridos pelo usuário.
 
 ### function salvarUser ()

A função salvarUser, que será chamada quando o usuário deseja salvar um nome.

### let nomeUser = document.getElementById('nomeUser').value;

Dentro da função, declara uma variável nomeUser e a inicializa com o valor do campo de entrada com o id nomeUser. A função document.getElementById('nomeUser').value recupera o valor digitado pelo usuário no campo de entrada.

### if(nomeUser)

Verifica se a variável nomeUser não está vazia (ou seja, se o usuário digitou algum texto). O código dentro do if será executado se essa condição for verdadeira.
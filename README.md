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

###  dadosLista.push(nomeUser);

Adiciona o valor de nomeUser ao array dadosLista usando o método push(), que adiciona um item ao final do array.

###  console.log(dadosLista);

Exibe o conteúdo atual do array dadosLista no console. Isso é útil para depuração, para verificar se o nome foi corretamente adicionado ao array.

###  criaLista();

Chama a função criaLista() para atualizar a exibição da lista de nomes na página. Essa função irá criar e mostrar uma lista HTML com os nomes armazenados no array.

### document.getElementById('nomeUser').value = "";

 Limpa o campo de entrada nomeUser após o nome ser salvo, definindo seu valor como uma string vazia.

 ### else alert("Favor, informar um nome para cadastro");

Se o campo de entrada estiver vazio (ou seja, a condição do if não for verdadeira), exibe uma mensagem de alerta pedindo para o usuário informar um nome para cadastro.

## Função decriação de Lista

<img src="a.png">

### let tabela = document.getElementById("tabela").innerHTML = "<tr><th>Nome Usuário</th><th>Ações</th></tr>";

 Esse código obtém o elemento HTML com o id tabela e define seu innerHTML inicial com um cabeçalho de tabela (<tr><th>Nome Usuário</th><th>Ações</th></tr>). Esse cabeçalho define as colunas da tabela: uma para o nome do usuário e outra para ações (editar e excluir). O valor de innerHTML é armazenado na variável tabela.

 ### for(let i = 0; i <= (dadosLista.length - 1); i++)

 Inicia um loop for que itera sobre cada índice do array dadosLista. A condição i <= (dadosLista.length - 1) garante que o loop percorra todos os elementos do array.

 ### tabela += "<tr><td>" + dadosLista[i] +"</td><td><button // type='button' onclick='editar(parentNode.parentNode.rowIndex)'>Editar</button><button // type='button' onclick='excluir(parentNode.parentNode.rowIndex)'>Excluir</button></td></tr>";

 Adiciona uma nova linha (<tr>) à variável tabela para cada nome no array dadosLista. Cada linha da tabela contém:
* Uma célula (<td>) com o nome atual do array (dadosLista[i]).
* Uma célula com dois botões:
* Editar: Um botão que chama a função editar passando o índice da linha (parentNode.parentNode.rowIndex), que representa a linha onde o botão foi clicado.
* Excluir: Um botão que chama a função excluir também passando o índice da linha (parentNode.parentNode.rowIndex).

### document.getElementById("tabela"). innerHTML = tabela;

Define o innerHTML do elemento com o id tabela para o valor da variável tabela. Isso atualiza a tabela na página com todas as linhas (nomes e botões) que foram adicionadas no loop.

## Função para excluir Nome de lista 

<img src="ka.png">

### function excluir(i)

Define a função excluir, que aceita um argumento i. Esse argumento representa o índice da linha da tabela que deve ser excluída. A função é chamada quando o usuário clica no botão "Excluir" correspondente a uma linha na tabela.

### dadosLista.splice((i - 1), 1);

 Usa o método splice do array dadosLista para remover um item do array. O método splice modifica o array original. Aqui está o que os parâmetros fazem:
* (i - 1): Especifica o índice no array onde a remoção deve começar. Como i é o índice da linha da tabela e o array dadosLista pode ser indexado a partir de zero, você precisa subtrair 1 para obter o índice correto no array.
* 1: O número de itens a serem removidos a partir do índice especificado. Neste caso, está removendo apenas um item.

### document.getElementById('tabela').deleteRow(i);

Usa o método deleteRow do objeto HTMLTableElement para remover a linha da tabela na página. O método deleteRow remove uma linha da tabela HTML com base no índice especificado. No caso, i é o índice da linha a ser removida.

## Função para editar Nome da Lista

<img src="ren.png">

### function editar(i)

Define a função editar que recebe um argumento i, que representa o índice da linha da tabela a ser editada.

### document.getElementById("nomeUser").value = dadosLista[(i - 1)]

Define o valor do campo de entrada com o id nomeUser para o valor do nome correspondente ao índice i - 1 no array dadosLista. Isso preenche o campo de entrada com o nome que pode ser editado pelo usuário. O índice i - 1 é usado para ajustar a diferença entre os índices da tabela (começando do 1) e do array (começando do 0).

### dadosLista.splice(dadosLista[(i - 1)], 1);

Remove o nome do array para que ele não apareça mais na tabela

### Splice

O método splice em JavaScript é uma função poderosa e versátil usada para modificar arrays. Ele pode adicionar, remover e substituir elementos dentro de um array. 

# Resultado:

<img src="amor.png">

# Alterações Email e CPF

<img src="u.png">

## Primeira alteração do Email

<img src="anjo.png">

### function validarEmail(email)

A função validarEmail é projetada para verificar se o valor passado para o parâmetro email atende a um padrão específico (neste caso, o padrão de um e-mail válido).

### const regex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

* ^[a-zA-Z0-9._%+-]+: Indica o início da string e define o padrão para a parte local do e-mail. Permite letras (maiúsculas e minúsculas), números, e alguns caracteres especiais (., _, %, +, -).
* @[a-zA-Z0-9.-]+: Depois do caractere @, deve haver um ou mais caracteres alfanuméricos, pontos ou hífens, que compõem a parte do domínio.
* \.[a-zA-Z]{2,}$: Um ponto literal seguido por duas ou mais letras (o domínio de nível superior), e garante que a correspondência ocorra até o final da string ($).

### return regex.test(email);

Retorna o resultado da aplicação da expressão regular ao parâmetro email

# Primeira alteração do CPF

<img src="mu.png">

### function validarCPF(cpf)

A função validarCPF é projetada para verificar se o valor passado para o parâmetro cpf está no formato correto de um CPF.

### const regex = /^\d{3}\.\d{3}\.\d{3}-\d{2}$/;

* '^': Indica o início da string.
* '\d{3}': Três dígitos numéricos. A sequência \d representa um dígito (0-9) e {3} especifica que deve haver exatamente três desses dígitos.
* '\.': Um ponto literal. O caractere \ é usado para escapar o ponto, que é um caractere especial em expressões regulares.
* '\d{3}': Outro grupo de três dígitos numéricos.
* '\.': Outro ponto literal.
* '\d{3}': Outro grupo de três dígitos numéricos.
* '-': Um hífen literal.
* '\d{2}': Dois dígitos numéricos.
* '$': Indica o final da string.

### return regex.test(cpf);

 Usa o método test da expressão regular para verificar se o valor de cpf corresponde ao padrão definido pela regex. Retorna true se a correspondência for encontrada e false se não for.

 # Segunda alteração do Email e CPF:

 <img src="si.png">

 ### function limparFormulario()

 A função limparFormulario será usada para limpar (ou redefinir) os valores dos campos de um formulário HTML

 ### document.getElementById('nomeUser').value = ""; document.getElementById('emailUser').value = ""; document.getElementById('cpfUser').value = "";
 
 seleciona o elemento do DOM com o ID nomeUser, emailUser e cpfUser. Normalmente, isso seria um campo de entrada (input) de um formulário.

 # Terceira alteração do Email e CPF:

 <img src="ca.png">

### if (nomeUser && emailUser && cpfUser)

Define uma função chamada adicionarUsuario que aceita três parâmetros: nomeUser, emailUser, e cpfUser. Estes parâmetros representam as informações do usuário a serem adicionadas.

### validarEmail(emailUser) && validarCPF(cpfUser)

Se todos os parâmetros estiverem preenchidos, esta linha chama as funções validarEmail e validarCPF para verificar se o email e o CPF fornecidos são válidos.

### dadosLista.push({ nome: nomeUser, email: emailUser, cpf: cpfUser });

Adiciona um novo objeto contendo nome, email, e cpf à lista dadosLista. Esta lista deve ser uma variável global ou definida em algum lugar fora desta função.

### limparFormulario()

Chama a função limparFormulario para limpar os campos do formulário após o usuário ser adicionado à lista.

### else  alert("Favor, informar um email e um CPF válidos.");

Se a validação do email ou do CPF falhar, exibe um alerta pedindo para informar um email e um CPF válidos.

### else alert("Favor, informar nome, email e CPF para cadastro.");

Se qualquer um dos parâmetros (nomeUser, emailUser, cpfUser) estiver ausente, exibe um alerta pedindo para informar todos os dados necessários para o cadastro.

<img src="nha.png">

Nessa parte só adiconei a código de Email e CPF que acaba fazendo a mesma coisa que ja expliquei a cima com o nome de usuaria que vai ajudar a editar.

# Resultado final:

<img src="resultado.png">

-[Liara Silva](https://github.com/LiaraSilva?tab=repositories)
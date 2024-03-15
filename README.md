# Modelo_CSS_JS_Sistema
Modelo pra criação de site e sistemas, com tamanhos padrões de campos e divs

Abaixo principais comandos para utilizar o Git

*** INSTALANDO O GIT ***
Faça o download do git em git-scm.com/download
Reinicie o VS Code

*** VINCULAR USUÁRIO ***
Faça login no VsCode vinculando o usuário do GitHub.
No terminal digite:
git config --global user.name "Seu usuário do Git"
git config --global user.email "Seu e-mail da conta do GitHub"
Para confirmar, clique em Accounts (lado esquerdo inferior do VsCode), se estiver seu usuário e ao lado GitHub então está correto.

*** ABRINDO REPOSITÓRIO OU CRIANDO UM NOVO ***
OPEN FOLDER: Abrir uma pasta do computador pra se tornar um novo repositório, é necessário exportá-lo pra nuvem do GitHub.
Obs: Caso já tenha um respositório aberto no VsCode, clique em "abrir nova janela" ou feche o repositório atual.
Crie a pasta no computador ou servidor a ser sincronizado com a nuvem.
Clique no botão OPEN FOLDER e selecione a pasta.
Após criar os códigos, clicar em Source Control (Ctrl+Shift+G).
Fazer o Commit (Inserir uma obs).
Clicar em criar repositório.
Abrirá uma tela de login caso ainda não tenha realizado.
Abrirá uma caixa onde você deve escolher se o repositório criado será público ou privado.

CLONE REPOSITORY: Clonar um repositório na máquina pra trabalhar em sincronia, o respositório já deve existir no GitHub.
Acessar o repositório nuvem e copiar o link do mesmo.
Informar no campo que aparece logo após clicar no botão de Clonar.

*** COMANDOS BÁSICOS ***
git pull : puxa os dados do servidor pra máquina, importante fazer isso sempre que estiver trabalhando na brench com mais de um usuário.

git init : Cria um arquivo do git dentro do workspace atual, referenciando o mesmo pra ser futuramente vinculado a um repositório.

git add nome.extenção : Cria um documento com o nome e extenção no workspace, caso o documento já exista, ele insere na fila pra criação de uma nova versão (commit).

git add . : Adiciona todos os arquivos pendentes na fila de sincronização e controle de versão.

git status : Verifica se todos os arquivos dentro do repositório/workspace estão sincronizados.

git commit -m "" : Commit é a versão do código, este comando cria uma nova versão do código e insere a descrição da alteração. O -m é pra inserir a mensagem ou observação.

git push -u origin main : Envia os arquivos em commit pra nuvem do Git, redirecionando pra branch selecionada, sendo neste exemplo a main.

git reflog : log dos arquivos e suas versões.

git stash : Deleta todas as alterações efetuadas após o último pull.

*** VOLTANDO A VERSÃO DE UM ARQUIVO ***
git reset --hard id_do_documento : Informar o documento e sua versão onde deve ser feito o resgate.

*** GESTÃO DE BRANCH ***
git branch : Mostra as branch disponíveis

git branch nome_da_branch : Cria uma nova branch.

git checkout nome_da_branch : Muda pra branch informada.

*** PASSANDO DADOS DE UMA BRENCH PRA OUTRA (MERGE) ***
Primeiro acesse a brench onde você quer que os dados sejam migrados (destino)

git merge nome_da_brench : Une as informações das duas brench, informando o nome da brench de onde quer puxar os dados.

git checkout -b nome_da_nova_branch nome_da_brench_referencia : Cria uma nova brench com base em outra.

touch .gitignore : Cria o arquivo ignore, sendo que os arquivos descritos dentro dele não são enviados pra nuvem.


*** ## COMANDOS JS ***
Concatenar / Interpolação ``
Em um string com cálculo, separa o cálculo e insere no meio da string
${}
Ex: Sem Interpolação com aspas símples
    'Itens (' + (1+1) + '): R$' + (2095 + 799) /100
    Resultado: Itens (2): R$28,94

    Com Interpolação com ``
    `Itens (${1+1}): R$${(2095+799)/100}`
    Resultado: Itens (2): R$28,94

    \n: Pula uma linha
    \': Insere o ' dentro do texto, ao invés de fechar um range de string
    \": Insere o " dentro do texto, ao invés de fechar um range de string

Comandos Térnários
    if (true) {
        console.log('verdadeiro');
    }else {
        console.log('falso');
        };
        OU 
    true ? 'verdadeiro' : 'falso';

    Guard Operator
    Atalho pra &&, caso já encontre falso na primeira opção, já retorna falso.
    
    let message;
    if (message = true) {
        message = 'ola';
    }

    OU

    const message = true && 'olá';

    Atalho pra ||, caso já encontre verdadeiro na primeira opção, já retorna verdadeiro.
    let message;
    if (message = true) {
        message = 'ola';
    }

    OU

    const message = true || 'olá';
    L.

*** ### JSON Objeto ### ***
    JSON = Possui menos funcionalidades que o JS mas se usa pra banco de dados, devido a capacidade de envio de dados pra outros computadores.

    JSON.stringify(nomeObjeto);
    Converte o Ojbeto pra JSON.
    Ex:
        const objetoJs {
            cor: 'vermelho',
            tamanho: 20,
            peso: 0.2
    }

        const objetoJSON {
            "cor": "vermelho",
            "tamanho": 20,
            "peso": 0.2
        }

    Converter JSON pra JS
    JSON.parse(nomeObjeto);

*** LOCAL STORAGE Objeto***
Guardar um valor mesmo que a tela feche ou alguém a recarregue, por exemplo um carrinho de compras.
Obs: Ela somente suporta String

localStorage.setItem('crieUmNome','sua mensagem'); // Salva algo de da variável que criou o nome, dentro do local storage
localStorage.getItem(); // Recupera algo dentro do local storage

*** DOM ***
Dom tras o HTML pra dentro do JS, permitindo alterar e consultar todos os objetos e elementos da página.

document. Acessa o DOM ou documento HTML
document.body Acessa o elemento body da página, trazendo seu conteúdo
document.body.innerHTML - Traz o conteúdo dentro do elemento.

<button class="classe1" id="id1"></button>
document.querySelector() - Permite selecionar qualquer elemento da página.
document.querySelector('button') - Traz o html do primeiro botão da página.
document.querySelector('button').InnerHTML - Traz o conteúdo dentro das tags <button>, ou seja o nome do botão.
document.querySelector('button').InnerHTML = 'Novo Nome' - Altera o conteúdo dentro das tags <button>, ou seja o nome do botão.
document.querySelector('.classe1') - Traz o conteúdo HTML do objeto que tem a classe = classe1
document.querySelector('button').InnerText = Traz o conteúdo dentro das tags <button>, somente texto, ignorando espaços.
# Jogo-do-Numero-Secreto

Segue toda a explicação do código para que seja estudado posteriormente 

Declaração de Variáveis Globais:


let listaDeNumerosSorteados = [];
let numeroLimite = 10;
let numeroSecreto = gerarNumeroAleatorio();
let tentativas = 1;

Aqui estamos declarando quatro variáveis globais:

listaDeNumerosSorteados: Uma lista vazia para armazenar números sorteados.

numeroLimite: Define o limite máximo para o número secreto (10 neste caso).

numeroSecreto: Armazenará o número secreto gerado aleatoriamente, utilizando a função gerarNumeroAleatorio().

tentativas: Inicializado com 1, será usado para contar o número de tentativas do jogador.


Definição de Funções:

function exibirTextoNaTela(tag, texto) {
    let campo = document.querySelector(tag);
    campo.innerHTML = texto;
    responsiveVoice.speak(texto, 'Brazilian Portuguese Female' , {rate:1.2} );
}

Esta função exibirTextoNaTela recebe uma tag HTML e um texto como parâmetros.
Seleciona o elemento HTML usando a tag fornecida e atualiza seu conteúdo com o texto recebido.
Também utiliza a biblioteca responsiveVoice para sintetizar o texto em voz.

Outras Funções:

function exibirMensagemInicial() {
    exibirTextoNaTela('h1' , 'Jogo do numero secreto');
    exibirTextoNaTela('p' , 'Escolha um número entre 1 e 10');
}

A função exibirMensagemInicial é usada para exibir as mensagens iniciais na tela quando o jogo é iniciado.
Chamada de Função Inicial:

exibirMensagemInicial();
Chama a função exibirMensagemInicial para exibir as mensagens iniciais assim que o jogo é carregado.


Função verificarChute():

function verificarChute() {
    let chute = document.querySelector('input').value;
    // Verificar se o chute do jogador está correto ou não
    if (chute == numeroSecreto) {
        // Se o chute estiver correto, exibir mensagem de vitória
    } else {
        // Se o chute estiver incorreto, exibir mensagem indicando se é maior ou menor
        // Incrementar o contador de tentativas e limpar o campo de entrada
    }
}
Esta função é chamada quando o jogador clica no botão "Chutar".
Obtém o valor inserido pelo jogador no campo de entrada e verifica se é igual ao número secreto.
Dependendo do resultado, exibe uma mensagem de vitória ou dica sobre o número secreto.

Função gerarNumeroAleatorio():


function gerarNumeroAleatorio() {
    // Lógica para gerar um número aleatório dentro do intervalo definido
}
Esta função é responsável por gerar um número aleatório dentro do intervalo de 1 a numeroLimite e garantir que seja único em relação aos números sorteados anteriormente.


Outras Funções Auxiliares:

function limparCampo() {
    // Lógica para limpar o campo de entrada
}

function reiniciarJogo() {
    // Lógica para reiniciar o jogo, incluindo gerar um novo número secreto, limpar o campo de entrada e resetar o contador de tentativas
}
Estas funções são responsáveis por limpar o campo de entrada e reiniciar o jogo, respectivamente.

link vercel
https://jogo-pi-ochre.vercel.app/

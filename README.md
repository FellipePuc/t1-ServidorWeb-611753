# Trabalho 1 - Servidor Web (Mini Visual Novel)

## Sobre o Projeto
Atividade prática desenvolvida para avaliar o entendimento e a configuração de consumo de conteúdos estáticos em um servidor web. O projeto consiste em uma aplicação "Data-Driven" (orientada a dados) construída na engine Godot, onde os assets da história não são compilados com o jogo, mas sim baixados em tempo real da internet.

## Desenvolvedor
* **Nome:** Fellipe Teixeira Leite
* **Matrícula:** 611753
* **Curso:** Jogos Digitais

## Como Funciona
A aplicação utiliza o nó `HTTPRequest` da Godot para buscar arquivos de texto (`.txt`) e imagem (`.png`) diretamente deste repositório no GitHub, utilizando o formato `raw`. 

Através da interface do jogo:
1. O usuário insere a **URL Base** deste repositório no campo de texto.
2. Ao clicar em "Próximo", o jogo concatena a URL com o número da cena atual (ex: `1.png` e `1.txt`).
3. O download é feito de forma assíncrona e a interface é atualizada com a nova parte da história.
4. Para alterar a narrativa, basta modificar os arquivos neste servidor, sem nenhuma necessidade de recompilar o executável do jogo.

## Tecnologias Utilizadas
* **Engine:** Godot 4.x
* **Linguagem:** GDScript
* **Servidor/Hospedagem:** GitHub (formato raw)

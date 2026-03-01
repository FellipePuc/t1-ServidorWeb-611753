# Trabalho 1 - Servidor Web (Mini Visual Novel)

## Sobre o Projeto
Atividade prática desenvolvida para avaliar o entendimento e a configuração de consumo de conteúdos estáticos em um servidor web. O projeto consiste em uma aplicação "Data-Driven" (orientada a dados) construída na engine **Unity**, onde os assets da história não são compilados com o jogo, mas sim baixados em tempo real da internet.

## Desenvolvedor
* **Nome:** Fellipe Teixeira Leite
* **Matrícula:** 611753
* **Curso:** Jogos Digitais

## Como Funciona
A aplicação utiliza a biblioteca `UnityEngine.Networking` para buscar arquivos de texto (`.txt`) e imagem (`.jpg`) diretamente deste repositório no GitHub, utilizando o formato `raw`. 

Através da interface do jogo:
1. O usuário visualiza a **URL Base** deste repositório vinculada ao script.
2. Ao clicar em "Próximo", o jogo utiliza Corrotinas (`IEnumerator`) para baixar a nova cena.
3. O download é feito de forma assíncrona através do `UnityWebRequest` e a interface (Canvas) é atualizada com a nova parte da história.
4. Para alterar a narrativa, basta modificar os arquivos neste servidor (GitHub), sem necessidade de recompilar o executável do jogo.

## Tecnologias Utilizadas
* **Engine:** Unity 6 (6000.3.10f1 LTS)
* **Linguagem:** C#
* **Servidor/Hospedagem:** GitHub (formato raw)

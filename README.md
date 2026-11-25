# Mario Jump

Jogo simples no navegador: o Mario corre e você aperta qualquer tecla para pular os canos. Se encostar em um cano, é fim de jogo.

**Online:** https://ygos-96.github.io/jogo-do-mario/

Feito em um workshop de tecnologia, para praticar animações em CSS e lógica de jogo com JavaScript.

## Como jogar

Pressione qualquer tecla para pular. Desvie dos canos que vêm da direita.

## Como funciona

- **Animações em CSS:** o cano e as nuvens se movem com `@keyframes` em loop infinito, e o pulo é uma animação de 500 ms ligada por uma classe (`jump`).
- **Detecção de colisão em JavaScript:** a cada 10 ms um `setInterval` lê a posição do cano (`offsetLeft`) e a altura do Mario (`getComputedStyle`). Se o cano está na faixa do personagem e o Mario está baixo, há colisão.
- **Fim de jogo:** na colisão, as animações são congeladas na posição atual, a imagem troca para a de "game over" e o loop é encerrado.

## Como está organizado

```
index.html
src/css/style.css   cenário, animações do cano, das nuvens e do pulo
src/js/script.js    pulo e detecção de colisão
src/imagem/         sprites
```

## Tecnologias

HTML5, CSS3 e JavaScript puro, sem bibliotecas.

## Rodar localmente

Abra o `index.html` no navegador.

## Limitações conhecidas

- Não há pontuação nem botão de reiniciar: para jogar de novo, recarregue a página.
- O jogo não tem controle por toque, só por teclado.

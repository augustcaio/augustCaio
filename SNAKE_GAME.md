# 🐍 Jogo da Cobra das Contribuições GitHub

Este repositório inclui uma animação do jogo da cobra baseada no gráfico de contribuições do GitHub, gerada automaticamente usando a action [Platane/snk](https://github.com/marketplace/actions/generate-snake-game-from-github-contribution-grid).

## Como funciona

A cobra "come" os quadrados de contribuição do GitHub em ordem cronológica, criando uma animação divertida que mostra o histórico de contribuições de forma lúdica.

## Configuração

O workflow está configurado para:

- **Execução automática**: Todos os dias às 00:00 UTC
- **Execução manual**: Pode ser executado manualmente através do GitHub Actions
- **Múltiplos formatos**: Gera SVG (claro e escuro) e GIF
- **Cores personalizadas**: Cobra laranja com gradiente azul para os pontos

## Arquivos gerados

- `dist/github-snake.svg` - Versão clara (modo light)
- `dist/github-snake-dark.svg` - Versão escura (modo dark)
- `dist/github-snake.gif` - Animação GIF colorida

## Suporte a modo escuro

O README principal usa a tag `<picture>` para mostrar automaticamente a versão correta baseada na preferência do usuário:

```html
<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="dist/github-snake-dark.svg"
  />
  <source
    media="(prefers-color-scheme: light)"
    srcset="dist/github-snake.svg"
  />
  <img alt="github-snake" src="dist/github-snake.svg" />
</picture>
```

## Personalização

Para personalizar as cores ou configurações, edite o arquivo `.github/workflows/snake.yml` e modifique os parâmetros:

- `color_snake`: Cor da cobra
- `color_dots`: Cores dos pontos de contribuição (5 cores separadas por vírgula)
- `palette`: Paleta de cores predefinida (github, github-dark, github-light)

## Créditos

- Action criada por [Platane](https://github.com/Platane)
- Disponível no [GitHub Marketplace](https://github.com/marketplace/actions/generate-snake-game-from-github-contribution-grid)

# 8 Ball Pool → HTML (Browser)

Projeto que converte o jogo **8 Ball Pool v55.2.3** (APK da Miniclip) para execução no navegador via HTML + WebAssembly.

## Como funciona o projeto

1. O APK original (`8-ball-pool-v55.2.3-apkvision.apk`) contém o engine de jogo em C++ nativo (bibliotecas `libgame-*.so`).
2. A Miniclip disponibilou uma versão web do jogo que usa **WebAssembly** (`wasm_guest_1.0.0_73372`) + HTML5 Canvas + RequireJS.
3. O arquivo `8-ball-pool.html` carrega essa versão web no navegador e inicializa o game.

## Como rodar

- Abrir o `8-ball-pool.html` no navegador via servidor local:
  ```bash
  python3 -m http.server 8000
  ```
  e acessar `http://localhost:8000/8-ball-pool.html`
- Ou acessar diretamente a versão oficial: `https://prod-web-pool.miniclip.com/mc`

## Arquivos

- `8-ball-pool.html` — HTML que roda o jogo 8 Ball Pool no browser
- `8-ball-pool-v55.2.3-apkvision.apk` — APK original (não versionado por limite do Git/GitHub)

## Observações

- O jogo requer conexão com internet (CDN + game servers).
- A conversão foi feita a partir da versão web oficial da Miniclip, que é a base do engine do APK.

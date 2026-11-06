# 8 Ball Pool → HTML (Browser)

Projeto que converte jogos de APK para execução no navegador via HTML + WebAssembly.

## Jogos convertidos

1. **8 Ball Pool v55.2.3** (Miniclip) — engine portada para WebAssembly (`wasm_guest_1.0.0_73372`) pela própria Miniclip; roda via RequireJS + WebAssembly no canvas.

2. **GTA San Andreas (Definitive)** — roda no browser via WebAssembly (PCSX2 / TabStation / revcDOS) no site [pixr.dev/gta/gtasa](https://pixr.dev/gta/gtasa/).

3. **People Playground** (PPGA) — engine Unity compilada para **WebAssembly** (`PPG.wasm` via Unity WebGL) rodando no browser; player em [khaxles.neocities.org/games/ppg](https://khaxles.neocities.org/games/ppg) com base em `https://cdn.jsdelivr.net/gh/genizy/web-port@main/people-playground/`.

## Como funciona

- O APK original (`8-ball-pool-v55.2.3-apkvision.apk`) contém o engine de jogo em C++ nativo (bibliotecas `libgame-*.so`).
- Para o 8 Ball Pool: a Miniclip disponibilou uma versão web que usa WebAssembly (`wasm_guest_1.0.0_73372`) + HTML5 Canvas + RequireJS.
- Para o GTA San Andreas: há portas de engine para WebAssembly que rodam o jogo no navegador.
- Para o People Playground: Unity WebGL (WASM) — `PPG.wasm`.

## Como rodar

- **8 Ball Pool:** abrir o `8-ball-pool.html` no navegador (via servidor local: `python3 -m http.server 8000` → `http://localhost:8000/8-ball-pool.html`) ou acessar `https://prod-web-pool.miniclip.com/mc`.
- **GTA San Andreas:** abrir o `gta_san_andreas.html` (iframe aponta para `https://pixr.dev/gta/gtasa/`).
- **People Playground:** abrir o `people_playground.html` (player Unity WebGL que carrega `PPG.wasm` + `PPG.data`).

## Arquivos

- `8-ball-pool.html` — HTML que roda o jogo 8 Ball Pool no browser
- `gta_san_andreas.html` — HTML que roda o jogo GTA San Andreas no browser (via WebAssembly / PCSX2)
- `people_playground.html` — HTML que roda o jogo People Playground no browser (via Unity WebGL / WebAssembly)
- `8-ball-pool-v55.2.3-apkvision.apk` — APK original (não versionado por limite do Git/GitHub)

## Observações

- Os jogos exigem conexão com internet (CDN + game servers).
- As conversões foram feitas a partir das versões web/portas WebAssembly disponíveis.

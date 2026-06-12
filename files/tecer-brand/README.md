# Tecer — pacote de marca

Logotipo da app **Tecer**: símbolo quadrifólio com pétalas alongadas (rácio 3.5:1) construído como interseção evenodd de duas vesicas perpendiculares.

## Cores

| Token | Hex | Uso |
|-------|-----|-----|
| Plum | `#4e1b4a` | Cor principal · sobre fundos claros |
| Branco | `#ffffff` | Sobre fundos escuros, especialmente plum |
| Creme (sugerido) | `#f5efe6` | Fundo neutro alternativo ao branco |

## Tipografia

Wordmark em **Jost Medium (500)**, tracking `-0.025em`, lowercase. As versões SVG do lockup têm o texto convertido em outlines, ou seja, não dependem do tipo de letra estar instalado.

## Ficheiros

### svg/

| Ficheiro | Descrição |
|----------|-----------|
| `tecer-mark.svg` | Apenas o símbolo, plum, viewBox 100×100 |
| `tecer-mark-white.svg` | Apenas o símbolo, branco |
| `tecer-favicon.svg` | Símbolo com troca automática plum↔branco via `prefers-color-scheme` |
| `tecer-logo.svg` | Lockup horizontal (símbolo + wordmark), plum, texto em outlines |
| `tecer-logo-white.svg` | Lockup horizontal, branco |

### png/

Renderizações do símbolo:

| Ficheiro | Tamanho | Uso típico |
|----------|---------|------------|
| `tecer-mark-16.png` | 16×16 | favicon legado |
| `tecer-mark-32.png` | 32×32 | favicon |
| `tecer-mark-48.png` | 48×48 | favicon HiDPI |
| `tecer-mark-64.png` | 64×64 | UI |
| `tecer-mark-128.png` | 128×128 | UI HiDPI |
| `tecer-mark-256.png` | 256×256 | hero / open-graph cards |
| `tecer-mark-512.png` | 512×512 | grande |
| `tecer-mark-1024.png` | 1024×1024 | masters / print |
| `apple-touch-icon-180.png` | 180×180 | iOS home screen |
| `android-chrome-192.png` | 192×192 | Android |
| `android-chrome-512.png` | 512×512 | Android splash |
| `tecer-mark-white-*.png` | vários | versão branca para fundos escuros |
| `tecer-logo-{plum,white}-{80,160,320}h.png` | altura fixa | lockup completo |

## Integração rápida no site

No `<head>`:

```html
<link rel="icon" href="/tecer-favicon.svg" type="image/svg+xml">
<link rel="icon" href="/png/tecer-mark-32.png" sizes="32x32">
<link rel="apple-touch-icon" href="/png/apple-touch-icon-180.png">
```

Logo no header (escala automática):

```html
<img src="/svg/tecer-logo.svg" alt="Tecer" height="40">
```

## Construção geométrica do símbolo

```svg
<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <path fill-rule="evenodd" fill="#4e1b4a"
        d="M 7 50 A 80 80 0 0 1 93 50 A 80 80 0 0 1 7 50 Z
           M 50 7 A 80 80 0 0 1 50 93 A 80 80 0 0 1 50 7 Z"/>
</svg>
```

Duas vesicas (lentes) — uma horizontal, uma vertical — combinadas com `fill-rule="evenodd"` para abrir o losango central em negativo. O símbolo total é uma única `<path>`.

## Margem de respiro mínima

Em redor do símbolo, manter uma margem mínima igual à altura da pétala curta (~25% da dimensão do símbolo). Em redor do lockup, manter uma margem mínima igual à altura da letra "e".

# ENAFIS 2026 — Programação

Página da **programação** do **ENAFIS 2026 – Encontro Nacional de Fiscalização**, promovido pela **SFC/ANTAQ**.

🔗 **Página publicada:** https://antaq.github.io/trilha-enafis-2026/

## Sobre

- **Período:** 21 a 25 de setembro de 2026 · **Local:** Curitiba/PR — Unidade Regional de Curitiba (URECB)
- **Carga horária:** 40 horas · formato híbrido · 5 módulos · 28 atividades
- Página única, estática e responsiva (HTML + CSS + JavaScript, sem build), com a identidade visual da ANTAQ
- Construída a partir do template de [`TrilhaTecnico/index.html`](../../TrilhaTecnico/index.html)

## Recursos

| Recurso | Descrição |
|---|---|
| **Duas visões** | *Cronograma* (linha do tempo dia a dia) e *Módulos* (conteúdo programático agrupado por módulo) |
| **Busca** | Casa tema, palestrante, módulo e também os debatedores do painel de abertura |
| **Filtro por módulo** | Chips coloridos com a contagem de atividades de cada módulo |
| **Navegação por dia** | Chips “Dia 1…Dia 5” com *scrollspy* e realce do dia corrente |
| **Estado temporal** | Contagem regressiva no topo; durante o evento marca a atividade **Agora** e as já **Concluídas** (relógio do navegador) |
| **Painel de abertura** | Card expansível com os 5 debatedores, seus papéis e instituições |
| **Impressão** | Layout dedicado para imprimir / salvar em PDF (botão na barra) |

## Como atualizar o conteúdo

Todo o conteúdo está em dois arrays no [`index.html`](index.html):

- **`MODULOS`** — rótulo, nome, ícone Font Awesome e cores (`mc` traço/texto, `mbg` fundo, `mbd` borda) de cada módulo.
- **`PROGRAMA`** — uma entrada por atividade, em ordem cronológica:

| Campo | Descrição |
|---|---|
| `data` | Data ISO `AAAA-MM-DD` |
| `ini` / `fim` | Horário `HH:MM` (a duração é calculada automaticamente) |
| `mod` | Chave do módulo (`abertura`, `m1`…`m5`, `visita`, `inst`) |
| `icon` | Ícone Font Awesome (ex.: `fa-anchor`) |
| `titulo` | Tema da atividade |
| `pessoas` | Array de palestrantes (opcional) |
| `obs` | Observação exibida abaixo dos palestrantes (opcional) |
| `detalhe` | Bloco expansível com mediação e lista de participantes (opcional) |
| `pausa` | `"intervalo"` ou `"almoco"` — entradas de pausa não têm os campos acima |

Estatísticas, período, contagem de módulos, numeração dos dias, resumo por dia, legenda do rodapé e a visão por módulo são **derivados automaticamente** desses dados.

## Pré-visualizar outra data/hora

No console do navegador, para ver a página como estaria durante o evento:

```js
window.__simularAgora("2026-09-23T10:40");  // Dia 3, durante o GEF Contêineres
window.__simularAgora(null);                // volta ao relógio real
```

## Publicação (GitHub Pages)

A pasta é autossuficiente (`index.html`, `Imagens/`, `favicon.ico`, `.nojekyll`). É servida pela branch `main` (raiz do repositório) em **Settings → Pages** → *Deploy from a branch* → `main` → `/ (root)`.

Qualquer `git push` na `main` republica a página automaticamente.

---

Fonte: [`Programacao-ENAFIS-2026.pdf`](Programacao-ENAFIS-2026.pdf) — programação atualizada pela SFC/ANTAQ em 16/09/2026.

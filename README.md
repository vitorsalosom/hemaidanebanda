# Hemaidan e Banda — Landing page

Site de uma página, feito em HTML/CSS/JS puro. Sem build, sem dependências.

## Como publicar

Qualquer uma destas opções funciona — é só subir a pasta inteira:

- **Netlify Drop** — arraste a pasta em https://app.netlify.com/drop
- **Vercel** — `vercel deploy` na pasta
- **GitHub Pages** — suba a pasta num repositório e ative Pages na branch `main`
- **Hospedagem tradicional** — envie a pasta via FTP para a raiz do domínio

Para testar localmente: `python3 -m http.server` e abra `http://localhost:8000`.

## Estrutura

```
index.html            página inteira (HTML + CSS + JS num arquivo só)
assets/logo.png       logo com fundo transparente
assets/favicon.png    ícone da aba do navegador
assets/fotos/         imagens já otimizadas para web
```

## Como trocar as fotos

| Arquivo | Onde aparece |
|---|---|
| `assets/fotos/c01.jpg` … `c15.jpg` | carrossel 3D (formato retrato 3:4, 900×1200) |
| `assets/fotos/sobre.jpg` | seção "A banda" (retrato 4:5) |
| `assets/fotos/show1–4.jpg` | cards de "Onde já tocamos" (paisagem 3:2) |
| `assets/fotos/crowd.jpg` | seção de contato |
| `assets/fotos/palco.jpg` | mapa de palco no rider |

Basta substituir o arquivo mantendo o mesmo nome e proporção.

Para mudar a quantidade de fotos do carrossel, edite a linha `var COUNT = 15;`
no script no fim do `index.html` e ajuste a lista `captions` logo abaixo.

## Como editar textos

Tudo está direto no `index.html`, em português, separado por comentários de
seção (`<!-- HERO -->`, `<!-- SOBRE -->`, `<!-- RIDER -->`, etc.).

O rider técnico fica no bloco `<!-- RIDER -->`, dividido em quatro cards
(`P.A. e console`, `Monitoração`, `Microfonação`, `Backline`) mais o bloco de
observações. Cada item é um `<li>` da lista `.spec` — para incluir ou remover
exigências, basta editar essas listas.

Contatos aparecem em três lugares: botões do topo, seção de contato e o botão
flutuante do WhatsApp. Procure por `5527997092240` para trocar o número.

## Cores

Definidas como variáveis no topo do CSS (`:root`), tiradas da própria logo:

- turquesa `#14ACB8` · verde `#43A94C` · amarelo `#F7B818` · coral `#EE4A2E`
- fundo creme `#FFF7EC` · texto `#16302F` · teal escuro `#0E5E63`

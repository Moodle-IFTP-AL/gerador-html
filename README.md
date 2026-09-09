# Gerador HTML Moodle — IFTP

Ferramenta interna de produção de conteúdo para o Moodle da formação de
professores do IFTP / SEDUC-AL.

**Endereço:** https://moodle-iftp-al.github.io/gerador-html/

O `index.html` deste repositório é o app inteiro, compilado num arquivo só.
Não se edita este arquivo à mão — ele é gerado a partir do código-fonte.

## Como publicar uma atualização

1. No projeto local, rodar `npm run build`.
2. Abrir `dist/index.html` num editor e conferir que o `<head>` **não**
   menciona `kaspersky`. Se mencionar, apagar a meta tag de
   `Content-Security-Policy`, a `<script>` e a `<link>` que apontam para
   `gc.kis.v2.scr.kaspersky-labs.com` — caso contrário as imagens quebram
   para todo mundo que abrir o site.
3. Aqui no GitHub, abrir o `index.html`, clicar no lápis, apagar tudo, colar o
   conteúdo novo e confirmar (*Commit changes*).
4. Esperar cerca de um minuto. Se a página não mudar, recarregar com
   Ctrl+Shift+R.

## O arquivo `.nojekyll`

Está vazio de propósito. Ele desliga o processamento automático de páginas do
GitHub, que poderia interferir no conteúdo compilado. Não apagar.

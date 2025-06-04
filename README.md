Clonagem Mobile Site Vanessa Paiva

## Descrição do Projeto

Este repositório tem como objetivo clonar fielmente a versão mobile do site Vanessa Paiva a partir do arquivo `index.html` fornecido, organizando todos os arquivos necessários (assets, imagens, fontes, CSS, JS) para deploy como **static site** no Render.com ou serviço similar.

## Como montar o projeto a partir do index.html

### 1. Organização dos arquivos

- Mantenha o `index.html` como arquivo principal.
- Crie as pastas:
  - `/assets` para imagens, logos, ícones, fundos, etc.
  - `/fonts` para arquivos `.woff2`.
  - `/img` para imagens auxiliares, como bandeiras usadas no input de telefone.

- Adicione os arquivos CSS e JS separados:
  - `css.css` (estilo principal)
  - `intlTelInput.css` (separado, usado no campo de telefone)
  - `js.js` (funções JS principais)

### 2. Baixar e referenciar assets locais

- **Baixe todas as imagens** referenciadas no HTML e CSS (logo, favicon, banners, fotos, etc.) e mova para `/assets` ou `/img`.
- **Baixe as bandeiras do plugin intlTelInput** e coloque em `/img/`:
  - `flags.webp`, `flags@2x.webp`, `globe.webp`, `globe@2x.webp`
- **Garanta que todas as fontes customizadas `.woff2` estejam em `/fonts`** e são realmente as usadas pelo site.

### 3. Atualizar referências de caminho

- No `index.html` e arquivos CSS, troque **todas as URLs externas** de imagens, fontes e favicons para caminhos relativos locais.
  - Exemplo:  
    De:  
    `<link rel="icon" href="https://pages.greatpages.com.br/xxx.png">`  
    Para:  
    `<link rel="icon" href="./assets/logo.png">`
- No `intlTelInput.css`, troque:
  - `url("../img/flags.webp")` para `url("./img/flags.webp")` (ajustar path conforme estrutura real).

### 4. Limpeza e otimização

- **Remova scripts de rastreamento (Google Analytics, Facebook Pixel, GTM etc.)** e arquivos .js que não tenham relação com o funcionamento visual do site.
- Exclua qualquer arquivo de mock/teste ou que não seja necessário para o funcionamento do site estático.

### 5. Estrutura final esperada

```plaintext
/
|-- index.html
|-- css.css
|-- intlTelInput.css
|-- js.js
|-- /assets/
|    |-- logo.png
|    |-- foto1.jpg
|    |-- banner1.png
|    |-- ...
|-- /img/
|    |-- flags.webp
|    |-- flags@2x.webp
|    |-- globe.webp
|    |-- globe@2x.webp
|-- /fonts/
|    |-- *.woff2

Clonagem Mobile Site Vanessa Paiva

## Descrição do Projeto

Este repositório tem como objetivo clonar fielmente a versão mobile do site www.vanessapaivacabeleireira.com.br para deploy como **static site** no Render.com ou serviço similar, tudo o que for vinculado ou de contexto ao greatpages é descenessario já que nosso static site no render não tera integração com greatpages.

## Como montar o projeto a partir do index.html

### 1. Organização dos arquivos 

- Crie as pastas:
  - Tendo liberdade para organizar da melhor forma
  - O importante é que sirvam ao proposito que é o clone da pagina.
  

- Adicione os arquivos CSS e JS separados:
  - Os encontrados no link referenciado que é o site oficial
  - Usaremos apenas CSS e JS que sirvam o Meta(facebook e instagram) e que sirvam a estrutura do site.
  - Tudo o que for vinculado ou de contexto ao greatpages é descenessario e não deve fazer parte do nosso projeto.

### 2. Baixar e Organizar

- **Baixe todas as imagens que sirvam para o site em verão mobile, não precisamos de nada para outras plataformas** referenciadas no HTML e CSS (logo, favicon, banners, fotos, etc.) e mova para as pastas que preferir para sua organização.
- **Garanta todas as fontes customizadas que você precisar,que são realmente as usadas pelo site, a organização é você quem define.

### 3. Atualizar referências de caminho

- Arquivos CSS, troque **todas as URLs externas** de imagens, fontes e favicons para caminhos relativos locais que melhor fiquem organizados pra você.

### 4. Limpeza e otimização

- **Remova scripts de rastreamento (Google Analytics, Facebook Pixel, GTM etc.)** e arquivos .js que não tenham relação com o funcionamento visual do site.
- Exclua qualquer arquivo de mock/teste ou que não seja necessário para o funcionamento do site estático.

### 5. Estrutura final esperada é definida por você, apenas citar no final do projeto como ficou.

### Integração de Tracking e Leads (Meta Pixel CAPI)

- Todo envio de lead é feito via AJAX pelo `script.js`, enviando os dados para o proxy no Render.
- O proxy processa, enriquece, loga e encaminha o evento para a API do Facebook, garantindo rastreabilidade, privacidade (hashing) e performance.
- Para garantir a integração perfeita, os campos do formulário devem ter os nomes:
  - `Nome`
  - `E_mail`
  - `Whatsapp`
- O script.js faz persistência de campos no localStorage e coleta UTM/referrer/cookies Meta automaticamente.
- Para eventos adicionais, basta chamar `enviarEvento("NOME_DO_EVENTO")` no JS.

**IMPORTANTE:**  
Qualquer alteração na URL do proxy deve ser atualizada em `script.js`.  
Sempre que criar uma landing nova, lembre-se de incluir esse JS.

---

### Qualquer dúvida ou necessidade antes, durante e depois, podem ser inseridas abaixo:

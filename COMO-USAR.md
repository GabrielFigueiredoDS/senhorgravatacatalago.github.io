# Catálogo Senhor Gravata — como usar

## Estrutura de pastas

```
catalogo-senhor-gravata/
├── index.html              ← o site (não precisa editar)
├── gravatas.json           ← nomes e preços (você edita aqui)
└── assets/
    ├── logo/
    │   └── logo.png         ← coloque o logo da loja aqui, com esse nome exato
    └── gravatas/
        ├── gravata-01/
        │   ├── foto1.jpg
        │   ├── foto2.jpg
        │   └── foto3.jpg
        ├── gravata-02/
        │   ├── foto1.jpg
        │   ├── foto2.jpg
        │   └── foto3.jpg
        ... (até gravata-35, já vêm 35 pastas criadas)
```

## Passo a passo

1. **Logo**: salve a imagem da logo como `logo.png` dentro de `assets/logo/`.
   Se não colocar nada, o site mostra "SG" no lugar, sem dar erro.

2. **Fotos de cada gravata**: em cada pasta `gravata-01`, `gravata-02` etc.,
   coloque exatamente 3 fotos com os nomes `foto1.jpg`, `foto2.jpg`, `foto3.jpg`.
   No site, elas aparecem como um carrossel (setas e bolinhas para trocar a foto).

   Se sua foto for `.png` ou `.jpeg`, troque a extensão do arquivo para `.jpg`
   (renomear funciona, não precisa converter) ou me avise para eu ajustar o código.

3. **Nome e preço**: abra `gravatas.json` em qualquer editor de texto e
   troque "Gravata 01" e "89,90" pelos valores reais. Exemplo:

   ```json
   { "id": "gravata-01", "nome": "Gravata Listrada Azul Marinho", "preco": "129,90" }
   ```

   Importante: o campo `"id"` precisa ser igual ao nome da pasta (gravata-01,
   gravata-02...). Não precisa editar o id, só nome e preço.

4. **Mais de 35 gravatas?** Crie uma nova pasta em `assets/gravatas/`
   (ex: `gravata-36`) e adicione uma nova linha em `gravatas.json` com o
   mesmo id. Pode usar qualquer nome de pasta, não precisa ser sequencial.

5. **Busca**: o site já tem uma barra de busca por nome, funciona automaticamente.

## Publicar como site (link)

A forma mais simples e gratuita é o **GitHub Pages** ou **Netlify Drop**:

- **Netlify Drop** (mais fácil, sem conta): acesse https://app.netlify.com/drop
  e arraste a pasta inteira `catalogo-senhor-gravata`. Em segundos você recebe
  um link público (ex: `senhor-gravata.netlify.app`).

- **GitHub Pages**: crie um repositório, suba esses arquivos, e ative o Pages
  nas configurações do repositório.

Qualquer uma das duas opções gera um link que você pode compartilhar com clientes.

## Testar no seu computador antes de publicar

Como o navegador bloqueia o carregamento do `gravatas.json` se você apenas
clicar duas vezes no `index.html`, rode um servidor local simples:

- Se tiver Python instalado: abra um terminal dentro da pasta e digite
  `python -m http.server 8000`, depois acesse `http://localhost:8000` no navegador.
- Ou simplesmente pule essa etapa e já publique direto no Netlify Drop —
  lá funciona sem precisar testar localmente.

# Luary Shop — imagens de produtos

Repositório público de imagens de produtos usadas no catálogo e nos marketplaces da Luary Shop. Não coloque neste repositório tokens, arquivos `.env`, dados de clientes ou qualquer material privado.

## Organização

Use a categoria e o SKU para encontrar rapidamente as fotos:

```text
catalogo/<categoria>/<SKU>/<SKU>-01-capa.webp
catalogo/<categoria>/<SKU>/<SKU>-02-detalhe.webp
catalogo/<categoria>/<SKU>/<SKU>-03-verso.webp
```

Exemplo: `catalogo/aneis/ANEL-001/ANEL-001-01-capa.webp`.

Use nomes ASCII sem espaços ou acentos. Numere as fotos na ordem que devem aparecer. Para substituir uma imagem já publicada no CDN, prefira um novo nome (`...-v2.webp`) para não depender do cache do URL anterior.

## URL CDN de exemplo

Depois de criar este repositório público como `luaryshop/luary-marketplace-images`, uma imagem em `catalogo/aneis/ANEL-001/ANEL-001-01-capa.webp` pode ser acessada por:

```text
https://cdn.jsdelivr.net/gh/luaryshop/luary-marketplace-images@main/catalogo/aneis/ANEL-001/ANEL-001-01-capa.webp
```

Confirme que o link abre a imagem diretamente sem login antes de cadastrá-lo em um marketplace. Regras de formato, tamanho e quantidade devem ser verificadas por canal e categoria.

## Regras do repositório

- Armazene arquivos de imagem originais e públicos; evite duplicar a mesma foto por marketplace.
- Prefira imagens otimizadas em WebP quando compatíveis com o canal; mantenha uma versão JPEG pronta caso uma integração não aceite WebP.
- Mantenha cada arquivo abaixo de 5 MB para facilitar o upload pelo app, salvo se o projeto for alterado e testado para outro limite.
- Não sobrescreva repetidamente o mesmo caminho de imagem; use nomes versionados para atualizações.
- Guarde o token de escrita somente como variável de ambiente do backend Luary. Nunca salve tokens neste repositório.

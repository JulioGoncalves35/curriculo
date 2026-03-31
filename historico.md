# Histórico de Alterações

- **Data/Hora**: 31/03/2026
- **Arquivo Editado**: `index.html`
- **Problema Relatado**: Os pôsteres dos filmes mais recentes, adicionados copiando o endereço de imagem do IMDb, não estavam carregando ou apareciam quebrados.
- **Causa**: Os servidores de imagem do IMDb (`m.media-amazon.com`) possuem uma proteção (anti-hotlinking) que bloqueia o carregamento das imagens quando detectam que elas estão sendo solicitadas por um site de terceiros.
- **Solução Aplicada**: Foi adicionada a tag `<meta name="referrer" content="no-referrer">` dentro da seção `<head>` do arquivo `index.html`. 
- **Resultado**: Com essa meta tag, o navegador web do usuário não avisa aos servidores da Amazon de onde a imagem está sendo carregada, o que "engana" a proteção e permite que todos os pôsteres do IMDb sejam exibidos normalmente no seu currículo.

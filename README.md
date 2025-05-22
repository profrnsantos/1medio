catalogo-videos-expandido/
├── public/
│   ├── index.html            // Página Principal: Lista todos os vídeos
│   ├── recomendacoes.html    // Página de Recomendações
│   ├── ranking.html          // Página de Ranking de Aprovação
│   ├── css/
│   │   └── style.css         // Seu CSS principal
│   ├── js/
│   │   ├── script.js         // JavaScript para carregar e exibir vídeos (compartilhado)
│   │   └── ranking.js        // JavaScript específico para a página de ranking (lógica de aprovação)
│   └── images/
│       └── logo.png          // Logo ou ícones
└── data/
    └── videos.json           // Seus dados dos vídeos (agora com um campo de aprovação!)

🚀 Começando o Projeto Diretamente no GitHub
Siga estes passos para configurar e desenvolver seu catálogo de vídeos sem precisar da linha de comando inicialmente.

1. Preparando Seu Repositório
Crie um Novo Repositório no GitHub:
Acesse github.com e faça login (ou crie uma conta).
Clique no botão + (canto superior direito) e selecione New repository.
Dê o nome de catalogo-de-videos ao seu repositório.
Marque a opção Add a README file para criar este arquivo automaticamente.
Clique em Create repository.
2. Criando a Estrutura de Pastas e Arquivos no GitHub (Vazio)
Vamos criar as pastas e os arquivos necessários diretamente no site do GitHub. Lembre-se que, para uma pasta aparecer, ela precisa conter um arquivo dentro dela.
**Seguiremos a estrutura como no modelo acima do início deste arquivo.

Na página principal do seu repositório, clique no botão Add file (verde, no topo) e depois em Create new file.
No campo "Name your file...", digite: public/
Quando digitar a / irá abrir um espaço para digitar o nome do arquivo, digite: index.html
Deixe o conteúdo do arquivo vazio por enquanto.
Role para baixo, adicione uma mensagem de commit (ex: Cria pasta public e index.html) e clique em Commit new file.
Crie a pasta public/css/ e o arquivo public/css/style.css:

Repita o passo anterior, dentro da pasta public clique em: Add file > Create new file.
No campo "Name your file...", digite: css/
Quando digitar a / irá abrir um espaço para digitar o nome do arquivo, digite: style.css
Deixe o conteúdo vazio.
Mensagem de commit: Cria pasta css e style.css
Clique em Commit new file.

Crie a pasta public/js/ e o arquivo public/js/script.js:

Repita o processo.
Nome: public/js/script.js
Conteúdo vazio.
Mensagem de commit: Cria pasta js e script.js
Clique em Commit new file.
Crie o arquivo public/js/ranking.js:

Repita o processo.
Nome: public/js/ranking.js
Conteúdo vazio.
Mensagem de commit: Cria ranking.js
Clique em Commit new file.
Crie a pasta public/images/ e o arquivo public/images/logo.png (ou outro):

Aqui você não vai criar um arquivo de texto, mas sim um espaço para uma imagem. Para que a pasta apareça, você pode criar um arquivo temporário.
Nome: public/images/placeholder.txt (Este será removido depois que você adicionar uma imagem de verdade).
Conteúdo vazio.
Mensagem de commit: Cria pasta images
Clique em Commit new file.
Crie a pasta data/ e o arquivo data/videos.json:

Repita o processo.
Nome: data/videos.json
Conteúdo vazio.
Mensagem de commit: Cria pasta data e videos.json
Clique em Commit new file.
Crie o arquivo public/recomendacoes.html:

Repita o processo.
Nome: public/recomendacoes.html
Conteúdo vazio.
Mensagem de commit: Cria recomendacoes.html
Clique em Commit new file.
Crie o arquivo public/ranking.html:

Repita o processo.
Nome: public/ranking.html
Conteúdo vazio.
Mensagem de commit: Cria ranking.html
Clique em Commit new file.
Crie o arquivo listas_de_videos.txt:

Repita o processo. Este arquivo ficará na raiz do seu repositório (não dentro de public/ ou data/).
Nome: listas_de_videos.txt
Conteúdo vazio.
Mensagem de commit: Cria listas_de_videos.txt
Clique em Commit new file.
Agora você tem a estrutura de pastas e todos os arquivos vazios criados diretamente no seu repositório do GitHub!

3. Gerando Sua Lista de Vídeos com o Gemini
Antes de preencher o videos.json, vamos criar uma lista inicial para facilitar.

Peça ao Gemini para Gerar a Lista:

Prompt para o Gemini:
Gere uma lista de 20 URLs de clipes musicais populares do YouTube que eu gostaria de incluir em um catálogo de vídeos. Por favor, forneça apenas as URLs completas.

Edite: Copie a lista de URLs gerada pelo Gemini.
Preencha listas_de_videos.txt no GitHub:

No seu repositório do GitHub, navegue até o arquivo listas_de_videos.txt que você criou.
Clique no ícone de lápis (editar) no canto superior direito do arquivo.
Cole as URLs que você obteve do Gemini.
Role para baixo, adicione uma mensagem de commit (ex: Adiciona lista de URLs de vídeos musicais) e clique em Commit changes.

4. Preenchendo os Arquivos com a Ajuda da IA (Gemini)
Agora que você tem os arquivos vazios e uma lista de vídeos, vamos preenchê-los. Para editar os arquivos, navegue até o arquivo no GitHub e clique no ícone de lápis (editar). Após colar o conteúdo, sempre faça um commit na parte inferior da página.

4.1. data/videos.json (Seu "Banco de Dados" de Vídeos)
Este arquivo armazenará as informações de todos os seus vídeos.

Abra para Editar: No GitHub, clique em data/videos.json e depois no ícone de lápis (editar).
Peça ao Gemini:
Prompt para o Gemini:
Usando a lista de 20 URLs de vídeos musicais que eu te dei, crie um arquivo JSON com uma lista desses 20 vídeos para um catálogo. Para cada vídeo, inclua os campos:
"id" (único, ex: "v1", "v2", ...),
"youtubeId" (apenas o ID do vídeo do YouTube extraído da URL),
"titulo" (um título adequado para o clipe),
"descricao" (uma breve descrição do clipe),
"categoria": "Música",
"aprovacao" (um número inicial de 1 a 10, variado),
"recomendado" (true ou false, para alguns aleatoriamente).
Me forneça as URLs das miniaturas padrão de alta qualidade do YouTube para cada ID de vídeo (ex: https://i.ytimg.com/vi/ID_DO_VIDEO/hq720.jpg).

[COLE AQUI A LISTA DE 20 URLs DE VÍDEOS MUSICAIS DO SEU ARQUIVO listas_de_videos.txt]
Edite: Copie o JSON gerado pelo Gemini e cole no seu arquivo videos.json no GitHub. Revise os dados e personalize se quiser.
Commit as mudanças.
4.2. public/index.html (Página Principal)
Esta é a página de entrada do seu catálogo, onde todos os vídeos serão listados.

Abra para Editar: No GitHub, clique em public/index.html e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie o código HTML completo para a página principal de um catálogo de vídeos.
Deve ter um cabeçalho (<header>) com o título do site e uma navegação (<nav>) para as páginas "Home" (link para index.html), "Recomendações" (link para recomendacoes.html) e "Ranking" (link para ranking.html).
No corpo (<main>), deve ter uma div com id "videos-container" onde os vídeos serão listados dinamicamente pelo JavaScript.
Inclua um rodapé (<footer>) simples.
Ligue para um arquivo CSS chamado "css/style.css" e um JavaScript chamado "js/script.js".
Edite: Copie o HTML gerado e cole no seu index.html. Adapte os textos, como o título do site.
Commit as mudanças.
4.3. public/recomendacoes.html (Página de Recomendações)
Esta página mostrará apenas os vídeos que você marcou como "recomendados".

Abra para Editar: No GitHub, clique em public/recomendacoes.html e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie o código HTML para a página de recomendações de um catálogo de vídeos.
O cabeçalho e a navegação devem ser os mesmos da página principal (links para index.html, recomendacoes.html, ranking.html).
O corpo deve ter um título "Vídeos Recomendados" e uma div com id "videos-container-recomendados" para a lista de vídeos.
O rodapé deve ser o mesmo.
Ligue para o mesmo arquivo CSS "css/style.css" e o mesmo JavaScript "js/script.js".
Edite: Copie o HTML e cole. Certifique-se de que o id da div no main seja videos-container-recomendados.
Commit as mudanças.
4.4. public/ranking.html (Página de Ranking de Aprovação)
Esta página exibirá os vídeos classificados pelo seu índice de aprovação.

Abra para Editar: No GitHub, clique em public/ranking.html e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie o código HTML para a página de ranking de vídeos.
O cabeçalho e a navegação devem ser os mesmos da página principal (links para index.html, recomendacoes.html, ranking.html).
O corpo deve ter um título "Ranking de Vídeos" e uma div com id "ranking-container" para a lista de vídeos.
O rodapé deve ser o mesmo.
Ligue para o mesmo arquivo CSS "css/style.css" e um JavaScript chamado "js/ranking.js".
Edite: Copie o HTML e cole. Verifique o id da div no main (ranking-container) e que ele está ligando para js/ranking.js.
Commit as mudanças.
4.5. public/css/style.css (Estilo Visual do Site)
Aqui você dará vida visual ao seu projeto.

Abra para Editar: No GitHub, clique em public/css/style.css e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie um código CSS para um catálogo de vídeos com cabeçalho, navegação, rodapé, e cards de vídeo.
Defina um estilo geral para o corpo (fonte, cor de fundo, espaçamento).
Estilize o cabeçalho, navegação (links flutuantes ou flexbox), rodapé.
Crie estilos para os cards de vídeo (uma div com classe .video-card), incluindo:
    - Dimensões e borda para o card.
    - Estilos para a imagem (img com classe .video-thumbnail) dentro do card.
    - Estilos para o título (h3) do vídeo.
Adicione estilos para o modal de vídeo (que deve ser invisível por padrão e aparecer com display: flex;).
Crie um layout de grade para os cards (usando display: grid ou flexbox com wrap) para as divs "videos-container" e "videos-container-recomendados".
Crie estilos para a lista de ranking (div com id "ranking-container") e seus itens.
Garanta que o layout seja responsivo para telas menores.
Edite: Cole o CSS gerado. Use o Canva para inspiração!
Inspiração com Canva: No Canva, você pode criar designs para "miniaturas de vídeo", "banners de site", "paletas de cores" ou até "layouts de cards". Use as ideias de cores, fontes e espaçamento para refinar seu CSS.
Commit as mudanças.
4.6. public/js/script.js (Lógica Comum das Páginas)
Este JavaScript carregará os vídeos e os exibirá nas páginas principal e de recomendações.

Abra para Editar: No GitHub, clique em public/js/script.js e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie um JavaScript para um catálogo de vídeos.
1. Deve buscar os dados do arquivo './data/videos.json' (usando fetch).
2. Crie uma função `renderVideos(videosToRender, containerId)` que recebe um array de vídeos e o ID da div onde eles serão exibidos. Esta função deve:
    - Criar dinamicamente elementos HTML para cada vídeo (div com classe .video-card, img.video-thumbnail para a miniatura, h3 para o título).
    - Adicionar um evento de clique a cada card de vídeo.
    - Ao clicar, um modal (que deve ser uma div no HTML com id "video-modal" e um iframe dentro com id "youtube-player") deve ser aberto e carregar o iframe do YouTube usando o youtubeId do vídeo e autoplay=1.
    - O modal deve ter um botão para fechar.
3. Implemente um evento `DOMContentLoaded` para:
    - Chamar `renderVideos` para a div "videos-container" (para a `index.html`) com todos os vídeos.
    - Se a página atual for `recomendacoes.html` (verifique `window.location.pathname`), filtre os vídeos para mostrar apenas aqueles com "recomendado: true" e chame `renderVideos` para a div "videos-container-recomendados".
Edite: Cole o código. Este será um dos arquivos mais importantes.
Commit as mudanças.
4.7. public/js/ranking.js (Lógica da Página de Ranking)
Este JavaScript é específico para a página de ranking, lidando com a aprovação dos vídeos.

Abra para Editar: No GitHub, clique em public/js/ranking.js e depois no ícone de lápis.
Peça ao Gemini:
Prompt para o Gemini:
Crie um JavaScript para a página de ranking de vídeos.
1. Deve buscar os dados do arquivo './data/videos.json' (usando fetch).
2. Crie uma função `loadAndRenderRanking()` que:
    - Carrega os vídeos do 'videos.json'.
    - Carrega os níveis de aprovação do `localStorage` (se existirem, caso contrário usa os do JSON como valores iniciais). As aprovações do localStorage devem ser salvas como um objeto, ex: `{ "v1": 8, "v2": 10 }`.
    - Ordena os vídeos do maior para o menor "aprovacao".
    - Renderiza a lista de vídeos na div com id "ranking-container", mostrando o título, a aprovação atual e um botão "👍 Aprovar" para cada vídeo.
    - Adiciona um evento de clique para o botão "Aprovar": quando clicado, incrementa a aprovação do vídeo no `localStorage` e depois chama `loadAndRenderRanking()` novamente para atualizar o ranking na tela.
3. Implemente um evento `DOMContentLoaded` para chamar `loadAndRenderRanking()`.
Edite: Cole o código. Esta parte é um pouco mais complexa devido ao localStorage.
Commit as mudanças.
5. Testando e Publicando Seu Projeto
Abra seus arquivos localmente (Opcional, mas Recomendado): Para um teste mais rápido antes de publicar, você pode clonar o repositório para seu computador (git clone [URL]) e abrir o index.html (e depois as outras páginas) diretamente no navegador. Isso permite ver as mudanças instantaneamente.
Ajuste o CSS: Use as ferramentas de desenvolvedor do navegador (F12) para inspecionar os elementos e ajustar seu style.css até que tudo pareça perfeito.
Depure o JavaScript: Se algo não funcionar, use o console do navegador (F12 -> Console) para ver mensagens de erro e depurar seu código JavaScript. O Gemini também pode ajudar a depurar!
Prompt para o Gemini (exemplo): "Por que este código JavaScript não está carregando os vídeos da div 'videos-container'? [Cole seu código JS aqui]"
6. Publicando Seu Site com GitHub Pages
Esta é a etapa final para compartilhar seu catálogo de vídeos com o mundo!

Verifique se todas as suas mudanças foram commitadas e enviadas para o GitHub. (Se você seguiu os passos acima editando diretamente no GitHub, elas já estão lá).

Configure o GitHub Pages:

Vá para o seu repositório no GitHub.
Clique na aba Settings (Configurações).
No menu lateral esquerdo, clique em Pages.
Em Build and deployment, em Source, selecione Deploy from a branch.
Em Branch, selecione a branch main (ou master) e a pasta /public.
Clique em Save.
Aguarde alguns minutos. O GitHub Pages irá construir e publicar seu site. Você verá uma mensagem indicando que "Your site is live at..." com a URL do seu catálogo!
💡 Dicas Extras e Próximos Passos
Imagens: Substitua o public/images/placeholder.txt por imagens reais (como um logo ou ícones) fazendo upload diretamente no GitHub ou usando a linha de comando.
Responsividade: Certifique-se de que seu site se adapte bem a diferentes tamanhos de tela (celulares, tablets).
Acessibilidade: Pense em usuários com deficiência visual. Use tags HTML semânticas e textos alternativos para imagens.
Mais Vídeos: Adicione muitos mais vídeos ao seu videos.json!
Funcionalidades Avançadas (Futuro):
Barra de busca/filtro de vídeos por categoria.
Sistema de "curtir" ou "descurtir" mais elaborado.
Integração com a API oficial do YouTube (mais complexo, mas permite buscar vídeos em tempo real).
Divirta-se criando e aprimorando seu catálogo de vídeos! Se tiver dúvidas, consulte a documentação do HTML, CSS, JavaScript ou use o Gemini para te ajudar.
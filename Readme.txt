No backend, configurei uma rota POST /api/articles que recebe os dados enviados pelo formulário de cadastro de artigos no frontend. 
Nessa rota, implementei a lógica para salvar o artigo no banco de dados MongoDB. 
Para isso, validei os campos obrigatórios, como name, title, e content, e verifiquei se já existia um artigo com o mesmo name no banco de dados, 
garantindo que o campo name seja único.

Se os dados fossem válidos e o name não estivesse duplicado, inseri o novo artigo na coleção articles, contendo os campos name, title, content, upvotes 
(inicializado em 0), e uma lista vazia de comments. Caso tudo corresse bem, o backend retornava uma mensagem de sucesso para o frontend.
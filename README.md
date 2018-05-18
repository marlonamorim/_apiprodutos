# _apiprodutos
Web Api com base em autorização JWT e ORM EF Core  In Memory

## Etapas para gerar um container local (Docker).
1.	Compilar o projeto (a patir do menu Build > Build Solution).
2.	Executar o comando docker images no PowerShell
a.	Será exibido o repositório com o nome apiprodutos e tag latest.
3.	Executar o comando docker tag apiprodutos:latest repositoriodockerhub/projectdockhub
a.	Onde o repositório informado “repositoriodockerhub/projectdockhub” é o repositório da sua conta no Docker Hub.
4.	Execute novamente o comando docker images no PowerShell
a.	Será exibido um repositório com o mesmo nome da tag que foi fornecida, “repositoriodockerhub/projectdockhub”
5.	Crie o container da imagem com o comando, docker run –p 12345:80 –name testeapiprodutos –d mgm1988/apiprodutos
a.	Onde -p é o comando para informar a porta do container, -d é o comando para executar o container em segundo plano e –name é o comando para informar o nome do container.

## Etapas para publicação e download de uma imagem no repositório do Docker Hub.
1.	Efetue login no docker com o comando, docker login
a.	Informe usuário e senha.
2.	Efetue a publicação da imagem com o comando, docker push repositoriodockerhub/projectdockhub
3.	Faça download da imagem no Docker Hube com o comando, docker pull repositoriodockerhub/projectdockhub

## Etapas para publicação de uma imagem no repositório do Docker Hub a partir do Visual Studio.
1.	Clique com o botão direito no projeto e selecione “Publishing”
2.	Em Publish, clicar sobre o item Container Registry, marcando em seguida a opção (radio button) Docker Hub
3.	Clique no botão Publish
4.	Será exibida uma janela (Container Registry) solicitando as credenciais para acesso ao Docker Hub
5.	Entre com as credenciais e verifique no Docker Hub se a imagem consta no repositório.

## Etapas para publicação do container no Azure
1.	Crie um novo recurso no Azure.
2.	Na configuração do container, selecione Docker Hub e acesso público (como configurado no Docker Hub)
3.	Insira sua imagem no campo obrigatório (repositóriodockerhub/projetodockerhub)
4.	Clique em Ok e Criar
5.	Vá em Overview/Visão geral e acesse a URL do aplicativo

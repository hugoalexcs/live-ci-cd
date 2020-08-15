 # Envia projeto para um container no google plataform
docker build -t gcr.io/fullcycle-examples/live-ci-cd:latest .

# Run projeto no container
docker run -p 8080:8080 gcr.io/fullcycle-examples/lime-ci-cd:latest

# Subir a imagem para o container register
 docker push gcr.io/fullcycle-exemples/live-ci-cd:latest

 # Criar um repositorio no github
 live-ci-cd

 # Configurações do repositorio com Google Cloud Build
 gcp.login

 # Criar um projeto chamado fullcycle-examples
 Abra o menu CLoud Build --> Acionadores

 # Conecta ao repositorio do Github

 # Cria um gatilho
 Editar Gatilho
 Qualquer push dado ao github o gatilho será rodado
 Deixar como detecção automatica (.yml)

Ciar arquivo chamado cloudbuild.yaml
$SHOT_SHA variavel que pegar o hash do commit para versionar a imagem





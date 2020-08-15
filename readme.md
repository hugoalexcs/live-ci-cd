# Configuração do cloudbuild.yaml
https://cloud.google.com/cloud-build/docs/build-config

 # Envia projeto para um container no google plataform
docker build -t gcr.io/fullcycle-examples/live-ci-cd:latest .

# Run projeto no container
docker run -p 8080:8080 gcr.io/fullcycle-examples/live-ci-cd:latest

# ativar Google Container Registry API
https://cloud.google.com/iam/docs/creating-managing-service-account-keys#creating_service_account_keys
https://cloud.google.com/container-registry/docs/advanced-authentication#gcloud-helper
https://cloud.google.com/sdk/docs?authuser=1
https://cloud.google.com/container-registry/
https://cloud.google.com/container-registry/docs/advanced-authentication#json_key_file
https://cloud.google.com/container-registry/docs/pushing-and-pulling
gcloud auth configure-docker
 https://gcr.io
 docker login gcr.io 
# Ativar o Google Storage

https://cloud.google.com/sdk/docs?authuser=1
 gcloud config set project PROJECT_ID
 gcloud auth activate-service-account test-service-account@google.com --key-file=/path/key.json --project=testproject
 gcloud auth activate-service-account --key-file key-file.json

# Subir a imagem para o container register
 docker push gcr.io/fullcycle-examples/live-ci-cd:latest

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


# - name: 'docker' 
#    args: ['push', 'gcr.io/fullcycle-examples/live-ci-cd:latest']

# - name: 'docker'
#    args: ['push', 'gcr.io/fullcycle-examples/live-ci-cd:$SHOT_SHA']


# Configurações no GitHub
Acessa as configurações do repositorio --> barnches --> add rules
branch name: master
Habilita: Require status checks to pass before merging

# Editar o gatilho do google cloud
Fonte: master
Habilita: Inverter Regex (O trigger deve rodar para qualquer push no github diferente do master)


Enabling branch restrictions


# https://github.com/codeedu/live-ci-cd/blob/master/cloudbuild.dev.yaml

# Deploy master
Google cloud run  --> serviço gerenciado do google para trabalhar com container


# Kubernetes Engine --> clusters
Okestrador de containers

# COnectar ao clusters direto
gcloud container clusters get-credentials fullcycle --zone us-central1-c --project fullcycle-examples
 # Install KUBERNETES
 https://kubernetes.io/docs/tasks/tools/install-kubectl/

kubectl get nodes
kubectl apply -f k8s.yaml

Acessar o google cloud e selecionar carga de trabalho
Acessar depois serviços e verifica se estar tudo ok, verifica o IP: este aponta para o loadbalance
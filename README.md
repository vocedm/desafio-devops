# Desafio DevOps - Kubernetes
## Motivação
Kubernetes atualmente é a principal ferramenta de orquestração e deployment de containers utilizada no mundo, práticamente tornando-se um padrão para abstração de recursos de infraestrutura.

Na DMCard temos varios serviços que são containerizados e distribuídos em clusters para cada ambiente, sendo assim é importante que as aplicações sejam adaptáveis para cada ambiente e haja controle via código dos recursos kubernetes através de seus manifestos.

## Objetivo
Dentro deste repositório existem dois subdiretórios service-1 e service-2, cada um deles tem um Dockerfile que constrói a imagem para cada um dos serviços, seu objetivo é:

- Construir a imagem docker da aplicação
- Criar os manifestos de recursos kubernetes para rodar a aplicação (deployments, services, ingresses, configmap e qualquer outro que você considere necessário)
- Criar um script para a execução do deploy em uma única execução.
- A aplicação deve ter seu deploy realizado com uma única linha de comando em um cluster kubernetes local
- Todos os pods devem estar rodando
- A aplicação deve responder à uma URL específica configurada no ingress

## Extras
- Utilizar Helm HELM
- Divisão de recursos por namespaces
- Utilização de health check na aplicação
- Fazer com que a aplicação exiba seu nome ao invés de "Hello, candidate!"

## Notas
Pode se utilizar o Minikube ou Docker for Mac/Windows para execução do desafio e realização de testes.

A aplicação do service-1 sobe por default utilizando a porta 3000 e a aplicação do service-2 sobre por default utilizando a porta 8000 e cada uma delas utiliza uma variável de ambiente $NAME.

Não é necessário realizar o upload das imagens Docker para um registro público, você pode construir a imagem localmente e utilizá-la diretamente.

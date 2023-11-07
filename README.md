# Tech-Challenge-Auth
## Overview
Este projeto é uma solução serverless que autentica usuários com base em seu CPF e senha através da integração com o AWS Cognito. Ele fornece um endpoint que aceita o CPF e senha, valida o formato do CPF, e então tenta autenticar o usuário com o AWS Cognito.

## Estrutura do Projeto
- auth  - Contém o código fonte para a função Lambda responsável pela autenticação.
- events - Eventos de invocação que você pode usar para testar a função.
- tests - Testes unitários para o código do projeto.
- template.yaml - Um modelo que define os recursos AWS da aplicação.

O aplicativo utiliza vários recursos da AWS, incluindo funções Lambda e uma API do API Gateway. Estes recursos estão definidos no arquivo template.yaml deste projeto. Você pode atualizar o template para adicionar mais recursos AWS através do mesmo processo de implantação que atualiza o código da sua aplicação.

## Como implantar
1 Pré-requisitos:
- SAM CLI - Instalar o SAM CLI
- Python 3
- Docker - Instalar Docker Community Edition

2 Construção e Implantação:
``````
bash
Copy code
sam build --use-container
sam deploy --guided
``````

3 Testar localmente:
- Construa a aplicação com sam build --use-container.
- Invoque a função diretamente com um evento de teste: sam local invoke HelloWorldFunction --event events/event.json.
- Ou simule a API localmente em localhost:3000: sam local start-api.

## Limpeza
Para excluir a aplicação implantada, você pode usar:
``````
bash
Copy code
sam delete --stack-name "tech-challenge-auth"
``````

## Recursos Adicionais
Para um entendimento mais profundo do AWS SAM, consulte o guia do desenvolvedor do AWS SAM.https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html

Se você estiver interessado em explorar mais sobre aplicações serverless, considere verificar o AWS Serverless Application Repository https://aws.amazon.com/serverless/serverlessrepo/ para implantar aplicativos prontos para uso que vão além dos exemplos básicos.


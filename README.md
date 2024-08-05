# alura-jenkins

## Subindo o jenkins
``` shell
docker run -p 8080:8080 \
           -p 8085:8085 \
           -d jenkins/jenkins:2.263.2-lts-centos

## user=fulano / password=pass
curl http://localhost:8085/login
xdg-open http://localhost:8085/leiloes
```

## Jobs
- tests: `clean test`
- deploy: `BUILD_ID="deploy" java -Dspring.profiles.active=prod -jar target/leilao*.jar &`

## Observações
- É necessário logar no container do jenkins e instalar o maven, além de instalar seu respectivo plugin

## Plugins
- Folders
- Matrix
- Maven
- Slack Notifications
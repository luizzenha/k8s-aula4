
# Aula de kubernetes

Obs: Projeto executado localmente utilizando kubernetes do Docker Desktop

### Para executar e subir os pods:
``` kubectl apply -f service  ```

Esse comando irá executar os services e os dois pods de MySQL e NGINX

### Para testar: 

Abra o browser e verifique se está carregando pagina do NGINX no seguinte endereco:

``` 127.0.0.1 ```

Para testar o mysql execute a seguinte linha para subirmos um pod e acessar o mysql-client atrvés do nome servico quer irá direcionar o tráfego para o pod correto do mysql

``` kubectl run -it --rm --image=mysql:5.6 --restart=Never mysql-client -- mysql -h myapp-db-svc -pTeste@1234 ```

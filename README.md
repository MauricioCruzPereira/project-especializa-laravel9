## Aprendizado do projeto
* Aprendendo a tratar melhor a separação de responsabilidade, tendo um repository para lidar com as ações do banco, o service para disponibilizar os métodos e o controller para lidar com as rotas. Além disso utilizando o dto para mapear as colunas necessárias no store e no update e também a utilização de enums.

## Passo a passo para rodar o projeto
Clone o projeto
```sh
git clone https://github.com/MauricioCruzPereira/project-especializa-laravel9.git laravel-10
```
```sh
cd laravel-10/
```

```sh
git config core.fileMode false
```

```sh
sudo chmod -R 777 .
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize essas variáveis de ambiente no arquivo .env
```dosini
APP_NAME="name"
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=nome_usuario
DB_PASSWORD=senha_aqui

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```

Instale as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

Crie as tabela do banco
```sh
php artisan migrate
```

* *OBS:* Caso ao rodar o comando de teste ou de migrate apresentar um erro de conectividade de bando de dados, siga os passoa a baixo:*
  * Linux:/etc/hosts
  * Windows: C:\Windows\System32\drivers\etc\hosts
  * Nesse arquivo adicionar a seguinte linha: 
  ```bash
    127.0.0.1	db
  ```

Acesse o projeto
[http://localhost](http://localhost)

# Projeto

* Curso utilizado para o aprendizado.
- :movie_camera: [Acesse o Curso](https://www.youtube.com/watch?v=AN-LZuw2GIc&list=PLVSNL1PHDWvQ1N6fqhQ5HQzFtN-xrkjNU&ab_channel=CarlosFerreira-EspecializaTi).

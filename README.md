Projeto base Wordpress
- User para iniciar um projeto novo; 
- Ou para rodar um já existente.

## Sumário

- [Requisitos para execução do projeto](#requisitos-para-execução-do-projeto)
- [Tecnologias em destaque](#tecnologias-em-destaque)
- [Configurar o projeto](#configurar-o-projeto)
- [Executar o projeto](#executar-o-projeto)

## Requisitos para execução do projeto:

+ [Docker](https://www.docker.com/)

## Tecnologias em destaque

+ [Wordpress](https://br.wordpress.org/)
+ [Mysql](https://www.mysql.com/)
+ [Docker](https://www.docker.com/)
+ [phpmyadmin](https://www.phpmyadmin.net/)

## Configurar o projeto

Baixe ou clone este projeto para sua máquina.

### Novo projeto: 
1. Baixe o wordpress e descompacte o conteúdo na pasta **wordpress**.
2. Configure o [wp-config.php](#configurar-o-wordpress)

### Projeto antigo: 
1. Baixe todos os arquivos do site e coloque na pasta **wordpress**.
2. Configure o [wp-config.php](#configurar-o-wordpress)
3. Coloque o dump do banco de dados (arquivo sql) dentro da pasta **dump**.

> Se tudo estiver correto com a execução, o arquivo dump, será executado o banco será totalmente clonado.

### Configurar o Wordpress

No arquivo wp-config.php, configure os dados do banco como o exemplo a baixo:

```php
define('DB_NAME', 'wordpressdb');
/** Usuário do banco de dados MySQL */
define('DB_USER', 'dbuser');
/** Senha do banco de dados MySQL */
define('DB_PASSWORD', 'dbpassword');
/** Nome do host do MySQL */
define('DB_HOST', 'db');
/** Charset do banco de dados a ser usado na criação das tabelas. */
define('DB_CHARSET', 'utf8mb4');
/** O tipo de Collate do banco de dados. Não altere isso se tiver dúvidas. */
define('DB_COLLATE', '');
```

> Se desejar utilizar outros valores para login e senha, lembre de atualizar o arquivo ***docker-compose.yml***.

> Não mexa no campo **DB_HOST** a menos que saiba, o que esta fazendo.

## Executar o projeto

Rode o comando do docker-compose:

```bash
> docker-compose up
```

Acesse a URL do wordpress:

[http://localhost:8080/](http://localhost:8080/)

Acesse a URL do phpmyadmin:

[http://localhost:8000/](http://localhost:8000/)


## Sumário

- [Requisitos para execução do projeto](#requisitos-para-execução-do-projeto)
- [Tecnologias em destaque](#tecnologias-em-destaque)
- [Configurar o projeto](#configurar-o-projeto)
- [Executar o projeto](#executar-o-projeto)
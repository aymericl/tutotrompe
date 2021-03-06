# tutotrompe-sf4-api-jwt

## Stack technique requis 

- PHP 7.2 min.
- MySQL 5.8 min.

## Informations de connexion

Utilisateurs créés via les fixtures :
- admin@attineos.com / admin
- user@attineos.com / user

## Installation 

- Modifier la DATABASE_URL dans le .env

- ```composer install```

- ```php bin/console doctrine:migrations:migrate```

- ```php bin/console doctrine:fixtures:load```

## Installation du bundle pour la gestion des JWT

- ```composer require lexik/jwt-authentication-bundle```

- Générer une clé publique et privée avec une passphrase à reporter dans le .env

```
$ mkdir -p config/jwt
$ openssl genrsa -out config/jwt/private.pem -aes256 4096
$ openssl rsa -pubout -in config/jwt/private.pem -out config/jwt/public.pem
```
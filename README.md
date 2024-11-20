## Configuration pour le dev HTTPS

Générez un certificat auto-signé pour le développement local :

`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./certs/local-key.pem -out ./certs/local-cert.pem`

Créez un fichier acme.json vide :

`touch acme.json`

`chmod 600 acme.json`

Créer un network pour traefik :

`docker network create traefiknetwork`

Hacher un mot de passe :

`htpasswd -nB user1`

Lancer le conteneur :

`docker compose -f compose.XXX.yaml up -d`
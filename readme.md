# 1
Creamos llave en el servidor
ssh-keygen -t ed25519 -C "GitHub Deploy Key"

# 2
Copiamos la llave al github

# 3
cd <directorio>
cp .env.sample .env

# 4
Edito .env


docker-compose -f docker-compose.deploy.yml run --rm certbot /opt/certify-init.sh



docker-compose -f docker-compose.deploy.yml down
docker-compose -f docker-compose.deploy.yml up

To renew, we can run:

docker-compose -f docker-compose.deploy.yml run --rm certbot sh -c "certbot renew"s

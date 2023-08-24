docker-compose -f docker-compose.deploy.yml run --rm certbot /opt/certify-init.sh



docker-compose -f docker-compose.deploy.yml down
docker-compose -f docker-compose.deploy.yml up

To renew, we can run:

docker-compose -f docker-compose.deploy.yml run --rm certbot sh -c "certbot renew"
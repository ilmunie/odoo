# odoo
Docker odoo repo. Multiple Versions


# Usage
## Odoo Version
Configure the wanted version in the docker-compose.yml

## Run Odoo
docker compose up
docker compose up -d

## Restore database from a sql.gz
gunzip -c ../backup.sql.gz|docker-compose exec -T db psql -U odoo -d [dbname]

## Instructions to use git submodules
git submodule update --init --recursive
git submodule add -b main https://github.com/ilmunie/combo_product.git addons/combo_product
add submodules path to config/odoo.conf
# LOGIN AWS VAULT (PRIYAAKASH) iam USER NAME
aws-vault exec priyaakash --duration=8h



# TO INITLIZATIONS TERRAFORM PROJECT
docker compose run --rm terraform -chdir=setup init

# TO CHECK FILE FORMAT
docker compose run --rm terraform -chdir=setup fmt


# TO CHECK FILE CODE
docker compose run --rm terraform -chdir=setup validate


# TO CREATE RESOURCES
docker compose run --rm terraform -chdir=setup apply


# TO PRINT SENSITIVE OUTPUTS
docker compose run --rm terraform -chdir=setup output cd_user_access_key_secret

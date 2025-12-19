stage-5-docker
How to run it
1. Create a .env file with fields
#####nginx-config#####
NGINX_HOST=#your domain or puplic ip
UPSTREAM_HOST=myswapi #by default
UPSTREAM_PORT=3000 #by defaul



#####myswapi-config#####
#db config
DB_TYPE=postgres #the database image is based on postgresql, better don`t change it
DB_HOST=myswapi-db #by default
DB_PORT=5432 #by defaul
DB_USERNAME=postgres #by default
DB_PASSWORD=#make password for db user
DB_NAME=starwars #by default

#s3 config
S3_REGION=#your AWS regin
S3_BUCKET_NAME=#your bucket name
S3_ACCESS_KEY=#your access key
S3_SECRET_ACCESS_KEY=#youe secret access key

#jwt
JWT_SECRET=#secret from JWT

#####postgres-config#####
POSTGRES_PASSWORD=#password that will be created for the database user when creating the container, use the same value here and in DB_PASSWORD

2. docker compose up -d


!!!nginx listens on port 80, you can change this to ./templates/default.conf.template

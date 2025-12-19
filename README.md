# stage-5-docker

## How to run

### 1. Create `.env` file

Create a `.env` file in the project root and fill in the following fields.

----------------------------

NGINX CONFIG

NGINX_HOST=your_domain_or_public_ip
UPSTREAM_HOST=myswapi #better don`t change
UPSTREAM_PORT=3000 #better don`t change

----------------------------

MYSWAPI CONFIG

DATABASE

DB_TYPE=postgres #better don`t change
DB_HOST=myswapi-db #better don`t change
DB_PORT=5432 #better don`t change
DB_USERNAME=postgres #better don`t change
DB_PASSWORD=your_db_password
DB_NAME=starwars #better don`t change

----------------------------

S3 (AWS)

S3_REGION=your_aws_region
S3_BUCKET_NAME=your_bucket_name
S3_ACCESS_KEY=your_access_key
S3_SECRET_ACCESS_KEY=your_secret_access_key

----------------------------

JWT

JWT_SECRET=your_jwt_secret

----------------------------

POSTGRES CONFIG

POSTGRES_PASSWORD=your_db_password

IMPORTANT:
POSTGRES_PASSWORD must be the same as DB_PASSWORD

----------------------------

### 2. Run containers

docker compose up -d

----------------------------

NOTES

- Nginx listens on port 80 by default
- You can change the port in:
  ./templates/default.conf.template
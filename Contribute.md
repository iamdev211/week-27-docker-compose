## Manual Installation
 - Install node js locally()
 - Clone the repo
 - Install dependencies (npm install)
 - Start the DB locally
    - docker run -e POSTGRES_PASSWORD=1234 -d -p 5432:5432 postgres
    - Go to neon.tech & get yourself a new DB
 - Change the .env files and update your DB credentials
 - Add build("tsc -b") and start("node dist/index.js") scripts to package.json
 - npx prisma migrate
 - npx prisma generate
 - npm run build
 - npm run start

## Docker Installation
 - Install docker
 - Create a network
   - docker network create user_project
 - Start postgres
   - docker run --network user_project --name postgres -e POSTGRES_PASSWORD=1234 -d -p 5432:5432 postgres
 - Build the image - `docker build --network=host -t user-project .`
 - Start the image - `docker run -e DATABASE_URL=postgresql://postgres:1234@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker Compose Installation
 - Install docker, docker-compose
 - Run `docker-compose up`


SSH - git@github.com:iamdev211/week-27-docker-compose.git
HTTPS - https://github.com/iamdev211/week-27-docker-compose.git
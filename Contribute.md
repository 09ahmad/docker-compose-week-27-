## Manual Installation 
- Install nodejs locally ()
- Clone the repo 
- Insatll dependepcies (npm install)
- Start the Db locally ()
  - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
  - Go to neon.tech and get yourselg a new DB
- Change the .env file and update your DB credentials
-npx prisma migrate dev
-npx prisma generate
-npm run build 
-npm run start

## Docker installation 
- Install docker
- Create a network - docker create network user_project
- Start postgres
   - docker run --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
- Build the image - `docker build --network=host -t user-project .`
- Start the image -  `docker run -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker Compose Installation steps
- Install docker, docker compose
- Run `docker-compose up`
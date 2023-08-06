# CaveLMS -  Adullam Theological Seminar Monorepo

CaveLMS - Adullam Theological Seminary Monorepo is a software repository that contains multiple projects related to an e-learning platform. The repository includes a web application project, a services project, and a website project, all written using different programming languages and frameworks. The web app project is built using TypeScript and SvelteKit, while the services project is written in Golang, and the website project is again built using TypeScript and SvelteKit. These different projects work together to create a comprehensive e-learning platform for Adullam Theological School.

## How run the project

```bash
# First, clone the repository 
git clone https://github.com/Adullam-Cave-LMS/cavelms.git

# navigate to the project directory
cd cavelms
```

#### The next step is to set up the MongoDB database using Docker. If you don't have Docker installed on your system, you can download it from the official website: https://www.docker.com/get-started.


```bash
# run the following command to start the MongoDB container
docker run --name mongodb -p 27017:27017 -d mongo:latest
```

> This command will start a MongoDB container named "mongodb" and map the container port 27017 to the host port 27017.


```bash
# navigate to the services directory 
cd services

# Copy the .env.example file to .env
cp .env.example .env
```

> Update the MONGODB_URI variable in the .env file with the MongoDB URI. The default MongoDB URI is mongodb://localhost:27017/cavelms, which maps to the MongoDB container we just started.

```bash
npm install
npm start
```


```bash
# terminal window and navigate to the root project directory 
cd ../
```



```bash
# Navigate to the website directory
cd website
```

```bash
# Copy the .env.example file to .env
cp .env.example .env
```


```bash
# Copy the .env.example file to .env
npm install
npm run dev
```

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

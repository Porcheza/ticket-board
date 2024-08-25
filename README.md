# Quick Starter Instruction

## Prerequisite

- Docker Desktop (https://www.docker.com/products/docker-desktop)
- Database Client (Recommended: https://dbeaver.io/download/)
- Code Editor (Recommended: https://code.visualstudio.com/download)

## Setup

### Step1: Pull all submodules

```
git submodule update --init
```

Note: After the git submodule is done, you might see the latest commit was a SHA commit number. Please change it to the main branch before continue to the next step.

### Step2: Run database

Run postgres database service container in the root directory of the workspace using belows command.

```
docker-compose up postgres
```

Open your database client and use database configuration as follow:

- host=localhost
- port=5432
- username=devuser
- password=P@ssw0rd123

### Step3: Run docker-compose to start backend

Run backend service container to start install dependencies and run all backend services. The backend services include: backend.

```
docker-compose up backend
```

After the service start, you can access the API document http://localhost:3002/doc

### Step4: Run docker-compose to start frontend

Run frontend service container to start install dependencies and run all frontend services. The frontend services include: frontend

```
docker-compose up frontend
```

After the service start, you can access the web application http://localhost:8082

### Step5: Explore the project

At this step, you will probably run all of the project environment.
More information about the stack that we use is listed belows:

- NestJS (Backend):https://nestjs.com/
- Pinia (Frontend): https://pinia.vuejs.org/
- VuexORM (Frontend): https://vuex-orm.org/
- VueRouter (Frontend): https://router.vuejs.org/
- Bootstrap (Frontend): https://getbootstrap.com/
- Jest (Testing): https://jestjs.io/docs/getting-started
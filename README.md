# Judo React Assignment

Welcome and thank you for taking the time to complete the Judo take-home assignment.

You will have 4 days to complete the assignment. Once you have completed your solution, please reply with a link to a github repository.

The goal of this assignment is to build the Judo login page with public and protected routes.

## Prerequisite

-   Docker (https://docs.docker.com/get-docker)
-   Yarn

## Running the stack

```
docker-compose up
```

You can now access the frontend via http://localhost:3000 and the backend via http://localhost:8080 (explore the GraphQL API http://localhost:8080/graphql)

# Requirements

-   build reusable components based on the design
-   build the `/login` page described in the [design](./design/login-measurments.png)
-   A simple page `/products` that lists the products with a button to logout. There are no design requirments here
-   A Home page `/` with a simple button to go to `/login`
-   Add protected and public routes:
    -   `/`: public anyone can view this page
    -   `/login`: if a user is already signed in redirect to `/products`
    -   `/products`: a user must be signed in to view
-   You can use either the Rest or the GraphQL API
-   When a session expires it must be refreshed before retrying the call again. To automatically expire sessions you can perform the following: `docker-compose run --rm postgres psql -U postgres dev -c "UPDATE sessions SET expires_at = now()"`

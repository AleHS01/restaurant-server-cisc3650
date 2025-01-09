# Restaurant Server (CISC 3650 Assignment)

This is a simple server for a restaurant application, implementing basic CRUD operations.   

## Tech Stack
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
## Prerequisites

# Mac OS
### For this only install **brew**, Install anything below **brew**, through **brew**.
- [brew](https://brew.sh/)
- [node](https://nodejs.org/en)
  
## Install brew

```bash

bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```


## Install node

```bash
brew install node
```
## Check npm Version
```bash
npm -v
```

---
## Setup
- Clone the repository:

```bash
git clone https://github.com/AleHS01/restaurant-server-cisc3650.git
cd restaurant-server-cisc3650
```
- Install dependecies:
```bash
npm install
```
---
## Run the server

```bash
npm run start
```
---
- Local Backend URL:
```bash
http://localhost:8080
```
---
## Features:
Users can perform the following operations:
- Retrieve all restaurants.
- Retrieve details of a specific restaurant.
- Retrieve all favorite restaurants.
- Add a restaurant to favorites.
- Remove a restaurant from favorites.
---
## Data Storage Approach
Instead of using a database, this application utilizes JSON files for data storage. Restaurant data is stored in a file named `restaurant.json`, while favorite restaurant data is managed in `favorite.json`. Favorite data is written to a `favorite.json` file using a custom function:

```javascript
function saveFavoritesData() {
  fs.writeFile(
    "./favorites.json",
    JSON.stringify(favorites, null, 2),
    (err) => {
      if (err) {
        console.error("Error saving data:", err);
      }
    }
  );
}
```
## Deployment

This project is deployed using Vercel, though it is not currently active. You can deploy your own instance by following these steps:
- Visit Vercel and create an account.
- Link your GitHub repository to Vercel.
- Set up deployment settings and deploy the project.


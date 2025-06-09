# PET STORE V2 User API Postman Tests

This repo contains automated Postman tests for the User API ON https://petstore.swagger.io/#. All postman variables are attached to the collection. Postman published collection is at- https://documenter.getpostman.com/view/8738160/2sB2x3ntFH 

## 🔧 Prerequisites

- [Postman](https://www.postman.com/downloads/) installed

## 📦 Files

- `user-api-tests.postman_collection.json` — Main collection

## 🚀 How to Run the Tests

1. Open Postman.
2. Import both the collection(Variables already attached).
3. Run the collection via **Collection Runner** or **Newman**:

   
## Observations

1. The api is a test api, as a result, some of the test case expections and edge cases checks were not met. 
2. For example, updating a user, user details do not change. And the test script checks that and so it validly fails.
3. When a new user is created, the username is removed after a period, so please run sequentially, as some of the later endpoints and tests are dependent on previous endpoints.

### Option A: Postman Collection Runner

- Open the collection.
- Click "Run".
- A right side panel comes up. Click **Advanced Setting** and uncheck **Stop run if an error occurs** - **This is important because some of the edge cases fails as they are not well handled in the api, but should be check for** 
- and click **Run User Endpoints**.

![image](https://github.com/user-attachments/assets/e1937c9e-47cb-4cfe-8d65-b7c79a1fc77a)
![image](https://github.com/user-attachments/assets/5051ee50-fa70-4e1d-ac88-e0f334fdf448)

### Option B: Run via Newman (CLI)

```bash
npm install -g newman
newman run user-api-tests.postman_collection.json


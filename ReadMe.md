# PET STORE V2 User API Postman Tests

This repo contains automated Postman tests for the User API ON https://petstore.swagger.io/#. All postman variables are attached to the collection

## 🔧 Prerequisites

- [Postman](https://www.postman.com/downloads/) installed

## 📦 Files

- `user-api-tests.postman_collection.json` — Main collection

## 🚀 How to Run the Tests

1. Open Postman.
2. Import both the collection(Variabled already attached).
3. Run the collection via **Collection Runner** or **Newman**:

### Option A: Postman Collection Runner

- Open the collection.
- Click "Run".
- A right side panel comes up. Click **Advanced Setting** and uncheck **Stop run if an error occurs** - **This is important because some of the edge cases fails as they are not well handled in the api, but should be check for**
- and click **Start Run**.

### Option B: Run via Newman (CLI)

```bash
npm install -g newman
newman run user-api-tests.postman_collection.json

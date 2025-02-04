# 🚀 GoRest API Testing with Postman  

## 📌 Overview  
This repository contains a Postman collection for testing the **GoRest API**. It includes requests for performing **CRUD operations** on users, posts, and comments.  

## 📂 Files in This Repo  
- **`gorest.postman_collection.json`** → API request collection.  
- **`New Environment.postman_environment.json`** → Environment variables (if applicable).  

## 🛠 How to Use  

### 1️⃣ Import Collection & Environment in Postman  
1. Open **Postman**  
2. Click **Import**  
3. Select `gorest.postman_collection.json`  
4. *(Optional)* Import `New Environment.postman_environment.json`  

### 2️⃣ Run the Collection in Postman  
1. Open the **GoRest API Collection**  
2. Set the environment (if applicable)  
3. Click **Run Collection** to execute the API tests  

### 3️⃣ Run the Collection via Newman (Command Line) *(Optional)*  
If you have [Newman](https://www.npmjs.com/package/newman) installed, run:  
```sh
newman run gorest.postman_collection.json -e New Environment.postman_environment.json
name: Run Postman Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v3
        
      - name: Install Newman
        run: npm install -g newman
        
      - name: Run Postman Collection
        run: newman run gorest.postman_collection.json -e New\ Environment.postman_environment.json

---

### ✅ **Next Steps**  
1. **Copy & Paste** this into your `README.md`  
2. **Commit & Push** to your GitHub repo  
3. *(Optional)* Set up GitHub Actions for automation  

Let me know if you need further improvements! 🚀

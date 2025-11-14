# MongoDB Practice Scripts

This repository contains **MongoDB scripts** for practicing basic database operations such as setup, reading, updating, and more. Each script is organized and numbered to help run them in sequence.

---

## 📁 File Structure

mongodb-scripts/
├── 01_setup.mongodb.js # MongoDB setup: create database & collections
├── 02_reading.mongodb.js # MongoDB read queries: find, filter, and query data
├── 03_update.mongodb.js # MongoDB update queries: updateOne, updateMany, $push, $inc
└── README.md # Project overview and instructions

---

## 🔹 Scripts Overview

### 1. `01_setup.mongodb.js`
- Sets up the database (`ecommerce`) and collections (`products`).  
- Inserts sample documents for testing.  
- Example operation: `db.products.insertOne(...)`.  

### 2. `02_reading.mongodb.js`
- Contains **reading/query operations**.  
- Examples include:  
  - `db.products.find()` → Get all products  
  - `db.products.find({ category: "Electronics" })` → Filter by category  
  - `db.products.find({ price: { $gte: 500 } })` → Filter by price range  

### 3. `03_update.mongodb.js`
- Contains **update operations**.  
- Examples include:  
  - Update the price of a product: `$set`  
  - Increment stock for multiple products: `$inc`  
  - Add a tag to an array field: `$push`  

---

## ⚡ How to Run

1. **Open `mongosh`** or connect via a MongoDB client.  
2. **Select the database** (if not using a Node.js script):  
   ```js
   use ecommerce
3. **Run scripts in order:**

   load("01_setup.mongodb.js")
   load("02_reading.mongodb.js")
   load("03_update.mongodb.js")


4. **Verify changes using:**

   db.products.find().pretty()

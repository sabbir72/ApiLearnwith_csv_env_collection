# 🧪 Restful Booker API Test Report

This repository contains Postman collections and environment files for automated API testing of the **Restful Booker** API using **Newman** and the **HTMLExtra Reporter**.

🔗 **Full Report**: [1 time Iterations  View HTML Report](https://sabbir72.github.io/ApiLearnwith_csv_env_collection/report.html)  1 time Iterations 

## 📊 Test Report Summary

📅 **Test Date**: January 26, 2025  
🔗 **Full Report**: [View HTML Report](https://sabbir72.github.io/ApiLearnwith_csv_env_collection/reporthtmlextra.html)  
🧪 **Test Tool**: Newman with htmlextra reporter

### ✅ Overall Test Stats

| Metric                 | Value        |
|------------------------|--------------|
| Total Iterations       | 5            |
| Total Requests         | 50           |
| Total Assertions       | 95           |
| Total Failures         | 15           |
| Average Response Time  | 356 ms       |
| Total Test Duration    | 22.7 seconds |
| Data Received          | 264.11 KB    |

---

### ❌ Key Failures

#### 1. **Response Time Threshold Breach**
- **Test**: `Response time is less than 200ms`
- **Failures**: 5 times (1 per iteration)
- **Max Response Time**: 1095 ms
- **Cause**: Slow API response, needs performance optimization.

#### 2. **Invalid Response for DELETE**
- **Test**: `Self Delete`
- **Expected**: JSON with status `Delete`
- **Actual**: Non-JSON response with status `Created`
- **Errors**:
  - `Unexpected token 'C' at 1:1` (JSON parsing issue)
  - Indicates API is returning plain text instead of JSON

---

## 🛠 Recommendations

- Optimize API endpoints to improve performance and reduce latency.
- Fix DELETE endpoint to return proper JSON format and appropriate response code (e.g., `204 No Content`).
- Align test expectations with actual API behavior or update API responses to meet REST standards.

---

## 📁 Files Included

- `Restfull_Booker.postman_collection.json` – Postman test collection
- `Book_Environment.postman_environment.json` – Environment variables
- `reporthtmlextra.html` – Visual HTML test report (auto-generated)

---

## 🚀 Run Tests Locally

To execute the collection 10 times and generate separate reports:

```bash
# 🧪 Restful Booker API Test Report

This repository contains Postman collections and environment files for automated API testing of the **Restful Booker** API using **Newman** and the **HTMLExtra Reporter**.

## 📊 Test Report Summary

📅 **Test Date**: January 26, 2025  
🔗 **Full Report**: [View HTML Report](https://sabbir72.github.io/ApiLearnwith_csv_env_collection/reporthtmlextra.html)  
🧪 **Test Tool**: Newman with htmlextra reporter

### ✅ Overall Test Stats

| Metric                 | Value        |
|------------------------|--------------|
| Total Iterations       | 5            |
| Total Requests         | 50           |
| Total Assertions       | 95           |
| Total Failures         | 15           |
| Average Response Time  | 356 ms       |
| Total Test Duration    | 22.7 seconds |
| Data Received          | 264.11 KB    |

---

### ❌ Key Failures

#### 1. **Response Time Threshold Breach**
- **Test**: `Response time is less than 200ms`
- **Failures**: 5 times (1 per iteration)
- **Max Response Time**: 1095 ms
- **Cause**: Slow API response, needs performance optimization.

#### 2. **Invalid Response for DELETE**
- **Test**: `Self Delete`
- **Expected**: JSON with status `Delete`
- **Actual**: Non-JSON response with status `Created`
- **Errors**:
  - `Unexpected token 'C' at 1:1` (JSON parsing issue)
  - Indicates API is returning plain text instead of JSON

---

## 🛠 Recommendations

- Optimize API endpoints to improve performance and reduce latency.
- Fix DELETE endpoint to return proper JSON format and appropriate response code (e.g., `204 No Content`).
- Align test expectations with actual API behavior or update API responses to meet REST standards.

---

## 📁 Files Included

- `Restfull_Booker.postman_collection.json` – Postman test collection
- `Book_Environment.postman_environment.json` – Environment variables
- `reporthtmlextra.html` – Visual HTML test report (auto-generated)

---

## 🚀 Run Tests Locally

To execute the collection 10 times and generate separate reports:

```bash
newman run Restfull_Booker.postman_collection.json \
  -e Book_Environment.postman_environment.json \
  -r htmlextra --reporter-htmlextra-export report.html


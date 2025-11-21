# Demonstration Guide - Quick Steps

## Pre-Demo Setup

```bash
# 1. Navigate to project directory
cd /Users/garvit/Desktop/Devops-Project

# 2. Ensure Docker is running
docker ps

# 3. Build and start the application
docker-compose up -d

# 4. Verify it's running
curl http://localhost:5000/health
```

---

## Demo Steps

### Step 1: Start Application (30 seconds)

```bash
# If not already running:
docker-compose up -d

# Check status
docker ps
```

**Say:** "I'll start the Flask application using Docker. It runs on port 5000."

---

### Step 2: Show Application UI (1 minute)

1. Open browser: `http://localhost:5000`
2. Show:
   - Sidebar navigation
   - Empty state (or existing orders)
   - Modern card-based design

**Say:** "This is the Order Management System with a clean, modern interface."

---

### Step 3: Create Test Orders (1 minute)

1. Click "New Order"
2. Fill form:
   - User ID: `USER001`
   - Product Code: `PROD123`
   - Quantity: `5`
   - Order Date: Today
   - Store Code: `STORE01`
3. Click "Create Order"
4. Create 2-3 more orders with different data

**Say:** "I'm creating orders. All data is stored in browser localStorage and persists across refreshes."

---

### Step 4: Show Features (1 minute)

- View orders list
- Show pagination (if > 25 orders)
- Show sorting (newest first)
- Show order count in sidebar
- Refresh page to show persistence

**Say:** "The application includes pagination, sorting, and data persistence."

---

### Step 5: Test Health Endpoint (30 seconds)

```bash
curl http://localhost:5000/health
```

**Expected Output:**
```json
{"status":"healthy","service":"order-management-app","version":"1.0.0"}
```

**Say:** "This health check endpoint is essential for monitoring and CI/CD pipelines."

---

### Step 6: Run Automated Tests (1 minute)

```bash
# Activate virtual environment first
source venv/bin/activate

# Run tests
pytest -v

```

**Say:** "I've written comprehensive tests. All 7 tests pass, ensuring the application works correctly."

---

### Step 7: Show Code Quality Checks (1 minute)

```bash
# Run linting
make lint
```

**Say:** "We use automated code quality tools: Flake8 for linting, Pylint for analysis, and Black for formatting."

---

### Step 8: Show Docker Containerization (1 minute)

```bash
# Show running container
docker ps

# Show Docker logs
docker-compose logs --tail=10
```

**Say:** "The application is containerized using Docker. This ensures it runs consistently across different environments."

---

### Step 9: Explain CI/CD Pipeline (1 minute)

**Say:** "The project includes a CI/CD pipeline that runs automatically on every code push:
1. Code quality checks (Black, Flake8, Pylint)
2. Automated testing (pytest with coverage)
3. Security scanning (Safety, Bandit)
4. Docker build and test
5. Health check verification"

---

## Quick Commands Reference

```bash
# Start application
docker-compose up -d

# Stop application
docker-compose down

# Run tests
pytest -v

# Run linting
make lint

# Format code
make format

# Check health
curl http://localhost:5000/health
```

---


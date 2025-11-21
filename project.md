# Order Management System - Project Overview

## What This Project Does

This is a **modern Order Management System** built as a **DevOps showcase project**. It demonstrates industry-standard DevOps practices including containerization, automated testing, CI/CD pipelines, and code quality checks.

## Core Application

### Functionality
- **Order Management**: Create, view, and manage customer orders
- **User Interface**: Modern, responsive web interface with sidebar navigation
- **Data Storage**: Client-side storage using browser localStorage (no backend database required)
- **Features**:
  - Create new orders with user ID, product code, quantity, order date, and store code
  - View all orders in a paginated list (25 orders per page)
  - Automatic sorting by date (newest first)
  - Order count display in sidebar
  - Data persistence across page refreshes

### Technology Stack
- **Backend**: Python 3.11 + Flask 3.x
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Storage**: Browser localStorage (client-side)
- **Architecture**: Minimal backend (serves static files), client-side data management

## DevOps Features

### 1. Containerization
- **Docker**: Multi-stage Dockerfile for optimized container builds
- **Docker Compose**: Local development and testing setup
- **Health Checks**: Built-in container health monitoring

### 2. Automated Testing
- **Unit Tests**: Test Flask routes, health endpoints, error handling
- **Integration Tests**: End-to-end application testing
- **Framework**: Pytest with coverage reporting
- **Test Coverage**: 7 comprehensive tests covering all functionality

### 3. Code Quality
- **Black**: Automated code formatting
- **Flake8**: Code linting and style checking
- **Pylint**: Advanced code analysis
- **Configuration**: Custom rules in `.flake8` and `pytest.ini`

### 4. CI/CD Pipeline
- **GitHub Actions**: Automated pipeline on every push/PR
- **Stages**: Code quality → Testing → Security → Docker build → Health check
- **Automation**: Zero manual steps, fully automated workflow

### 5. Security
- **Safety**: Dependency vulnerability scanning
- **Bandit**: Security linting for Python code
- **Best Practices**: Container security, non-root user, minimal base images

### 6. Infrastructure as Code
- **Dockerfile**: Defines container build process
- **docker-compose.yml**: Orchestrates services
- **Makefile**: Standardizes common DevOps tasks
- **Version Controlled**: All infrastructure defined in code

### 7. Monitoring & Health
- **Health Endpoint**: `/health` returns service status in JSON
- **Container Health Checks**: Automatic container monitoring
- **Status Reporting**: Version, service name, and health status

## Project Structure

```
Devops-Project/
├── app.py                 # Flask application (minimal backend)
├── requirements.txt       # Production dependencies
├── requirements-dev.txt   # Development/testing tools
├── Dockerfile            # Container image definition
├── docker-compose.yml    # Local development setup
├── Makefile             # Automation commands
├── pytest.ini           # Test configuration
├── .flake8              # Linting configuration
├── .dockerignore        # Docker build exclusions
├── templates/           # HTML templates
│   └── orders.html      # Main application page
├── static/              # Static assets
│   ├── script.js       # Client-side JavaScript
│   └── style.css       # Styling
└── tests/               # Test suite
    ├── test_app.py     # Unit tests
    └── test_integration.py  # Integration tests
```

## Key Features

### Application Features
✅ Modern, card-based UI design  
✅ Sidebar navigation  
✅ Pagination (25 orders per page)  
✅ Automatic sorting (newest first)  
✅ Client-side data persistence  
✅ Responsive design  

### DevOps Features
✅ Docker containerization  
✅ Automated testing (pytest)  
✅ Code quality checks (Black, Flake8, Pylint)  
✅ CI/CD pipeline (GitHub Actions)  
✅ Security scanning (Safety, Bandit)  
✅ Health monitoring  
✅ Infrastructure as Code  
✅ Makefile automation  

## Use Cases

1. **Learning DevOps**: Demonstrates real-world DevOps practices
2. **Portfolio Project**: Showcases containerization, testing, and automation skills
3. **CI/CD Practice**: Complete pipeline implementation
4. **Containerization Demo**: Docker best practices
5. **Testing Example**: Comprehensive test suite


## Learning Outcomes

This project demonstrates:
- Setting up CI/CD pipelines with GitHub Actions
- Containerizing applications with Docker
- Writing and running automated tests
- Implementing code quality checks
- Security best practices
- Infrastructure as Code concepts
- Modern DevOps workflows

---

**Note**: This project uses 100% free and open-source tools, making it accessible for learning and portfolio purposes.


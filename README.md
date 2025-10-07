# 🎛️ Grafana Production Dashboards

This repository contains all production Grafana dashboards for monitoring our infrastructure and applications.

## 📊 Dashboard Categories

### 🐘 Database Monitoring
- **`postgresql-production-monitor.json`** - ⭐ **MAIN POSTGRESQL DASHBOARD** 
  - User-friendly production database monitor
  - Shows connection status, performance metrics, vacuum needs
  - Highlights missing indexes and slow queries
  - **Recently Updated** with working queries ✅

### 🌺 Queue Monitoring (Celery/Flower)
- **`flower_celery_monitoring.json`** - Main Celery monitoring dashboard (25K)
- **`flower_overview.json`** - Flower overview dashboard (8K)
- **`celery_tasks_dashboard.json`** - Celery tasks specific dashboard

### 💰 Credit & Usage Monitoring  
- **`credit_used_by_companies_with_pages.json`** - Credit usage with pagination
- **`credit_used_by_companies.json`** - Basic credit usage by company
- **`credit_nutzung_pro_kunde.json`** - Credit usage per customer (German)
- **`credit_used_per_method.json`** - Credit usage by method

### 🏢 Business Intelligence
- **`docbits_business_intelligence_dashboard.json`** - Main BI dashboard
- **`docbits_api_it_operations_dashboard.json`** - IT operations dashboard  
- **`docbits_usage_overview.json`** - Usage overview
- **`docbits_documents_overview.json`** - Documents overview

### 🔧 Infrastructure & System Monitoring
- **`click_house.json`** - ClickHouse database monitoring
- **`redis.json`** - Redis monitoring dashboard
- **`redis_streaming.json`** - Redis streaming specific metrics
- **`egress-dashboard.json`** - Network egress monitoring
- **`slow_reuests_by_service.json`** - Slow requests monitoring

### 👥 Customer & Organization Monitoring
- **`Customer-Info.json`** - Customer information dashboard
- **`customer_data_microservice_dashboard.json`** - Customer data microservice
- **`fehlgeschlagene_email_imports_pro_organisation.json`** - Failed email imports

### 🧪 Testing & Development
- **`test_coverage_rates_on_services.json`** - Test coverage rates
- **`keda_sandbox.json`** - KEDA autoscaling sandbox
- **`subscription.json`** - Subscription monitoring

### 📋 Operations
- **`doc-operator-dashboard.json`** - Document operator dashboard  
- **`docoperator-system-dashboard.json`** - Doc operator system dashboard
- **`docbits_celery_usage.json`** - Celery usage metrics
- **`docbits.json`** - Main Docbits dashboard (260K - comprehensive)

## 📁 Directory Structure

### `/Old/` - Legacy Dashboards
Contains older versions and deprecated dashboards:
- `postgres_overview.json` (37K) - Old PostgreSQL dashboard
- `postgresql_infrastructure.json` (104K) - Old PostgreSQL infrastructure
- `flower_monitoring.json` (13K) - Old Flower monitoring
- `docbits_main.json` (560K) - Legacy main dashboard
- `observability.json` - Old observability dashboard
- `polydocs_dashboard.json` - Old Polydocs dashboard

### `/Automated_Tests/` - Test Dashboards
Contains dashboards for automated testing monitoring.

### `/Linkerd/` - Service Mesh Monitoring  
Contains Linkerd service mesh related dashboards.

### `/Test/` - Development/Test Dashboards
Contains test and development dashboards.

## 🧹 Recent Cleanup (October 2025)
- ✅ Added `.json` extension to all dashboard files
- ✅ Removed duplicate dashboards (kept newest/largest versions)
- ✅ **Added working PostgreSQL production monitor dashboard**
- ✅ Organized legacy dashboards into `/Old/` directory
- ✅ Fixed file naming conventions

## 🚀 Usage

### Import a Dashboard
1. Go to Grafana → **"+"** → **"Import"**
2. Upload the `.json` file
3. Select appropriate datasource (usually "API PROD" for PostgreSQL)
4. Click **"Import"**

### PostgreSQL Dashboard
The **`postgresql-production-monitor.json`** dashboard provides:
- 🟢 Database connection status
- 📊 Active connections monitoring  
- 🧹 Tables needing VACUUM
- 🔍 Missing indexes detection
- ⚡ Performance metrics with color-coded alerts

## 📝 Notes
- All dashboards are in JSON format for easy version control
- Use descriptive commit messages when updating dashboards  
- Test dashboards in staging before deploying to production
- Keep the `/Old/` directory for reference but avoid importing those dashboards

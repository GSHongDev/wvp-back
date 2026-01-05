# Backend Development Log

## Version History

### [2026-01-04] Initial Setup

#### Project Initialization
- Initialize project structure with all modules
- Configure Maven project dependencies
- Add all module code (ruoyi-admin, ruoyi-common, ruoyi-framework, ruoyi-generator, ruoyi-isup, ruoyi-onvif, ruoyi-quartz, ruoyi-rtsp, ruoyi-system, ruoyi-wvp)
- Set up Git branch structure (main, test)

#### Configuration
- Configure UTF-8 encoding in pom.xml
  - `project.build.sourceEncoding=UTF-8`
  - `project.reporting.outputEncoding=UTF-8`
- Configure Tomcat URI encoding to UTF-8 in application.yml

#### Database
- Add SQL initialization script: `sql/ry-wvp-v1.3.0.sql`
  - Database schema for GB/T 28181-2016 streaming media platform
  - Includes all required tables for WVP functionality
  - **Important**: Execute this SQL file before starting the backend service

#### Git Workflow
- Create `main` branch for production environment
- Create `test` branch for integration testing
- All commits follow conventional commit format with English messages

#### Notes
- **Before starting the backend**: Make sure to execute the SQL file `sql/ry-wvp-v1.3.0.sql` in your database
- The backend service requires a MySQL database to be configured
- Default port: 8080 (configurable in application.yml)

### [2026-01-04] [23:41] Database Configuration Update
- Update database connection configuration for test environment
- Configure test database credentials in application-druid.yml
- Note: This is a test database configuration, no security risk

### [2026-01-04] [23:49] Deployment and Testing
- Complete backend deployment and configuration
- Successfully start backend service
- Database connection verified and working
- All modules initialized correctly
- **Test Status**: ✅ Passed - Backend service running normally

### [2026-01-05] [15:00] ZLM Service Integration
- Integrate ZLMediaKit service with backend
- Add ZLM configuration file: `config/ZLMediakit_config.ini`
- Synchronize ZLM config with Ubuntu server configuration
- Update application.yml with ZLM service connection settings
- Successfully establish connection between backend and ZLM service
- **Test Status**: ✅ Passed - ZLM service connected and running normally

#### Deployment Environment
- **Ubuntu Server**: 
  - System: Linux 6.14.0-37-generic (Ubuntu 24.04)
  - IP: 192.168.0.142
  - ZLM Service: Running on Ubuntu
- **Windows Development**:
  - System: Windows 11
  - IP: 192.168.0.138
  - Backend Service: Running on Windows

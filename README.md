# Backend Development Log

## Version History

### [2025-01-XX] Initial Setup

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

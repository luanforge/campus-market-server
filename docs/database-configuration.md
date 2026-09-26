# Database configuration

The application requires database connection settings from the environment. It does not provide defaults for these values:

- `DB_URL`: JDBC URL for the MySQL database
- `DB_USERNAME`: database account name
- `DB_PASSWORD`: database account password

For local development, export the values in your shell before starting the application. For example:

```sh
export DB_URL='jdbc:mysql://localhost:3306/campus_market?useUnicode=true&characterEncoding=utf-8&useSSL=false&serverTimezone=Asia/Shanghai&allowPublicKeyRetrieval=true'
export DB_USERNAME='campus_market_app'
export DB_PASSWORD='<your-local-database-password>'
./mvnw spring-boot:run
```

Use a dedicated, least-privilege database account. Do not commit credentials or local environment files. Configure production values through the deployment platform's secret manager, and restrict database network access to trusted application hosts.

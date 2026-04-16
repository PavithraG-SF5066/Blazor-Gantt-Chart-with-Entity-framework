# Blazor Gantt Chart with Entity framework

This repository demonstrates how to integrate a Blazor Gantt Chart with a SQL database using the Entity Framework Data Model, enabling full CRUD operations through server-side communication.

## Project overview

In the Gantt Chart, we can fetch data from the SQL database using the Entity Framework Data Model and the update the changes in CRUD action to the server by using DataManager support. To communicate with the remote data, we are using CustomAdaptor of DataManager property to call the server method.

**Key Benefits of Entity Framework Core**

- Automatic SQL generation with optimized queries
- Strongly typed models for compile-time safety
- Parameterization to mitigate SQL injection
- Migrations to version database schema changes
- LINQ queries for expressive data access

## Prerequisites

Ensure the following software and packages are installed before proceeding:

| Software/Package | Version | Purpose |
|-----------------|---------|---------|
| Visual Studio 2026 | 18.2.1 or later | Development IDE with Blazor workload |
| .NET SDK | net10.0 or compatible | Runtime and build tools |
| SQL Server | 2021 or later | Database server |
| Syncfusion.Blazor.Gantt | -v {{site.blazorversion}} | Gantt Chart and UI components |
| Syncfusion.Blazor.Themes | -v {{site.blazorversion}} | Styling for Gantt Chart components |
| Microsoft.EntityFrameworkCore | 10.0.2 | Core framework for database operations |
| Microsoft.EntityFrameworkCore.SqlServer | 10.0.2 | SQL Server provider for Entity Framework Core |

## How to run the project

1. Clone or checkout this project to a local folder on your disk.
2. Open the solution file with Visual Studio 2026.
3. Rebuild the solution to restore NuGet packages.
4. Update the database connection string in the project's configuration (for example, `appsettings.json` or the DbContext configuration) to point to your SQL Server instance.
5. Ensure the database is available and migrations (if any) are applied.
6. Run the project and open the Gantt page. Test create, update and delete operations — changes are sent to the server via the CustomAdaptor and persisted by Entity Framework.
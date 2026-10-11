# WarehouseIO

A warehouse management web app for tracking inventory, transfers between warehouses, and shipments. Users can create warehouses, manage operators, and review stock and transfer activity from a dashboard.

Built with ASP.NET MVC 5, Web API 2, Entity Framework 6, and ASP.NET Identity on .NET Framework 4.8.

## Run locally

Requires Windows, Visual Studio with the **ASP.NET and web development** workload, the .NET Framework 4.8 targeting pack, and SQL Server Express LocalDB.

1. Open `WarehouseIO.sln` in Visual Studio and restore NuGet packages.
2. Check `DefaultConnection` in `WarehouseIO/Web.config`. It uses the `MSSQLLocalDB` instance and a database file in `App_Data` by default.
3. In **Tools > NuGet Package Manager > Package Manager Console**, select `WarehouseIO` as the default project and run:

   ```powershell
   Update-Database
   ```

4. Run the `WarehouseIO` project with IIS Express. Register an account and create a warehouse to start using the dashboard.

## Project layout

- `Controllers/` and `ApiControllers/` — web pages and API endpoints.
- `Models/` and `ViewModels/` — inventory, warehouse, transfer, shipment, and account data.
- `Views/`, `Content/`, and `Scripts/` — Razor templates, styles, images, and client scripts.
- `Migrations/` — database schema history.
- `App_Start/` — routing, authentication, and bundle configuration.

These folders are inside `WarehouseIO/`.

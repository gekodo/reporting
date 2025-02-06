# reporting

## How to get started a similar solution?

```
md reporting
cd reporting
dotnet new gitignore
dotnet new sln
dotnet new install Microsoft.Build.Sql.Templates
dotnet new sqlproj -n Reporting.Database -o src\database
dotnet sln add src\database
dotnet new classlib -n Reporting.Shared -o src\shared --no-restore
dotnet sln add src\shared
dotnet new console -n Reporting.Console -o src\console --use-program-main --no-restore
dotnet sln add src\console
dotnet new webapi -n Reporting.Api -o src\api --use-program-main --no-restore
dotnet sln add src\api
dotnet new worker -n Reporting.Worker -o src\worker --use-program-main --no-restore
dotnet sln add src\worker
dotnet new razor -n Reporting.Website -o src\website --use-program-main --no-restore
dotnet sln add src\website
dotnet new xunit -n Reporting.Database.Test -o test\database --no-restore
dotnet sln add test\database
dotnet new xunit -n Reporting.Shared.Test -o test\shared --no-restore
dotnet sln add test\shared
dotnet new xunit -n Reporting.Console.Test -o test\console --no-restore
dotnet sln add test\console
dotnet new xunit -n Reporting.Api.Test -o test\api --no-restore
dotnet sln add test\api
dotnet new xunit -n Reporting.Worker.Test -o test\worker --no-restore
dotnet sln add test\worker
dotnet new xunit -n Reporting.Website.Test -o test\website --no-restore
dotnet sln add test\website
git init
git add *
git commit -m "Initial commit"
git remote add origin https://github.com/gekodo/reporting.git
git push origin main
```
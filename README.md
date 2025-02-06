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
git init
git add *
git commit -m "Initial commit"
git remote add origin https://github.com/gekodo/reporting.git
git push origin main
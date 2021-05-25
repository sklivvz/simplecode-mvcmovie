# Simple Code Workshop
## Vanilla MVCMovie to refactor

This is a vanilla MVCMovie tutorial, written following [the Microsoft walkthrough]().

### Database with docker

```bash
docker pull mcr.microsoft.com/mssql/server:2019-latest
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=Aa_12345" -p 1433:1433 --name sql-server-intelligenthack -h intelligenthack -d mcr.microsoft.com/mssql/server:2019-latest
docker exec -it sql-server-intelligenthack "bash"
/opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P Aa_12345
```
```sql
> CREATE DATABASE [MvcMovieContext-1];
> GO
> EXIT
```
```bash
exit # exit container
```

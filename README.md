<p align="center">
  <img align="center" width="280" height="280" src="./icon.jpeg"/>
</p>

<h1 align="center">WarpSQL</h1>
<hr>
Opinionated extensions to Postgres packaged as a single docker deployment. Why install 10 DBs when you can have everything at once (maybe not everything).

Certified as Indie Hacker's best friend!!!

## Test on GitPod
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/ChakshuGautam/postgres-tsdb-vector-docker)

## Current and Future Supported Extensions

- [x] [PgVector](https://github.com/pgvector/pgvector)
- [x] [TimescaleDB](https://github.com/timescale/timescaledb)
- [x] [Citus](https://www.citusdata.com/)
- [x] [PostGIS](https://postgis.net)
- [ ] [ZomboDB](https://github.com/zombodb/zombodb)
- [ ] [PLV8](https://github.com/plv8/plv8)
- [ ] [PgRepack](https://github.com/reorg/pg_repack)

Bootstrapped from [TimescaleDB](https://github.com/timescale/timescaledb-docker)

## Usage with Compose

```yaml
version: '3.6'
services:
  warpsql:
    container_name: warpsql
    image: samagragovernance/postgres:latest-pg15
    restart: always
    ports:
      - "5432:5432"
    volumes:
      - ./pgdata:/var/lib/postgresql/data
    environment:
      POSTGRES_USER: warpSQLUser
      POSTGRES_PASSWORD: warpSQLPass
```
## Contribution

Here's how you can get started:

Ensure that the CI tests pass by running them locally.

Make any necessary changes or improvements to the codebase.

Test your changes to ensure they work as expected.

Commit your changes to a new branch or forked repository.

Submit a pull request (PR) with a descriptive title and mention the issue number (#28) in the PR description to link it to the issue.

Wait for project maintainers or other contributors to review your PR. Address any feedback or suggestions they provide, if necessary.

Development with GitHub Codespaces
You can use GitHub Codespaces to develop this project in the cloud. Here's how:

Click on the "Code" button.

Select "Open with Codespaces" from the dropdown menu.

Choose the appropriate Codespace configuration.

Wait for the environment to be provisioned.

Once the environment is ready, you can start working on the project.

Install the project dependencies by running the following command in the terminal:

pip install -r requirements.txt

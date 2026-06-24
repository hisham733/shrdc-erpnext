# SHRDC ERPNext v15

Custom ERPNext v15 with all SHRDC apps pre-installed. Single-command deployment.

## Requirements

- Docker (20.10+) and Docker Compose
- 4 GB RAM minimum, 8 GB recommended

## Quick Start

```bash
curl -O https://raw.githubusercontent.com/hisham733/shrdc-erpnext/main/docker-compose.yml
docker compose up -d
```

Wait for the site to be created:

```bash
docker compose logs create-site -f
```

Once complete (5-10 min), access at **http://localhost:8080**

- **Username:** Administrator
- **Password:** admin

## Apps Included

| App | Purpose |
|---|---|
| ERPNext | Core ERP system (v15) |
| Autocount | Accounting integration |
| Short Courses | Training management |
| Frepple | Production planning |
| Barcode SHRDC | Barcode scanning |
| Telegram Integration | Telegram messaging |
| HRMS | HR management |
| Metabase Integration | Analytics integration |
| Shopify | E-commerce integration |
| SQL Accounting | SQL accounting software |
| E Invoice ERP | E-invoicing (LHDN) |

## Custom Port

If port 8080 is in use, edit `docker-compose.yml` and change:

```yaml
    ports:
      - "8081:8080"
```

Then access at http://localhost:8081.

## Stop

```bash
docker compose down
```

To remove all data:

```bash
docker compose down -v
```

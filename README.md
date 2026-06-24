# SHRDC ERPNext v15

Custom ERPNext v15 with all SHRDC apps pre-installed. Single-command deployment.

## Requirements

- Docker (20.10+) and Docker Compose
- 4 GB RAM minimum, 8 GB recommended

## Quick Start

```bash
git clone https://github.com/hisham733/shrdc-erpnext.git
cd shrdc-erpnext
docker compose -f shrdc-compose.yml up -d
```

Wait for the site to be created:

```bash
cd shrdc-erpnext
docker compose -f shrdc-compose.yml logs create-site -f
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

If port 8080 is in use, edit `shrdc-erpnext/shrdc-compose.yml` and change:

```yaml
    ports:
      - "8081:8080"
```

Then access at http://localhost:8081.

## Stop

```bash
cd shrdc-erpnext
docker compose -f shrdc-compose.yml down
```

To remove all data:

```bash
cd shrdc-erpnext
docker compose -f shrdc-compose.yml down -v
```

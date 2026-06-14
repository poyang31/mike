# mike

本專案提供兩組本機資料庫環境：

- `mike-mysql`：MySQL + phpMyAdmin
- `mike-mssql`：Microsoft SQL Server

---

## MySQL

位置：`mike/mike-mysql/docker-compose.yml`

### MySQL 連線資訊

- Host: `127.0.0.1`
- Port: `9020`
- Username: `root`
- Password: `mike`

### MySQL 管理介面

- phpMyAdmin: [phpMyAdmin](http://127.0.0.1:9021)

### MySQL 啟動

```bash
docker compose up -d
```

請在 `mike/mike-mysql/` 目錄下執行。

---

## MSSQL

位置：`mike/mike-mssql/docker-compose.yml`

### MSSQL 連線資訊

- Host: `127.0.0.1`
- Port: `9019`
- Username: `sa`
- Password: `mike`

### MSSQL 啟動

```bash
docker compose up -d
```

請在 `mike/mike-mssql/` 目錄下執行。

### 注意

SQL Server 的 `sa` 密碼必須符合複雜度要求。
如果你要直接啟動這份設定，請先把 `MSSQL_SA_PASSWORD` 改成符合規則的密碼。

---

## 停止

在對應目錄執行：

```bash
docker compose down
```

如果要連同資料卷一起刪除：

```bash
docker compose down -v
```

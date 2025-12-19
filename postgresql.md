# PostgreSQL Asosiy Buyruqlar

## Shell orqali ulanish

```bash
psql postgres
```
PostgreSQL serveriga `postgres` default database orqali ulanish.

---

## Database boshqaruvi

### Database yaratish
```sql
CREATE DATABASE <database_name>;
```
Yangi database yaratadi. `<database_name>` o'rniga kerakli nom yoziladi.

### Databasega ulanish
```sql
\c <database_name>
```
Joriy sessiyada boshqa databasega o'tish.

### Databaselar ro'yxati
```sql
\l
```
Serverdagi barcha databaselarni ko'rsatadi.

---

## Foydalanuvchi boshqaruvi

### User yaratish
```sql
CREATE USER <user_name> WITH PASSWORD '<password>';
```
Yangi foydalanuvchi yaratadi va parol belgilaydi.

### Userga huquq berish
```sql
GRANT ALL PRIVILEGES ON DATABASE <database_name> TO <user_name>;
```
Foydalanuvchiga database ustida to'liq huquqlar beradi.

---

## Foydali buyruqlar

| Buyruq | Tavsif |
|--------|--------|
| `\l` | Barcha databaselar ro'yxati |
| `\c <db>` | Databasega ulanish |
| `\dt` | Joriy databasedagi tablelar ro'yxati |
| `\du` | Barcha userlar ro'yxati |
| `\q` | psql dan chiqish |

---

## Misol

```sql
-- Database yaratish
CREATE DATABASE hrm_pro;

-- User yaratish
CREATE USER hrm_admin WITH PASSWORD 'secret123';

-- Huquq berish
GRANT ALL PRIVILEGES ON DATABASE hrm_pro TO hrm_admin;
````

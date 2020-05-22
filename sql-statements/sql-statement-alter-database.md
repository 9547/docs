---
title: ALTER DATABASE | TiDB SQL Statement Reference
summary: An overview of the usage of ALTER DATABASE for the TiDB database.
category: reference
aliases: ['/docs/v2.1/reference/sql/statements/alter-database/']
---

# ALTER DATABASE

`ALTER DATABASE` is used to specify or modify the default character set and collation of the current database. `ALTER SCHEMA` has the same effect as `ALTER DATABASE`.

## Examples

```sql
ALTER {DATABASE | SCHEMA} [db_name]
    alter_specification ...
alter_specification:
    [DEFAULT] CHARACTER SET [=] charset_name
  | [DEFAULT] COLLATE [=] collation_name
```

The `alter_specification` option specifies the `CHARACTER SET` and `COLLATE` of a specified database. Currently, TiDB only supports some character sets and collations. See [Character Set Support](/character-set-and-collation.md) for details.

## See also

* [CREATE DATABASE](/sql-statements/sql-statement-create-database.md)
* [SHOW DATABASES](/sql-statements/sql-statement-show-databases.md)
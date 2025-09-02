# Docker most used base images:

| Base Image                 | Size (approx) | Package Manager                 | Use Case(s)                                      | Notes                                                                                   |
| -------------------------- | ------------- | ------------------------------- | ------------------------------------------------ | --------------------------------------------------------------------------------------- |
| **alpine**                 | \~5 MB        | `apk`                           | Minimal, fast containers                         | Great for microservices and quick startup. Requires careful handling for missing tools. |
| **ubuntu**                 | \~29 MB+      | `apt`                           | General-purpose image, popular in CI/CD, ML, etc | Full GNU toolchain. Familiar to most users.                                             |
| **debian**                 | \~22–120 MB   | `apt`                           | Stable base for many apps                        | Very stable and popular upstream of Ubuntu.                                             |
| **python**                 | \~25–900 MB   | Varies (based on Debian/Alpine) | For Python apps and scripts                      | Comes in many variants: `python:3.11-alpine`, `python:3.10-slim`, etc.                  |
| **node**                   | \~50–900 MB   | Varies                          | Node.js-based apps and frontends                 | Multiple variants like `node:alpine`, `node:slim`                                       |
| **golang**                 | \~300–800 MB  | Varies                          | Go language builds and apps                      | Often used with multi-stage builds.                                                     |
| **busybox**                | \~1 MB        | N/A                             | Super minimal shell scripting or base tools      | More for testing/debugging or very minimal containers.                                  |
| **scratch**                | 0 MB          | N/A                             | Ultra-minimal (empty) base                       | Used in final stage of multi-stage builds (e.g., for static binaries).                  |
| **centos**                 | \~200 MB      | `yum/dnf`                       | Legacy support and RHEL-based systems            | Now deprecated. Replaced by `rockylinux`, `alma`.                                       |
| **rockylinux**             | \~200 MB      | `dnf`                           | Enterprise-grade containers (CentOS successor)   | RHEL-compatible.                                                                        |
| **nginx**                  | \~20–50 MB    | N/A                             | Web server base container                        | Pre-configured with NGINX, sometimes based on Alpine.                                   |
| **mysql / postgres**       | \~50–200 MB   | N/A                             | Pre-built databases                              | Used in local dev, CI, and testing.                                                     |

# Evolution of SQL Standards
## SQL‑86 (1986)

-- Introduced basic SQL foundations: SELECT, INSERT, UPDATE, DELETE, GROUP BY, HAVING, simple subqueries.

-- No support for ALTER, JOIN, or advanced schema evolution.

# SQL‑89 (1989)

-- Minor revision adding integrity constraints: PRIMARY KEY, FOREIGN KEY, DEFAULT, and CHECK.

-- Introduced bindings for C and Ada languages.

SQL‑92 (1992)

Major overhaul: added explicit JOIN syntax (INNER, LEFT, RIGHT, FULL, CROSS, NATURAL).

Introduced set operations: UNION, INTERSECT, EXCEPT, plus the CASE statement.

Expanded type support (DATE, TIME, TIMESTAMP) and more rigorous integrity features.

learnsql.com
letsupdateskills.com

SQL:1999 (SQL3)

Introduced object-relational extensions:

User-defined types, structured types (akin to classes).

Recursive queries via WITH [RECURSIVE].

OLAP enhancements (ROLLUP, CUBE, GROUPING SETS).

Procedural extensions (triggers, stored procedures via SQL/PSM).

UNNEST, boolean types, distinct types, and role-based access control.

Wikipedia
learnsql.com

SQL:2003

Introduced window functions, MERGE, CREATE TABLE AS, CREATE TABLE LIKE.

Added SQL/XML support and sequence generators, identity columns.

Wikipedia
Coginiti

SQL:2006

Focused on enhancements to SQL/XML interoperability.

learnsql.com
Medium

SQL:2008

Enhanced functionality: TRUNCATE, extended MERGE, INSTEAD OF triggers, partitioned joins.

Added CASE enhancements (WHEN lists), derived column name enhancements, and improved pattern matching (XQuery).

Wikipedia

SQL:2011

Integrated temporal database support:

PERIOD FOR, SYSTEM VERSIONING, system & application time tables.

Temporal predicates: CONTAINS, OVERLAPS, AS OF SYSTEM TIME, VERSIONS BETWEEN.

Wikipedia

SQL:2016

Major updates including:

JSON support: functions to create, query, and validate JSON.

Row Pattern Recognition: pattern querying in row sequences.

LISTAGG aggregation function.

Polymorphic table functions (flexible return types).

DECFLOAT data type.

Wikipedia

SQL:2019

Introduced Part 15: multidimensional arrays, enabling MDARRAY types and related operators.

more.io.vn

SQL:2023

Key modern enhancements:

Property Graph Queries (SQL/PGQ): enabling graph-style queries over relational data.

Advanced JSON features:

Native JSON types (T801, T802, T803)

JSON path enhancements, comparators, simplified accessors, hex integer literals in JSON paths.

Other additions: GREATEST/LEAST, string padding, multi-character TRIM, ANY_VALUE, UNIQUE NULL treatment, and underscores in numeric literals.
| **openjdk**                | \~250 MB+     | Varies                          | Java applications                                | Based on Debian/Alpine/Ubuntu.                                                          |
| **mariadb**                | \~90–250 MB   | N/A                             | Lightweight MySQL-compatible database            | Popular in containerized environments.                                                  |
| **jupyter/scipy-notebook** | 1 GB+         | `conda`, `pip`                  | Data science, ML pipelines                       | Based on Debian with Jupyter, Pandas, Numpy, etc.                                       |

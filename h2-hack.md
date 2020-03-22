
H2
==============

`version: af6a5662c5d4e772f2c1db6469b8a5f112857dd2`

Build In
==============

```
mem:management_db_9092
    Database ->
    infoSchema
        CATALOGS
        COLLATIONS
        COLUMNS
        COLUMN_PRIVILEGES
        CONSTANTS
        CONSTRAINTS
        CROSS_REFERENCES
        DOMAINS
        FUNCTION_ALIASES
        FUNCTION_COLUMNS
        HELP
        INDEXES
        IN_DOUBT
        RIGHTS
        ROLES
        SCHEMATA
        SEQUENCES
        SETTINGS
        TABLES
        TABLE_PRIVILEGES
        TABLE_TYPES
        TRIGGERS
        TYPE_INFO
        USERS
        VIEWS
```

URL
===============

```
jdbc:h2:{
 {.|mem:|inmemory:}[name] |
 [file:]fileName |
 {tcp|ssl}:[//]server[:port][,server2[:port]]/name
}[;key=value;...]
```

Properties
===============

* data suffix: .data.db
* trace suffix: .trace.db
* trace suffix start: .trace.db.start
* log suffix: .lock.db
* temp suffix: .tmp.db
* lob suffix: .lob.db

`-`

* CACHE_TYPE
* CIPHER
* CREATE
* DB_CLOSE_ON_EXIT
* FILE_LOCK
* IGNORE_UNKNOWN_SETTINGS
* IFEXISTS
* PASSWORD: [filePassword\s]?[userPassword]
* RECOVER
* STORAGE: BINARY | TEXT
* USER

`-`

* ALLOW_LITERALS
* ASSERT
* DB_CLOSE_DELAY
* CACHE_SIZE: LRU | TQ
* CLUSTER
* COLLATION
* COMPRESS_LOB
* DEFAULT_LOCK_TIMEOUT
* DEFAULT_TABLE_TYPE
* DATABASE_EVENT_LISTENER: '?className'?
* IGNORECASE
* LOCK_TIMEOUT
* LOG: 0[admin rights required] | 1 | 2
* LOCK_MODE
* MAX_LENGTH_INPLACE_LOB
* MAX_LOG_SIZE
* MAX_MEMORY_ROWS
* MAX_MEMORY_UNDO
* MODE
* MULTI_THREADED
* OPTIMIZE_REUSE_RESULTS
* READONLY
* SCHEMA
* TRACE_LEVEL_FILE
* TRACE_LEVEL_SYSTEM_OUT
* TRACE_MAX_FILE_SIZE
* THROTTLE
* WRITE_DELAY

Constants
=================

magic: -- H2 0.5/[B|T] -- 

Data Structure
=================

structure
-----------------

|     0-7     |  8-15  | 16-23 | 24 | ... | ... | ... | ... | pos - 2  | pos - 1 |
|-------------|--------|-------|----|-----|-----|-----|-----|----------|---------|
| block count |   id   |  len  |type|data |type |data | ... | Checksum |   LF    |

e.g.
-----------------

00000001 00000000 00000004 e 00000001 e 00000000 e 00000006 n

type
-----------------

|   b   | c  |  d  | e | f  |   g   |
|-------|----|-----|---|----|-------|
|BOOLEAN|BYTE|SHORT|INT|LONG|DECIMAL|

|  h   |  i  | j  | k  |    l    |  m  |
|------|-----|----|----|---------|-----|
|DOUBLE|FLOAT|TIME|DATE|TIMESTAMP|BYTES|

|  n   |        o        | p  | q  |
|------|-----------------|----|----|
|STRING|STRING_IGNORECASE|BLOB|CLOB|

|  r  |    s     |     t     | u  | -  |
|-----|----------|-----------|----|----|
|ARRAY|RESULT_SET|JAVA_OBJECT|UUID|NULL|

Misc
=================

userPasswordHash: sha([username]@[password])

FileLockMethod: file | no | socket














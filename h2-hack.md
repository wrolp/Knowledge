
H2
==============

`version: af6a5662c5d4e772f2c1db6469b8a5f112857dd2`

Build In
==============

```
mem:management_db_9092
    Database ->
    infoSchema
        FUNCTION_COLUMNS
        CONSTANTS
        SEQUENCES
        RIGHTS
        TRIGGERS
        CATALOGS
        CROSS_REFERENCES
        SETTINGS
        FUNCTION_ALIASES
        VIEWS
        TYPE_INFO
        CONSTRAINTS
        COLUMNS
        DOMAINS
        SCHEMATA
        COLUMN_PRIVILEGES
        HELP
        TABLE_PRIVILEGES
        TABLE_TYPES
        TABLES
        ROLES
        IN_DOUBT
        USERS
        COLLATIONS
        INDEXES
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
* LOG
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






















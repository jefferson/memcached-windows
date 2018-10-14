# Memcached-windows
What is Memcached?
Free & open source, high-performance, distributed memory object caching system, generic in nature, but intended for use in speeding up dynamic web applications by alleviating database load.

Memcached is an in-memory key-value store for small chunks of arbitrary data (strings, objects) from results of database calls, API calls, or page rendering.

Memcached is simple yet powerful. Its simple design promotes quick deployment, ease of development, and solves many problems facing large data caches. Its API is available for most popular languages. 

Reference: (https://memcached.org/)

There are two major sources for the pre-built windows binary: Jellycan and Northscale, and both versions can be used.

# Attention
This versions are vulnerable to multiple RCE vulnerabilities and out of date.

# Install version < 1.4.5

- c:\memcached\memcached.exe -d install

# Start and Stop
- c:\memcached\memcached.exe -d start
- c:\memcached\memcached.exe -d stop

# Windows Service
- c:\memcached\memcached.exe" -d runservice -m 512

# Uninstall
- c:\memcached\memcached.exe -d uninstall

# Install version >= 1.4.5

- schtasks /create /sc onstart /tn memcached /tr "'c:\memcached\memcached.exe' -m 512"

# Uninstall
- schtasks /delete /tn memcached

# Clients

- .Net in C#:
1. Repository: https://github.com/enyim/EnyimMemcached
2. Nuget: https://www.nuget.org/packages/EnyimMemcached/



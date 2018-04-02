# Memcached-windows
What is Memcached?
Free & open source, high-performance, distributed memory object caching system, generic in nature, but intended for use in speeding up dynamic web applications by alleviating database load.

Memcached is an in-memory key-value store for small chunks of arbitrary data (strings, objects) from results of database calls, API calls, or page rendering.

Memcached is simple yet powerful. Its simple design promotes quick deployment, ease of development, and solves many problems facing large data caches. Its API is available for most popular languages. 

Reference: (https://memcached.org/)

There are two major sources for the pre-built windows binary: Jellycan and Northscale, and both versions can be used. The following are the download links for the memcached windows binaries:

- http://code.jellycan.com/files/memcached-1.2.5-win32-bin.zip
- http://code.jellycan.com/files/memcached-1.2.6-win32-bin.zip
- http://downloads.northscale.com/memcached-win32-1.4.4-14.zip
- http://downloads.northscale.com/memcached-win64-1.4.4-14.zip
- http://downloads.northscale.com/memcached-1.4.5-x86.zip
- http://downloads.northscale.com/memcached-1.4.5-amd64.zip

Reference: https://commaster.net/content/installing-memcached-windows

# Install version < 1.4.5

1. c:\memcached\memcached.exe -d install

# Start and Stop
c:\memcached\memcached.exe -d start
c:\memcached\memcached.exe -d stop

#Windows Service
"c:\memcached\memcached.exe" -d runservice -m 512

# Uninstall
c:\memcached\memcached.exe -d uninstall

# Install version >= 1.4.5

1. schtasks /create /sc onstart /tn memcached /tr "'c:\memcached\memcached.exe' -m 512"

# Uninstall
1. schtasks /delete /tn memcached

# Clients

- .Net in C#:
1. Repository: https://github.com/enyim/EnyimMemcached
2. Nuget: https://www.nuget.org/packages/EnyimMemcached/



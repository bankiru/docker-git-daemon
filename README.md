# Docker for git-daemon

## Quick start

```bash
docker run --name git-daemon -d \
    -p 9418:9418 \
    -v /var/git:/git \
    bankiru/git-daemon
```

## Options

```bash
docker run --name git-daemon -d \
    -p 9418:9418 \
    -v /var/git:/git \
    -e "OPTION_NAME=OPTION_VALUE" \
    bankiru/git-daemon
```

* STRICT_PATHS    : 0 or 1, default 0
* INIT_TIMEOUT    : numeric, 0 - use git default value
* TIMEOUT         : numeric, 0 - use git default value
* MAX_CONNECTIONS : numeric, default 32
* VERBOSE         : 0 or 1, default 0
* REUSEADDR       : 0 or 1, default 1
* USER            : string, default root
* GROUP           : string, default root

## References

- http://git-scm.com/docs/git-daemon

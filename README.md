phpSphinxRedis
==============

This is a smarter Sphinx full text search API client which effectively caches all search results in Redis. This effectively lets you take load off Sphinx when you know your indexing intervals. Presently, the TTL for all keys are set at 1800 seconds.

***You will need to install Predis***

```
sudo pear channel-discover pear.nrk.io
sudo pear install nrk/Predis
```

***Deleting all the cached search results***

`redis-cli KEYS "sphinx_search_*" | xargs redis-cli DEL`


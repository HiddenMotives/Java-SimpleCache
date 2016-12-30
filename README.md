# Java SimpleCache

The Java SimpleCache Class is an easy way to cache 3rd party API calls.

## Usage

A very basic usage example:

```java
SimpleCache cache = new SimpleCache();
String data = cache.get_data("label", "http://some.api.com/file.json");
System.out.println(data);
```

A more advanced example:

```java
SimpleCache cache = new SimpleCache();
cache.set_cache_time(3);
cache.set_cache_path("cache/");	
cache.set_cache_extension(".json");

String data = null;

if(cache.is_cached("label)) {
    data = cache.get_cache("label");
} else {
    data = cache.grab_url("http://some.api.com/file.json");
    cache.set_cache("label", data);
}

System.out.println(data);
```

## Credits

SimpleCache Caching Class Originally published in PHP by [Gilbert Pellegrom](https://github.com/gilbitron/PHP-SimpleCache). Ported to Java by me :)

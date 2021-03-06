<!--
layout:  index.html
title:   SERVER - Tile38
class:   command
command: server
-->

Show server stats and details.

## Examples

```tile38
SERVER
```

## Returns

The `stats` array will contain information about the server.

- `aof_size`: The size in bytes of the aof on disk.
- `avg_item_size`: An estimated size in bytes of each object.
- `caught_up`: When in follow mode, this indicates if the server has the same data as the leader.
- `following`: When in follow mode, this is the address of the leader.
- `heap_size`: The actual amount of memory in bytes that the server is using.
- `id`: A unique identifier for the server. This is auto-generated once when the server first starts up.
- `in_memory_size`: The estimated memory size in bytes that the key is using.
- `num_collections`: The key count.
- `num_objects`: The object count.
- `num_points`: The total number of latitude, longitude coordinates in the key. This will always be equal to or greater than `num_objects`.
- `pointer_size`: The size in bytes of an underlying pointer. May be used to provide a hint if the server is in 32-bit or 64-bit mode.
- `read_only`: Is `true` when the server is in readonly mode.


```tile38-json
{
    "ok":true,
    "stats":{
        "aof_size":38,
        "avg_item_size":264488,
        "caught_up":true",
        "following":"localhost:9851",
        "heap_size":264488,
        "id":"968d0db485fb2e33911a4d172ae47954",
        "in_memory_size":90,
        "num_collections":1,
        "num_objects":1,
        "num_points":1,
        "pointer_size":8,
        "read_only":false
    },
    "elapsed":"190.941µs"
}
```

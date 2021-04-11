---
title: "Interesting PHP question"
date: 2021-04-02T11:15:00Z
---

Recently, I've come up with an interesting question that can potentially be used for interviewing candidates 🙂

Imagine we have such a PHP class.

```
class Collection implements Countable
{
    private $items = [];

    public function __construct(array $data)
    {
        $this->items = $data;
    }

    public function count(): int
    {
        return count($this->items);
    }
}

$collection = new Collection(['one', 'two', 'three']);
```

Which is going to be faster: ```count($collection)``` or ```$collection->count()```? 

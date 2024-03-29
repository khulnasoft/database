# Access through our API endpoint

You can access our whole database through a JSON endpoint:

```
GET https://khulnasoft.github.io/database/database.json
```

**Example:**

```js
{
    "tool-1": {
        "__url": "https://github.com/khulnasoft/database/blob/main/category/tool-1.yaml"
        /* tool data */
    },
    ...
}
```

The schema of tools can be found in [`_sample.yaml`](../_sample.yaml), but there are some special
fields that might be computed during build time. Usually we will prefix them with 2 underscores `__`
(e.g. `__url`).

This is a list of those special fields:
- `__url`: A back link to the YAML file hosted on Github.

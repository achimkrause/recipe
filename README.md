# recipe
CLI which scrapes recipe pages into markdown (dropping all the nonessential info)

# usage
Requires pup and jq. To use, simply invoke the recipe script on the URL of a recipe website, like

> ./recipe www.example.com

# how it works
The script looks for <script type="application/ld+json"> tags which contain JSON data with @type: 'recipe', following the schema.org standard for recipes. This metadata is typically exposed by most big cooking websites.

For now, there is no clean error handling, and I have tested it only with a few websites. If you use it, let me know how it works!

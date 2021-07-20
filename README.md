# shoky recipe database
hello welcome to this database thingy

as you can see there are 4 files here

- [ ] changelist.json
- [ ] change2.json
- [ ] ebookchange.json
- [ ] recipe2.json

Don't question me about the weird names. Allow me to explain what these files do:

## Uses for files

- changelist.json: checks if a certain word inputted is a thing, and then changes the word (key) into the value. (one word shortcuts)
- change2.json: checks if the entire input is equal to a key. If so, replace entire thing with the value. (multi word shortcuts)
- ebookchange.json: a shortcut for enchanted books.
- recipe2.json: a recipe database lol

## additional notes

YOU MUST FOLLOW THE SYNTAXES IN ALL THE FILES!!!

For example, in recipe2.json you must capitalize the item names.

### guide for recipe2

ok so you want to add new recipes to the database? no problem!

first, please look at recipe2.json and then go to the end.

next thing you do should be to add a recipe in JSON format, in the style of:

```
{   
    ...
    "item":{
        "item":{
            "useditem1":count1,
            "useditem2":count2,
            ...
            "useditemn":count_n
        }
    }
}
```

```
Example: Aspect of the End

"Aspect of the End":{
  "Aspect of the End":{
   "Enchanted Eye of Ender":32,
   "Enchanted Diamond":1
  }
 }
```

if the item is forged:

```
{   
    ...
    "item":{
        "item":{
            "useditem1":count1,
            "useditem2":count2,
            ...
            "useditemn":count_n
        },
        "forge":{
            "tier":hotm_tier_required <int>,
            "time":"xhxmxs" (omit when necessary)
        }
    }
}
```

```
Example: DR-X355
Note: the capitalization is weird, i know, this is due to how the bot capitalizes things in the code
{
    ...
    "Titanium Drill Dr-x355":{
        "Titanium Drill Dr-x355":{
            "Drill Engine":1,
            "Fuel Tank":1,
            "Golden Plate":6,
            "Refined Titanium":10,
            "Refined Mithril":10
    },
    "forge":{
        "time":"2d16h",
        "tier":5
    }
}
}```

additionally, if multiple items are created using the recipe, you can add "for" to tell the bot how much is crafted:

```
{   
    ...
    "item":{
        "item":{
            "useditem1":count1,
            "useditem2":count2,
            ...
            "useditemn":count_n
        },
        "count":count (This is how many items are crafted using the recipe! If it's just 1, no need to add this.)
    }
}
```

```Example: Ultimate Carrot Candy (8x Superb Carrot Candy + 1x Ultimate Carrot Candy Upgrade -> 10x Ultimate Carrot Candy)
{
    ...
    "Ultimate Carrot Candy":{
        "Ultimate Carrot Candy":{
            "Superb Carrot Candy":8,
            "Ultimate Carrot Candy Upgrade":1
        },
    "for":10
 }
 ```

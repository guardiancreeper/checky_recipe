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

```{   
    ...
    "item":{
        "item":{
            "useditem1":count1,
            "useditem2":count2,
            ...
            "useditemn":count_n
        }
    }
}```

if the item is forged:

```{   
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
}```
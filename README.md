# LaundryMap

<img src="https://media.giphy.com/media/bCvO8biVh8WyI/giphy.gif" width=300px placeholder="iron man">

Welcome to my LaundryMap! We offer the following services: `iron`, `mend`, `clean`. Unfortunately, we can only process individual items of clothing. We have not figured out how to process loads... ¯\\_(ツ)_/¯

## Iron
Write a function `iron` that removes the wrinkles (capital letters) from a single piece of clothing.

``` javascript
function iron(clothing_item){
    // code in here
}

// DRIVER CODE
console.log("ironed green shirt", iron("grEEn shIrt") === "green shirt" )
```

#### Ironing Load - Mock Data

```
// input
var wrinkled_clothes = [
  "grEEn shIrt",
  "TubE sockS",
  "TIe Dye shIrt",
  "gray pants",
  "HAndKerChief",
  "whItE bLousE"
]

// expected output
var expected_ironed_clothes = [
  "green shirt",
  "tube socks",
  "tie dye shirt",
  "gray pants",
  "handkerchief"
  "white blouse"
]
```

## Mend

Write a function `mend` that repairs/removes the holes ("/") in a single piece of clothing.

``` javascript
function mend(clothing_item){
    // code in here
}

// DRIVER CODE
console.log("mended tube socks", mend("tu/be socks") === "tube socks" )
```

#### Mending Load - Mock Data
```
// input
var torn_clothes = [
  "knit swe/ater",
  "tu/be socks",
  "blue je/ans",
  "whit/e blouse"
]

// expected output
var expected_mended_clothes = [
  "knit sweater",
  "tube socks",
  "blue jeans",
  "white blouse"
]
```


## Clean

Write a function `clean` that removes the dirt ("*") from a single piece of clothing.

``` javascript
function clean(clothing_item){
    // code in here
}

// DRIVER CODE
console.log("cleaned blue shirt", clean("*blue shirt*") === "blue shirt" )
```

#### Cleaning Load - Mock Data
```
var dirty_clothes = [
  "*blue shirt*",
  "****argyle socks****",
  "**ugly sweater**",
  "**brown plaid pants**",
  "*paisley dress shirt*"
]

var expected_clean_clothes = [
  "blue shirt",
  "argyle socks",
  "ugly sweater",
  "brown plaid pants",
  "paisley dress shirt"
]
```


## Challenge: Help us process loads!
Can you help the LaundryMap process an entire load of laundry, not just individual clothing items?

Given the inputs and expected output, specified above, what needs to happen for the following assertions to pass?

``` javascript
console.log("ironed", my_output === expected_ironed_clothes)
console.log("mended", my_output === expected_mended_clothes)
console.log("cleaned", my_output === expected_clean_clothes)
```

> **Hint**: You're going to need to loop (or iterate!) over the clothes in each load of laundry!

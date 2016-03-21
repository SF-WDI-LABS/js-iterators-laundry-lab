# LaundryMap

<img src="https://media.giphy.com/media/bCvO8biVh8WyI/giphy.gif" width=300px placeholder="iron man">

Welcome to my LaundryMap! We offer the following services: `iron`, `mend`, `clean`. Unfortunately, we can only process individual items of clothing. We have not figured out how to process loads... ¯\\_(ツ)_/¯

## Iron
Write a function `iron` that removes the wrinkles (capital letters) from a single piece of clothing.

``` javascript
function iron(clothing_item){
    // code in here
    // return ironed_clothing_item;
}

// DRIVER CODE
console.log("ironed green shirt:", iron("grEEn shIrt") === "green shirt" );
```

<details>
<summary>**Solution** (Click Here)</summary>
<br>
```js
function iron(clothing_item){
    return clothing_item.toLowerCase();
}

console.log("ironed green shirt:", iron("grEEn shIrt") === "green shirt" )
```
</details>

#### Ironing Load - Sample Data

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
    // return mended_clothing_item;
}

// DRIVER CODE
console.log("mended tube socks:", mend("tu/be socks") === "tube socks" )
```

<details>
<summary>**Solution** (Click Here)</summary>
<br>
```js
function mend(clothing_item){
    return clothing_item.replace("/", "");
}

console.log("mended tube socks:", mend("tu/be socks") === "tube socks" )
```
</details>

#### Mending Load - Sample Data
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
    // return clean_clothing_item;
}

console.log("cleaned blue shirt:", clean("*blue shirt*") === "blue shirt" );
```

<details>
<summary>**Solution** (Click Here)</summary>
<br>
```js
function clean(clothing_item){
    return clothing_item.replace(/\*/g, "");
}

console.log("cleaned blue shirt:", clean("*blue shirt*") === "blue shirt" );
```
</details>

#### Cleaning Load - Sample Data
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

Given the inputs and expected output, specified above, how would you generate the `expected` output?

> **Hint**: You're going to need to loop (or iterate!) over the clothes in each load of laundry!

## Solutions

<details>
<summary>**Using a painful manual approach** (Click Here)</summary>
<br>
```js
var output = [];

output.push( iron(wrinkled_clothes[0]) );
output.push( iron(wrinkled_clothes[1]) );
output.push( iron(wrinkled_clothes[2]) );
output.push( iron(wrinkled_clothes[3]) );
output.push( iron(wrinkled_clothes[4]) );
output.push( iron(wrinkled_clothes[5]) );

console.log("ironed:", output);
```
</details>

<details>
<summary>**Using a `for` loop** (Click Here)</summary>
<br>
```js
var output = [];

for(var i=0; i<wrinkled_clothes.length; i++){
    output.push( iron(wrinkled_clothes[i]) );   
}

console.log("ironed:", output);
```
</details>

<details>
<summary>**Using the `forEach` method** (Click Here)</summary>
<br>
```js
var output = [];

wrinkled_clothes.forEach(function process_item(item){
    output.push( iron(item) );   
})

console.log("ironed:", output);
```
</details>

<details>
<summary>**Using the `map` method** (Click Here)</summary>
<br>
```js
var output = wrinkled_clothes.map(iron);

console.log("ironed:", output);
```
</details>

# Javascript snippets

## In operator

```js
let building = {
  levels: 101,
  buildingName: 'Financial Tower'
}

console.log('levels is a property of building:', 'levels' in building)
console.log('name is a property of building:', 'name' in building)
```

output:
```
levels is a property of building: true
name is a property of building: false
```

---

## Spread operator

### Add property to object based on a condition
See the positive conditions after spread operator

```js
let isNameValid = true
let buildingName = 'Financial Tower'

let building = {
  levels: 101,
  ...(isNameValid && {buildingName}),
  ...(true && {city: 'New York'})
}

console.log(building)
```
output:
```
{
  levels: 101 ,
  buildingName: "Financial Tower" ,
  city: "New York"
} 
```

See the negative conditions after spread operator
```js
let isNameValid = false
let buildingName = 'Financial Tower'

let building = {
  levels: 101,
  ...(isNameValid && {buildingName}),
  ...(false && {city: 'New York'})
}

console.log(building)
```
output:
```
{
  levels: 101
} 
```



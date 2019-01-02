---
subtitle: "There is now way you can throw 3 lines of code in an algorithm without have to include a conditional. It's time to guide the computer on how to make decisions!"
status: "draft"
title: "Using Conditionals in Coding"
cover: "https://ucarecdn.com/4cc6fa0b-2530-4052-aa7e-8dac03788ac3/"
textColor: "white"
date: "2018-12-12"
tags: ["conditional rendering", "if else", "using conditionals"]

---

## What is a condition?

We make decisions every day since we wake up, most of them are already automated in our brains like taking a shower and some other requiere more attention like were to invest money or deciding were to eat

A very similar process can happen when coding a computer, you can create scripts that automate the computer behavior and decisions depending on certain variables. 

For example, a baby monitor that send you an SMS when any sound or camera movement happends:

`If`... 
**signal is detected on the mic or camera**... 
send an sms to +1345 5557777.

`Else`... do nothing.

That is what we call a "condition": It limits the execution of a particular block of code depending on one or more variable having expected values.

## How to code a condition

If you are using Javascript conditions can be coded using the `if... else` syntax, for example asuming you have a variable called `babyHasMoved` that you know it will always contain a boolean inside (that can be either true or false), you could have the following condition:
```js
if(babyHasMoved === true){
	sendSMS("The baby has moved just now", +13455557777)
}
```  
[[warning]]
| :point_up: Notice how we are using 3 equal symbols instead of just one. That is because we are doing logical operations. 

You could have a block of code execute only if the condition does not apply using the `else` statement:
```js
if(babyHasMoved === true){
	sendSMS("The baby has moved just now", +13455557777);
}
else{
	//this will only execute if babyHasMoved is different than true 
	sendSMS("The baby has NOT moved", +13455557777);
}
``` 

Or you could have separate conditionals asking in different ways:
```js
if(babyHasMoved === true){
	sendSMS("The baby has moved just now", +13455557777);
}
if(babyHasMoved === false){
	sendSMS("The baby has NOT moved", +13455557777);
}
```

## Combining different logical operations

Some times the situation is more complicated and you need several variables to be able to ask the right question, for example: Should I wear the blue shirt today? Only if it is not dirty, if it fits me and also if the color matches with the pant.

#### The `AND` operator:

Those are 3 separate questions that you can ask on the same condition using **the AND operator** that in Javascript is represented with two amperson characters `&`:

```js
let isDirty = true;
let shirtColor = "blue";
let size = "M";

if(isDirty === false && shiftColor == "blue" && size == "M"){
	putOnShirt();
}
```

#### The `OR` operator:

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE4NDUwNzY3OSwtMTAwMzI3NTM4MCwtNj
g5MzMwMjc0LDIwOTg4NjcyNzgsMTIzODY5MDE0NiwtMTYzNTA0
NzI5MywtMTIyNzI2NjM3MCw3MzA5OTgxMTZdfQ==
-->
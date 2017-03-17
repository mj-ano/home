---
title:  "a = b ?? does it copy all for an Objects. – Shallow Vs Deep Copy"
date:   2017-03-16 15:04:23
categories: [concepts]
tags: [coding]
---

First we need to understand the concept , 

For  an example, you have an object containing references to other objects.

For instance, a Person object, containing references to an Address object, several Phone objects, etc.

```
If you make a shallow copy of that Person object you now have two Person objects, 
but they share the Address objects and Phone objects.
```

In other words, you only make a new Person object, and then link it up to the existing Address and Phone objects.

```
A deep copy, on the other hand, will make new copies of everything, 
so that both Person objects now have their own set of Address and Phone objects.
```

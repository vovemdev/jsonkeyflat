## Overview of jsonKeyFlat

jsonKeyFlat - flatten or unflatten json data. Need of flattening JSON:- There are many reasons for the need of flattening JSON, such as for a better and more understandable view that is there are only key-value pairs are present without any nesting.

## Why?

jsonKeyFlat Objects extension to convert a nested data layer object into a new object with only one layer of key/value pairs.

## Angular Module TS

```
import { Injectable } from "@angular/core";
import { HttpClient } from "@angular/common/http";
import { Observable } from "rxjs";

import { flatten } from "jsonkeyflat";

// service.ts
  constructor(private http: HttpClient) {
    this.fetchJSON().subscribe(json => {
      this.languageDictionary = flatten(json);
    });
  }

```

## JavaScript / TypeScript - Modules

## jsonKeyFlat

```
import { flatten } from "jsonkeyflat";

const json = flatten(
   {
      json: {
         flatten: {
             deep: 100
      } },
      recursive: {
         level: {
            nested: true
       } }
    }
)
console.log(json);
```

## unflatten

```
import { unflatten } from 'jsonkeyflat';

const json = unflatten(
   {
   'json.flatten.deep': 100,
   'recursive.level.nested': true
   }
)

console.log(json);
```

## NPM Package

```
https://www.npmjs.com/package/jsonkeyflat

```

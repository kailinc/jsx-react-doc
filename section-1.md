## Specifying the React Element Type

First part of JSX tag determins type of React Element

Capitalized types = JSX tag is referring to React component

tags get compiled into a direct reference to the named variable
if use JSX <Foo /> expression, Foo must be in scope

# React Must Be in Scope

JSX compiles into call React.createElement, so React Library must also always be in scope from your JSX code.
 - only worry about this when integrate react into diff parts of app

ex:
```js
import React from 'react';
import CustomButton from './CustomButton';

function WarningButton() {
  // return React.createElement(CustomButton, {color: 'red'}, null);
  return <CustomButton color="red" />;
}

```
if don't use JS bundler (import react from 'react') and load React from <script> tag = it is already in scope as the React Global

# @degreerichi/laravelform

> Laravelform helps you to handle laravel validation automatically directly on you react app using axios

[![NPM](https://img.shields.io/npm/v/@degreerichi/laravelform.svg)](https://www.npmjs.com/package/@degreerichi/laravelform) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save @degreerichi/laravelform
```

## Usage

```jsx
import React, { Component } from 'react'

import LaravelForm from '@degreerichi/laravelform'
import '@degreerichi/laravelform/dist/index.css'

class Example extends Component {
  render() {
    return (
      <LaravelForm url="http://www.example.com" method="get">
        <div>
          <div>
            <label htmlFor="">Username</label>
            <input type="text" name="username" className="customclass"/>
          </div>
          <div>
            <label htmlFor="">Email</label>
            <input type="text" name="email" className="customclass"/>
          </div>
          <div>
            <label htmlFor="">Pass</label>
            <input type="password" name="pass" className="customclass"/>
          </div>
          <input type="submit" value="Send"/>
      </div>
    </LaravelForm>
    );
  }
}
```
> **Important note:** The **name** attribute on each input is required
> and has to be the exact same name placed on the laravel validation rule on the backend.

## LaravelForm parameters

```jsx
/**
* @param string {url} Action for the form (expect laravel app and validation via api)
* @param string {method}[get, post...] Method to be used on the request
* @param any {inputComponent} If you want to use a custom input react component, just pass the raw component to be used
* @param function {success([])} Called once the form was succesfully submitted without validation errors
* @param function {onChange(state)} Called every time any form input has changed its value (onchange event)
* @param function {error([error])} Called when a validation error was found
* @param boolean {submitDisabled} Variable to handle externally if the submit button is disabled
*/
```

## License

MIT © [degreerichi](https://github.com/degreerichi)

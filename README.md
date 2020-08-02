# react-jwt

> Small library for decoding a json web token (JWT)

[![NPM](https://img.shields.io/npm/v/react-jwt.svg)](https://www.npmjs.com/package/react-jwt)

## Install

```bash
npm install react-jwt
or
yarn add react-jwt
```

## Usage

```jsx
import React from "react";
import { useJwt } from "react-jwt";

const token = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiR3VzdGF2byIsImlhdCI6MTU5NjQwODI1OSwiZXhwIjo0NzUyMTY4MjU5fQ.ThwsJW2KfMTl0y24tTGWKHqvYWRp1iyo_Kh2KWTHuXc";

const Example = () => {
  const { decodedToken, isExpired } = useJwt(token);
  /*
    If is a valid jwt, 'decodedToken' will be a object
    it could look like:
    {
      "name": "Gustavo",
      "iat": 1596408259,
      "exp": 4752168259
    }

    'isExpired' will return a boolean
    true => your token is expired
    false => your token is not expired
  */

  return (
    <div>
      ...
    </div>
  );
};
```

## License

MIT © [@gustavo0197](https://github.com/@gustavo0197)

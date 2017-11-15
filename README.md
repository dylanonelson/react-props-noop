# react-props-noop
> Sensible defaults for function props in React.js

## Motivation
I found myself writing lots of React components that take props that are functions. Having a default prop defined for all your non-required props is a best practice, but in the case of a function, the best default is often to do nothing. Thus, react-props-noop was born.

## What this library does
Nothing. For example:

```js
import noop from 'react-props-noop';
noop(); // Nothing happens
```

In React code:
```jsx
import PropTypes from 'prop-types';
import React from 'react';
import noop from 'react-props-noop';

const Button = ({ onClick }) => <button onClick={onClick} />

Button.propTypes = {
  onClick: PropTypes.func,
};

Button.defaultProps = {
  onClick: noop,
};
```

## Installation
```bash
npm install --save react-props-noop
```

## Is this library a joke?
Yes.

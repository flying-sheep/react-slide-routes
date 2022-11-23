# react-slide-routes 🏄‍♂️

The easiest way to slide React routes

[![npm](https://img.shields.io/npm/v/react-slide-routes.svg?style=flat-square)](https://www.npmjs.com/package/react-slide-routes)
[![npm](https://img.shields.io/npm/dt/react-slide-routes?style=flat-square)](https://www.npmtrends.com/react-slide-routes)
[![npm bundle size](https://img.shields.io/bundlephobia/minzip/react-slide-routes?style=flat-square)](https://bundlephobia.com/result?p=react-slide-routes)
[![npm peer dependency version](https://img.shields.io/npm/dependency-version/react-slide-routes/peer/react?style=flat-square)](https://github.com/facebook/react)
[![npm peer dependency version](https://img.shields.io/npm/dependency-version/react-slide-routes/peer/react-router?style=flat-square)](https://github.com/remix-run/react-router)
[![GitHub](https://img.shields.io/github/license/nanxiaobei/react-slide-routes?style=flat-square)](https://github.com/nanxiaobei/react-slide-routes/blob/main/LICENSE)

## Fit

React Router v6

> For React Router v5, please use [`react-slide-routes@1.1.0`](https://github.com/nanxiaobei/react-slide-routes/blob/367ff0dfa94c9ff3234fc55493c27e3a53996ccd/README.md) and note that the usage is different.

## Add

```shell script
yarn add react-slide-routes

# or

npm i react-slide-routes
```

## Use

```jsx
import SlideRoutes from 'react-slide-routes';
import { Route } from 'react-router-dom';

const App = () => (
  <SlideRoutes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
    <Route path="/contact" element={<Contact />} />
  </SlideRoutes>
);
```

## Live

[Play a live demo here → 🤳](https://codesandbox.io/s/react-slide-routes-bnzlu)

![live](live.gif)

## API

| Prop        | Type       | Required | Default   | Description                                                                                              |
| ----------- | ---------- | -------- | --------- | -------------------------------------------------------------------------------------------------------- |
| `animation` | `string`   |          | `'slide'` | Animation effect type, `'slide'`, `'vertical-slide'`, or `'rotate'`                                      |
| `compare`   | `function` |          | `null`    | Comparison function that defines route order, defaults to definition order; see below for details        |
| `duration`  | `number`   |          | `200`     | `transition-duration` in `ms`                                                                            |
| `timing`    | `string`   |          | `'ease'`  | `transition-timing-function`, one of `'ease'` `'ease-in'` `'ease-out'` `'ease-in-out'` `'linear'`        |
| `destroy`   | `boolean`  |          | `true`    | If `false`, prev page will still exits in dom, just invisible                                            |

The `compare` prop works similarly to [`Array.prototype.sort`][sort]’s `compareFn` argument.
It takes two arguments “a” and “b”, both react-router’s [`RouteObject`s][route].
The return value is `-1` if “a” sorts before “b”, `1` if after, and `0` if they should stay in original order:

```ts
(a: RouteObject, b: RouteObject) => -1 | 0 | 1 
```

[sort]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#syntax
[route]: https://reactrouter.com/en/main/hooks/use-routes

## License

[MIT License](https://github.com/nanxiaobei/react-slide-routes/blob/main/LICENSE) © [nanxiaobei](https://lee.so/)

## FUTAKE

If you use WeChat, please try "**FUTAKE**". It's a WeChat mini app for your inspiration moments. 🌈

![FUTAKE](https://s3.bmp.ovh/imgs/2022/07/21/452dd47aeb790abd.png)

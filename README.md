This repo reproduces an issue with Next.js on Ubuntu/Debian machines.

Run:

```
yarn install && yarn run build && yarn run start
```

And visit [http://localhost:3000/](http://localhost:3000/) to reproduce:
```
ready - started server on 0.0.0.0:3000, url: http://localhost:3000
TypeError: Cannot read property 'vertical' of undefined
    at Object.children (/pnpm-next-antd/node_modules/antd/lib/form/FormItemLabel.js:84:26)
    at a.b.render (/pnpm-next-antd/node_modules/react-dom/cjs/react-dom-server.node.production.min.js:44:213)
    at a.b.read (/pnpm-next-antd/node_modules/react-dom/cjs/react-dom-server.node.production.min.js:41:83)
    at Object.exports.renderToString (/pnpm-next-antd/node_modules/react-dom/cjs/react-dom-server.node.production.min.js:52:138)
    at Object.renderPage (/pnpm-next-antd/node_modules/next/dist/server/render.js:756:46)
    at Object.defaultGetInitialProps (/pnpm-next-antd/node_modules/next/dist/server/render.js:369:51)
    at Function.getInitialProps (/pnpm-next-antd/.next/server/chunks/105.js:422:20)
    at Object.<anonymous> (/pnpm-next-antd/node_modules/next/dist/shared/lib/utils.js:103:33)
    at Generator.next (<anonymous>)
    at asyncGeneratorStep (/pnpm-next-antd/node_modules/next/dist/shared/lib/utils.js:15:28)
```

There should be no error if built/ran on macOS.


(This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app)).

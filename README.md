<div align="center">
  <img src="/tyfon.svg" width="200px"/>
  <h1>TyFON</h1>
  <span><b>Ty</b>ped <b>F</b>unctions <b>O</b>ver <b>N</b>etwork</span>
</div>

<br><br>

TyFON serves TypeScript functions over network, in a seamless RPC style that is super easy to consume as well.
```bash
npm i tyfon -g
```

## Usage

Suppose you have `index.ts` as follows:
```ts
export function getMsg(name: string) {
  return `Hellow ${name}!`;
}
```

Init tyfon and set it to serve:
```bash
tyfon init
tyfon serve
```

Now open `localhost:8000/getMsg/?1=World`.

## Client-Side

```bash
tyfon add backend localhost:8000
```

Now in your client-side code, do this:

```ts
import { getMsg } from '@api/backend';

getMsg('World').then(console.log);
```

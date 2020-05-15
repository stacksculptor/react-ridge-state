# react-ridge-state :weight_lifting_woman: :muscle:	:weight_lifting_man: 
**Simple** :muscle: **fast** ⚡️ and **small** (1.6kb) global state management for React which does not get in your way. # :racing_car:


```
yarn add react-ridge-state
```

or

```
npm install react-ridge-state --save
```

## Roadmap :running_woman: :running_man:

- Persistent storage with custom get / set

## Features :woman_juggling:

- Uses proxy
- React / React Native
- Simple
- Fast
- Very tiny

## Getting started :clap: :ok_hand:

### Create a new state

```typescript
import { newRidgeState } from "react-ridge-state";
interface CartProduct {
  id: number;
  name: string;
}
const defaultState: CartProduct[] = [{ id: 1, name: "Product" }];
export const cartProductsState = newRidgeState<CartProduct[]>({
  key: "CartState", // needs to be unique across other global state
  defaultState,
});
```

### Use state inside components

```typescript
import { useRidgeState } from "react-ridge-state";

const [cartProduct, setCartProduct] = useGlobalState(cartProductsState);
```

### Use state outside of React

```typescript
import { getRidgeState } from "react-ridge-state";
getRidgeState(cartProductsState);
```

### Set state outside of React

```typescript
import { getRidgeState } from 'react-ridge-state'
setRidgeState(cartProductsState, [{{id:1, name:'NiceProduct'}])

```

## Publish

```
yarn build
```

or

```
npm run build
```

```
npm version patch
npm publish
```

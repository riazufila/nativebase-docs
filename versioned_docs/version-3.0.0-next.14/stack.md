---
id: stack
title: Stack
---

Align Items vertically

## Implements

- `View` from [react-native](https://reactnative.dev/docs/view)
- `space`, `border`, `layout`, `flexbox` and `color` from [style-system](https://styled-system.com/api)

## Example

```SnackPlayer name=Stack%20Example
import React from "react";
import { Stack, Box, NativeBaseProvider } from "native-base";
function StackComponent() {
  return (
    <Stack space={3} mb={3}>
      <Box borderRadius={4} height={70} shadow={1} bg="red.400" />
      <Box borderRadius={4} shadow={1} height={70} bg="purple.500" />
      <Box borderRadius={4} shadow={1} height={70} bg="yellow.300" />
    </Stack>
  );
}
export default function () {
  return (
    <NativeBaseProvider>
      <StackComponent />
    </NativeBaseProvider>
  );
}
```

> If you want to pass custom components (not a nativebase imported component) as direct Children of Stack, VStack, HStack, or ZStack you must wrap that in a `Box` for Stacks to work as expected.

## Extra props

- `style`: Applies user-defined styles and accepts a `stylesheet`.
- `children` : Renders components as `Box` children. Accepts a `JSX.Element` or an array of `JSX.Element`
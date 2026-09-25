# Calculator App | React Native + Expo

![React Native](https://img.shields.io/badge/react_native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Expo](https://img.shields.io/badge/expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

An iOS-style calculator for Android, iOS and web, built with **React Native**, **Expo** and **Expo Router**.

## Features

- **Basic operations:** addition, subtraction, multiplication and division.
- **Live formula and sub-result:** the screen shows the formula you type and a preview of the result before you press `=`.
- **Editing tools:** clear (`C`), toggle sign (`+/-`) and delete the last digit.
- **Input guards:** no leading zeros and only one decimal point per number.
- **Reusable UI:** `CalculatorButton` and `ThemeText` components with a shared color palette.

## Architecture

All calculator logic lives in the `useCalculator` custom hook. The screen only renders state and calls actions.

- `number` holds the value being typed, `prevNumber` holds the sub-result and `formula` holds the full expression.
- The last operator is kept in a `useRef`, so changing it does not cause extra renders.
- An `Operator` enum maps each operation to its symbol.

## Project structure

```
app/                         Screens (Expo Router)
components/CalculatorButton  Keypad button
components/ThemeText         Text with display variants
hooks/useCalculator.tsx      Calculator state and logic
constants/Colors.ts          Color palette
styles/global-styles.ts      Shared styles
```

## Tech stack

React Native 0.76, Expo SDK 52, Expo Router 4, TypeScript, Jest (`jest-expo`).

## Getting started

```bash
npm install
npx expo start
```

Open the app in Expo Go, an Android emulator, an iOS simulator or the browser.

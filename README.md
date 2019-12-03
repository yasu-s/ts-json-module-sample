# ts-json-module-sample

## 概要

* TypeScript で resolveJsonModule を使用したサンプルです。
* tsconfig.json 上で resolveJsonModule を指定することでjsonファイルから型の抽出・生成を行うことができます。

## 実行環境

* Node.js - 10.x
* Yarn - 1.17.x

## 使用ライブラリ

* TypeScript - 3.7.x

## サンプルソース

### tsconfig.json

```json
{
  "compilerOptions": {
    "target": "esnext",
    "module": "commonjs",
    "sourceMap": true,
    "outDir": "./dist",
    "esModuleInterop": true,
    "resolveJsonModule": true
  },
  "include": [
   "src/**/*"
  ]
}
```

### src/data.json

```json
{
  "id": 1,
  "memo": "hogehoge"
}
```

### src/main.ts

```typescript
import data from './data.json';

console.log(`id=${data.id}, memo=${data.memo}`);
```

## 実行結果

```bash
yarn start
id=1, memo=hogehoge
```

## URL

* https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-9.html#new---resolvejsonmodule

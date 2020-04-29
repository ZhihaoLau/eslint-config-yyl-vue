# eslint-config-yyl-vue
为 yyl-vue 项目提供 eslint 文件

## install
```bash
yarn add eslint-config-yyl-vue prettier eslint -D
```

## usage
修改 `package.json` 文件
```json
{
  "eslintConfig": {
    "extends": ["yyl-vue"]
  },
  "eslintIgnore": [
    "node_modules",
    "/build"
    "/dist",
    "/test",
    "**/js/lib"
  ],
  "prettier": {
    "printWidth": 100,
    "tabWidth": 2,
    "singleQuote": true,
    "semi": false,
    "trailingComma": "none",
    "bracketSpacing": true,
    "jsxBracketSameLine": true,
    "arrowParens": "always",
    "quoteProps": "consistent"
  },
  "scripts": {
    "eslint": "eslint --ext=vue,js ./",
    "prettier": "prettier --write ./**/*.{vue,js}"
  }
}
```
> 为了和 prettier 不冲突，请按照 `package.json` 的 `prettier` 属性进行配置

## 自定义 prettier
可以通过定义 `prettier/prettier` rules 来修改
```json
{
  "eslintConfig": {
    "rules": {
      "prettier/prettier": ["error", {
        "semi": true
      }]
    }
  },
  "prettier": {
    "semi": true
  }
}
```

## 定义 .prettierignore
```
node_modules/
dist/
```

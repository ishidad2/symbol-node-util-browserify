# symbol-node-util-browserify

ブラウザ用 symbol-node-util です。

## how to build

```
npm install symbol-node-util
npm install browserify -g
npm install uglify-js -g

browserify -r ./node_modules/symbol-node-util -o symbol-node-util-2.0.0.js
uglifyjs -o  symbol-node-util-2.0.0.min.js  symbol-node-util-2.0.0.js
```

## how to use

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>symbol-node-util</title>
</head>
<body>

  <script src="./symbol-node-util.min-2.0.0.js"></script>
  <script>
    const symbolUtil = require("/node_modules/symbol-node-util");
    (async()=>{
      const node = await symbolUtil.getActiveNode(104);
      console.log(node);
    })()
  </script>
</body>
</html>
```

or

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>symbol-node-util</title>
</head>
<body>

  <script src="https://ishidad2.github.io/symbol-node-util-browserify/symbol-node-util-2.0.0.min.js"></script>
  <script>
    const symbolUtil = require("/node_modules/symbol-node-util");
    (async()=>{
      const node = await symbolUtil.getActiveNode(104);
      console.log(node);
    })()
  </script>
</body>
</html>
```

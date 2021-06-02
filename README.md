## Background

This is a minimal reproducible example for [issue 34](https://github.com/tim-soft/react-spring-lightbox/issues/34) of https://github.com/tim-soft/react-spring-lightbox.

In summary, in a clean repo, `npm i` needs to be executed twice for this package to be installed properly.

## Tested Environment

```
NodeJS: 12.12.0 / 14.16.0
NPM: 6.11.3 / 6.14.11
```

## Step to reproduce

1. Remove `node_modules` folder if exists.
2. Run `npm i`.
3. Notice that `package-lock.json` is changed. (diff is attached)
4. Necessary packages are not installed.
5. Run `npm i` again.
6. Notice that `package-lock.json` is changed back.

## Changes to `package-lock.json` after the first run

```diff
{
  "name": "spring-lightbox-issue",
  "version": "1.0.0",
  "lockfileVersion": 1,
  "requires": true,
  "dependencies": {
    "@babel/runtime": {
      "version": "7.14.0",
      "resolved": "https://registry.npmjs.org/@babel/runtime/-/runtime-7.14.0.tgz",
      "integrity": "sha512-JELkvo/DlpNdJ7dlyw/eY7E0suy5i5GQH+Vlxaq1nsNJ+H7f4Vtv3jMeCEgRhZZQFXTjldYfQgv2qmM6M1v5wA==",
      "requires": {
        "regenerator-runtime": "^0.13.4"
      }
    },
-    "@react-spring/animated": {
-      "version": "npm:@tim-soft/react-spring-animated@9.0.0-beta.33",
-      "resolved": "https://registry.npmjs.org/@tim-soft/react-spring-animated/-/react-spring-animated-9.0.0-beta.33.tgz",
-      "integrity": "sha512-fXPywLQOWciayrq6nbdl+bAngZxNDDC7ZNigOvYv6Gfhqr9RNNQ0Nkn71bTomjQ4YKRlXjz9gcjzwKS/cW10gA==",
-      "requires": {
-        "@babel/runtime": "^7.3.1",
-        "@react-spring/shared": "9.0.0-beta.33",
-        "tiny-invariant": "^1.0.4"
-      }
-    },
-    "@react-spring/core": {
-      "version": "npm:@tim-soft/react-spring-core@9.0.0-beta.34",
-      "resolved": "https://registry.npmjs.org/@tim-soft/react-spring-core/-/react-spring-core-9.0.0-beta.34.tgz",
-      "integrity": "sha512-12DdLwQNgq+bFLGlcEaqUqe3tdqchZipbMb2F9H4jYfSIieQ8hQHRQvunS88j3EOMBKv9fdT8NTCZ0Br1Hd4Wg==",
-      "requires": {
-        "@babel/runtime": "^7.3.1",
-        "@react-spring/animated": "npm:@tim-soft/react-spring-animated@9.0.0-beta.33",
-        "@react-spring/shared": "9.0.0-beta.33",
-        "use-memo-one": "^1.1.0"
-      }
-    },
-    "@react-spring/shared": {
-      "version": "9.0.0-beta.33",
-      "resolved": "https://registry.npmjs.org/@react-spring/shared/-/shared-9.0.0-beta.33.tgz",
-      "integrity": "sha512-oGalrGtIg7ZMn9VW5PzLFMDAa8vH5V0XIeC4WFk7JB4hBfhxx6yzPwjMxSJfRrt/Q+WuS2cPoR5qN0RpH+fJOA==",
-      "requires": {
-        "@babel/runtime": "^7.3.1",
-        "tiny-invariant": "^1.0.4"
-      }
-    },
-    "@react-spring/web": {
-      "version": "npm:@tim-soft/react-spring-web@9.0.0-beta.36",
-      "resolved": "https://registry.npmjs.org/@tim-soft/react-spring-web/-/react-spring-web-9.0.0-beta.36.tgz",
-      "integrity": "sha512-9qhvnJ/VkIeG59jTB4KgYvq5MH6qW/cPxylnORZlwHjNTA4WWtGB8CO08HDgIEoF6f5VaHWs3QIlthgsiN++Jg==",
-      "requires": {
-        "@babel/runtime": "^7.3.1",
-        "@react-spring/animated": "npm:@tim-soft/react-spring-animated@9.0.0-beta.33",
-        "@react-spring/core": "npm:@tim-soft/react-spring-core@9.0.0-beta.34",
-        "@react-spring/shared": "9.0.0-beta.33"
-      }
-    },
    "react-spring-lightbox": {
      "version": "1.5.0",
      "resolved": "https://registry.npmjs.org/react-spring-lightbox/-/react-spring-lightbox-1.5.0.tgz",
      "integrity": "sha512-/MzmJ3cNuFTVvn4A5MG4HQXWxnfGVyZ9FHwFnJvsKLr/X1Vp6iw1ojFBFrrJegoEC2tVzWZ1UK4GJLul/dBMfw==",
      "requires": {
        "@babel/runtime": "^7.12.13",
-        "@react-spring/web": "npm:@tim-soft/react-spring-web@9.0.0-beta.36",
        "react-use-gesture": "9.0.4"
      }
    },
    "react-use-gesture": {
      "version": "9.0.4",
      "resolved": "https://registry.npmjs.org/react-use-gesture/-/react-use-gesture-9.0.4.tgz",
      "integrity": "sha512-G0sbQY+HSm2gSVIlD+LE1unpVpG7YZRTr8TI72vo0Nu1lecJtvjbcY3ZLonEZLTtODJgLL6nBllMRXyy0bRSQA=="
    },
    "regenerator-runtime": {
      "version": "0.13.7",
      "resolved": "https://registry.npmjs.org/regenerator-runtime/-/regenerator-runtime-0.13.7.tgz",
      "integrity": "sha512-a54FxoJDIr27pgf7IgeQGxmqUNYrcV338lf/6gH456HZ/PhX+5BcwHXG9ajESmwe6WRO0tAzRUrRmNONWgkrew=="
-    },
-    "tiny-invariant": {
-      "version": "1.1.0",
-      "resolved": "https://registry.npmjs.org/tiny-invariant/-/tiny-invariant-1.1.0.tgz",
-      "integrity": "sha512-ytxQvrb1cPc9WBEI/HSeYYoGD0kWnGEOR8RY6KomWLBVhqz0RgTwVO9dLrGz7dC+nN9llyI7OKAgRq8Vq4ZBSw=="
-    },
-    "use-memo-one": {
-      "version": "1.1.2",
-      "resolved": "https://registry.npmjs.org/use-memo-one/-/use-memo-one-1.1.2.tgz",
-      "integrity": "sha512-u2qFKtxLsia/r8qG0ZKkbytbztzRb317XCkT7yP8wxL0tZ/CzK2G+WWie5vWvpyeP7+YoPIwbJoIHJ4Ba4k0oQ=="
    }
  }
}

```

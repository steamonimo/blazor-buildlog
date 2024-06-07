# repository for debugging build problem

## versions

* visual studio: 17.10.1
* dotnet --version: 8.0.300
* affected project: blazor
* edge: 125.0.2535.79

## build command to publish

dotnet publish -c Release -o c:\iis-publish

## errors in edge

```javascript
127.0.0.1/:1  Failed to find a valid digest in the 'integrity' attribute for resource 'http://127.0.0.1/_framework/dotnet.native.wasm' with computed SHA-256 integrity 'U1JSgnum2OTerSq8i5Y9L17deHEWJmae0djinSPLyJM='. The resource has been blocked.
127.0.0.1/:1  Unknown error occurred while trying to verify integrity.
dotnet.js:3  Error in mono_download_assets: Error: download 'http://127.0.0.1/_framework/dotnet.native.wasm' for dotnet.native.wasm failed 0 TypeError: Failed to fetch
Q @ dotnet.js:3
await in Q (asynchron)
(anonym) @ dotnet.js:3
setTimeout (asynchron)
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
Ne @ dotnet.js:3
await in Ne (asynchron)
create @ dotnet.js:3
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
dotnet.js:3  Uncaught (in promise) TypeError: Failed to fetch
    at Object.S [as fetch_like] (dotnet.js:3:4466)
    at dotnet.js:3:11553
    at dotnet.js:3:11569
S @ dotnet.js:3
(anonym) @ dotnet.js:3
(anonym) @ dotnet.js:3
Promise.then (asynchron)
oe @ dotnet.js:3
(anonym) @ dotnet.js:3
Y @ dotnet.js:3
G @ dotnet.js:3
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
Ne @ dotnet.js:3
await in Ne (asynchron)
create @ dotnet.js:3
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
dotnet.js:3  Uncaught (in promise) Error: download 'http://127.0.0.1/_framework/dotnet.native.wasm' for dotnet.native.wasm failed 0 TypeError: Failed to fetch
    at dotnet.js:3:9940
    at async Y (dotnet.js:3:8828)
    at async G (dotnet.js:3:8153)
(anonym) @ dotnet.js:3
Promise.catch (asynchron)
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
Ne @ dotnet.js:3
await in Ne (asynchron)
create @ dotnet.js:3
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
dotnet.js:3  Uncaught (in promise) Error: download 'http://127.0.0.1/_framework/dotnet.native.wasm' for dotnet.native.wasm failed 0 TypeError: Failed to fetch
    at dotnet.js:3:9940
    at async Y (dotnet.js:3:8828)
    at async G (dotnet.js:3:8153)
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
(anonym) @ dotnet.js:3
setTimeout (asynchron)
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
Ne @ dotnet.js:3
await in Ne (asynchron)
create @ dotnet.js:3
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
blazor.webassembly.js:1  Uncaught (in promise) Error: Failed to start platform. Reason: TypeError: Cannot read properties of undefined (reading 'out')
    at mn (blazor.webassembly.js:1:57654)
mn @ blazor.webassembly.js:1
await in mn (asynchron)
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
```

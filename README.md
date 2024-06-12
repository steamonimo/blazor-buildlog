# repository for debugging build problem

## versions

* visual studio: 17.10.2
* dotnet --version: 8.0.300
* affected project: blazor
* edge: 125.0.2535.79

## build command to publish

dotnet publish -c Release -o c:\iis-publish

## errors in edge

```javascript
dotnet.js:3  MONO_WASM: TypeError: Cannot read properties of undefined (reading 'out')
    at $l (http://localhost/_framework/dotnet.runtime.8.0.5.8hv7wyhg5a.js:3:198913)
    at ze (http://localhost/_framework/dotnet.js:3:30895)
    at http://localhost/_framework/dotnet.js:3:30131
    at async Object.create (http://localhost/_framework/dotnet.js:3:34510)
    at async http://localhost/_framework/blazor.webassembly.js:1:43466
    at async http://localhost/_framework/blazor.webassembly.js:1:58010
    at async mn (http://localhost/_framework/blazor.webassembly.js:1:57613)
u @ dotnet.js:3
(anonym) @ dotnet.js:3
ke @ dotnet.js:3
create @ dotnet.js:3
await in create (asynchron)
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ (Index):20
dotnet.js:3  Error in mono_download_assets: TypeError: Cannot read properties of undefined (reading 'out')
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
(anonym) @ (Index):20
9dotnet.runtime.8.0.5.8hv7wyhg5a.js:3  Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'out')
    at $l (dotnet.runtime.8.0.5.8hv7wyhg5a.js:3:198913)
    at ze (dotnet.js:3:30895)
    at dotnet.js:3:30131
    at async Object.create (dotnet.js:3:34510)
    at async blazor.webassembly.js:1:43466
    at async blazor.webassembly.js:1:58010
    at async mn (blazor.webassembly.js:1:57613)
$l @ dotnet.runtime.8.0.5.8hv7wyhg5a.js:3
ze @ dotnet.js:3
(anonym) @ dotnet.js:3
await in (anonym) (asynchron)
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
load @ blazor.webassembly.js:1
(anonym) @ blazor.webassembly.js:1
await in (anonym) (asynchron)
hn @ blazor.webassembly.js:1
mn @ blazor.webassembly.js:1
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ (Index):20
dotnet.runtime.8.0.5.8hv7wyhg5a.js:3  Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'out')
    at $l (dotnet.runtime.8.0.5.8hv7wyhg5a.js:3:198913)
    at ze (dotnet.js:3:30895)
    at dotnet.js:3:30131
    at async Object.create (dotnet.js:3:34510)
    at async blazor.webassembly.js:1:43466
    at async blazor.webassembly.js:1:58010
    at async mn (blazor.webassembly.js:1:57613)
$l @ dotnet.runtime.8.0.5.8hv7wyhg5a.js:3
ze @ dotnet.js:3
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
(anonym) @ (Index):20
blazor.webassembly.js:1  Uncaught (in promise) Error: Failed to start platform. Reason: TypeError: Cannot read properties of undefined (reading 'out')
    at mn (blazor.webassembly.js:1:57654)
mn @ blazor.webassembly.js:1
await in mn (asynchron)
fn @ blazor.webassembly.js:1
An @ blazor.webassembly.js:1
(anonym) @ (Index):20
localhost/:1  Failed to find a valid digest in the 'integrity' attribute for resource 'http://localhost/_framework/dotnet.native.wasm' with computed SHA-256 integrity 'U1JSgnum2OTerSq8i5Y9L17deHEWJmae0djinSPLyJM='. The resource has been blocked.
localhost/:1  Unknown error occurred while trying to verify integrity.
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
(anonym) @ (Index):20
```

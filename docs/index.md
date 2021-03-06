<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [prepare][1]
-   [hibernate][2]
-   [resume][3]

## prepare

[index.js:16-18][4]

Prepares a binary by injecting getter and setter function for memory, globals and tables.

**Parameters**

-   `binary` **[ArrayBuffer][5]** a wasm binary
-   `include` **[Object][6]**  (optional, default `{memory:true,table:true}`)
    -   `include.memory` **[Boolean][7]** whether or not to include memory (optional, default `true`)
    -   `include.table` **[Boolean][7]** whether or not to include the function table (optional, default `true`)
    -   `include.globals` **[Array][8]&lt;[Boolean][7]>** whether or not to
        include a given global. Each index in the array stands for a global index.
        Indexes that are set to false or left undefined will not be persisted. By
        default all globals are persisted. (optional, default `Array.<true>`)
-   `symbol` **[String][9]** a string used to prefix the injected setter and getter functions (optional, default `'_'`)

Returns **[ArrayBuffer][5]** the resulting wasm binary

## hibernate

[index.js:27-64][10]

Given a Webassembly Instance this will produce an Object containing the current state of
the instance

**Parameters**

-   `instance` **Webassembly.Instance** 
-   `symbol` **[String][9]** the symbol that will be used to find the injected functions (optional, default `'_'`)

Returns **[Object][6]** the state of the wasm instance

## resume

[index.js:72-102][11]

Resumes a previously hibernated Webassembly instance

**Parameters**

-   `instance` **WebAssembly.Instance** 
-   `state` **[Object][6]** the previous state of the wasm instance

Returns **WebAssembly.Instance** 

[1]: #prepare

[2]: #hibernate

[3]: #resume

[4]: https://github.com/dfinity/wasm-persist/blob/6d8733c40b8d0082927219c30a05351081c913eb/index.js#L16-L18 "Source code on GitHub"

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer

[6]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[7]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[8]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[9]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[10]: https://github.com/dfinity/wasm-persist/blob/6d8733c40b8d0082927219c30a05351081c913eb/index.js#L27-L64 "Source code on GitHub"

[11]: https://github.com/dfinity/wasm-persist/blob/6d8733c40b8d0082927219c30a05351081c913eb/index.js#L72-L102 "Source code on GitHub"

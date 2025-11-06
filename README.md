Reproduction repo for testing formatting when both EditorConfig and Prettier are present.

Setup:

- The `test.js` file contains unformatted code
- [.editorconfig](./.editorconfig) specifies `indent_size = 4`
- Prettier default tab width is 2
- Custom Prettier config in [package.json](./package.json) sets `"semi": false` to help see if Prettier is being used.

Test with Zed:

- Format (by saving) the `test.js` file
- Disable or enable built-in Prettier: `"prettier"` in [.zed/settings.json](.zed/settings.json)
- Disable or enable npm-installed Prettier: `"formatter"` in [.zed/settings.json](.zed/settings.json)

Desired outcome:

```js
const a = {
    foo: "bar",
}
```

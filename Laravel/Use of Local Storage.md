Visit Url: https://blog.logrocket.com/localstorage-javascript-complete-guide/

To use `localStorage` in your web applications, there are five methods to choose from:

1.  `setItem()`: Add key and value to `localStorage`
2.  `getItem()`: This is how you get items from `localStorage`
3.  `removeItem()`: Remove an item by key from `localStorage`
4.  `clear()`: Clear all `localStorage`
5.  `key()`: Passed a number to retrieve the key of a localStorage

### `setItem()`: How to store values in `localStorage`
window.localStorage.setItem('name', 'Obaseki Nosa');

To store arrays or objects, you would have to convert them to strings.
To do this, we use the `JSON.stringify()` method before passing to `setItem()`.

const person = {
    name: "Obaseki Nosa",
    location: "Lagos",
}
window.localStorage.setItem('user', JSON.stringify(person));

### `getItem()`: How to get items from `localStorage`
window.localStorage.getItem('user');

This returns a string with value as:
“{“name”:”Obaseki Nosa”,”location”:”Lagos”}”

To use this value, you would have to convert it back to an object.
To do this, we make use of the `JSON.parse()` method, which converts a JSON string into a JavaScript object.
JSON.parse(window.localStorage.getItem('user'));

### `removeItem()`: How to delete `localStorage` sessions
window.localStorage.removeItem('name');

### `clear()`: How to delete all items in `localStorage`
Use the `clear()` method to delete all items in `localStorage`.
window.localStorage.clear();

### `key()`: How to get the name of a key in `localStorage`
The `key()` method comes in handy in situations where you need to loop through keys and allows you to pass a number or index to `localStorage` to retrieve the name of the key.

var KeyName = window.localStorage.key(index);

## `localStorage` browser support
`localStorage` as a type of web storage is an HTML5 specification. It is supported by major browsers including IE8. To be sure the browser supports `localStorage`, you can check using the following snippet:

if (typeof(Storage) !== "undefined") {
    // Code for localStorage
    } else {
    // No web storage Support.
}

## `localStorage` limitations

As easy as it is to use `localStorage`, it is also easy to misuse it. The following are limitations, and also ways to NOT use `localStorage`:

-   Do not store sensitive user information in `localStorage`
-   It is not a substitute for a server based database as information is only stored on the browser
-   `localStorage` is limited to 5MB across all major browsers
-   `localStorage` is quite insecure as it has no form of data protection and can be accessed by any code on your web page
-   `localStorage` is synchronous, meaning each operation called would only execute one after the other

With these, we have been armed with the power of `[localStorage](https://blog.logrocket.com/web-storage-made-simple-use-local-storage-state/)` in our web applications.


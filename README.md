# webdriver-testpage
This simple web page tests the value of the `navigator.webdriver` JavaScript DOM property.

## Test scenario
There are three different buttons that check the value of `navigator.webdriver` in different scopes:
1. In the regular page scope;
2. In the scope of the (at page load already) included iframe;
3. In the scope of a runtime created iframe.

## How to run
To serve the page for localhost, run
```
$ python -m SimpleHTTPServer
```
in the project folder. Then use the web browser and surf to `http://localhost:8000`.

The output is printed to the browser tools console. In Firefox, this can be opened with the shortcut `Ctrl+Shift+k`.

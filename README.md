# webdriver-testpage
This web page tests the value of the `navigator.webdriver` JavaScript DOM property. It can also check for different `navigator` properties by adjusting `let property = "webdriver";` inside `index.html`.

## Test scenario
The opened test page determines the specified property `navigator.webdriver` in different contexts:
1. In the regular page scope;
2. In a statically included iframe;
3. In a dynamically created iframe;
4. In a dynamically created, nested iframe;
5. It tries to open a pop-up window and access the property there.

Each context is checked instantly and for a second time after an intentional delay. For details check `index.html`.

## How to run
To serve the page for localhost, run
```
$ python -m SimpleHTTPServer
```
in the project folder. Then use the web browser and surf to `http://localhost:8000`. We use this method to access the test page via `localhost` because web browsers sometimes seem to behave differently for `file:///` domains.

Note there is no Python program contained in this project.`SimpleHTTPServer` is a Python module serving the current directory via a local HTTP server. It may be necessary to first install `SimpleHTTPServer`. Other methods to serve the test page via HTTP will also work.

The test results are added to a list on the actual web page.

## Acknowledgment
Thanks to Alexander Schlarbs [User Agent Switcher](https://gitlab.com/ntninja/user-agent-switcher/), their code and discussions regarding DOM spoofing.

# react-loading-ui
React loaing component.

## Getting started

#### Install with NPM:

```
$ npm install react-loading-ui
```

#### Usage

**Live Demo [CodeSandbox](https://codesandbox.io/s/react-loading-ui-khrt7 "CodeSandbox")**

- Set the default settings (optional).
- To use, just call the ````Loading()```` function.

> Note: The ````Loading()```` function **toggle** between **hide** and **show**.

```jsx
import React, { Component } from 'react';
import { Loading } from 'react-loading-ui'

class App extends Component {

    saveForm() {

        /* Show loading-ui */
        Loading();

        fetch(url, requestOptions)
            .then((response) => {
                if (response.ok) {
                    return response.json();
                }

                /* Hide loading-ui */
                Loading();
            });

    }
    render() {
        return (
            <div>
                <button type="button" onClick={(e) => this.saveForm()}>Save Form</button>
            </div>
        )
    }

}

export default App;
```

##### Default Settings
You can set the component settings for your entire application or whenever you call ````Loading({settings})````.

```jsx
SetDefault({
    /* Loading title */
    title: "",
    /* Loading text */
    text: "",
    /* Show progress bar */
    progress: false,
    /* Close the loading when progress is over */
    progressedClose: false,
    /* Default theme [light|dark] */
    theme: "light",
});
```
##### Loading

````Loading()```` preview with light color theme.

![Loading()](http://barisates.com/git/rlui/loading.jpg "Loading")

##### Progress
```Loading({ progress: true })``` preview with light color theme.

With the ```Progress(progress)``` function you can ensure the loading progress, see the [demo](https://codesandbox.io/s/react-loading-ui-khrt7 "demo").

![Porgress](http://barisates.com/git/rlui/progress.jpg "Porgress")

##### CSS Overrides

If you want to customize the styles, you can use the following classNames:
- loading-ui-overlay
- loading-ui-body
- loading-ui-title
- loading-ui-text
- loading-ui-spinner
- loading-ui-progress-bar

------------
#### Author

**Barış Ateş**
 - http://barisates.com
 - [github/barisates](https://github.com/barisates "github/barisates")
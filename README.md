# Typescript React/Redux Snippets

Contains basic snippets for React components and React-redux components.

| Snippet | Prefix |
| --- | --- |
| Basic react component | `tsrc→` |
| Redux container | `tsrrc→` |
| Redux container with implemented connect | `tsrrci→` |
---
## Basic react component preview
```javascript
import * as React from "react";

interface IComponentNameProps {};

interface IComponentNameState {};

class ComponentName extends React.Component<IComponentNameProps, IComponentNameState> {
    public render(): JSX.Element {
        return (<span>Body</span>);
    }
}
export default ComponentName;
```
---
## Redux container preview
```javascipt
import * as React from "react";
import { connect } from "react-redux";

interface IComponentNameProps {};

interface IComponentNameState {};

class ComponentName extends React.Component<IComponentNameProps, IComponentNameState> {
    public render(): JSX.Element {
        return (<span>Body</span>);
    }
}

export default connect()(ComponentName);
```
---
## Redux container with implemented connect preview
```javascript
import * as React from "react";
import { connect } from "react-redux";

interface IComponentNameProps {};

interface IComponentNameState {};

class ComponentName extends React.Component<IComponentNameProps, IComponentNameState> {
    public render(): JSX.Element {
        return (<span>Body</span>);
    }
}

export default connect(
    (state) => ({
        // Map state to props
    }),
    {
        // Map dispatch to props
    })(ComponentName);
```
---
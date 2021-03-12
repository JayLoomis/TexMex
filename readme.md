# Tex Mex Full Stack #

This is a repository to capture notes about using Django and React to make web apps.
It is based on (at least as a start) the
[Tech with Tim tutorial series](https://www.youtube.com/watch?v=JD-age0BPVo&list=PLzMcBGfZo4-kCLWnGmK0jUBmGLaJxvi4j).

## React stuff ##

### Components ###

A React component is an object that inherits from the `Component` class (there's also a funcitonal
way of working with them). A component identifies a discrete piece of a web page. React is all
about making dynamic updates to HTML, and it does that by making changes to components as required
on the fly.

#### Rendering ####

Within your implementation of a component, you define a `render` method. That method returns the 
HTML representation of the component.

You can embed JavaScript inside the HTML os a `render` method's return statement by surrounding
it in curly braces. For example:

```javascript
render() {
    return <h1>{this.props.name}</h1>
}
```

#### Properties ####

Your components can have properties that are passed as an object to the component's constructor.
You must pass those properties along to the base `Component` class constructor using `super`.

The canonical name for the properties is `props`.

```javascript
export default class App extends Component {
    constructor(props) {
        super(props);
    }
}
```

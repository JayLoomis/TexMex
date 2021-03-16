# Tex Mex Full Stack #

This is a repository to capture notes about using Django and React to make web apps.
It is based on (at least as a start) the
[Tech with Tim tutorial series](https://www.youtube.com/watch?v=JD-age0BPVo&list=PLzMcBGfZo4-kCLWnGmK0jUBmGLaJxvi4j).

## Project setup ##

Install:

-   VSCode
-   Python
-   Node + NPM

### VS Code extensions ###

When installing VS Code extensions, you may find multiple extensions that do the same thing.
Pick your extensions from those that are from well-known, reputable sources. All else being equal,
choose the one that has the most downloads. For this list, I've added the specific extension that
Tex Mex Tim used in his tutorial in parentheses:

-   Prettier
-   Python (ms-python.python)
-   Django (batisteo.vscode-django)
-   ES7 React/Redux/GraphQL/React-Native snippets (dsznajder.es7-react-js-snippets)
-   JavaScript (xabikos.javascriptsnippets)

### Python packages ###

Use `pip install` (`pip3` on Mac) to get these:

-   django
-   djangorestframework

### Set up your Django project ###

1.  Initialize a Django project from a root folder of your choosing:
    
    ```bash
    django-admin startproject my_project
    ```
    
    Django creates a driectory structure for your project with a root folder named
    the same as the project name you specified. For this example, it's named 
    `my_project`.
    
2.  Initialize a Django app within the newly created project for API handling:

    ```bash
    cd my_project
    django-admin startapp api
    ```
    
    Django defines projects that contain multiple applications. Each app has its own
    root folder containing all the structure that Django expects. Your new app should
    be set up in `root/my_project/api`.
    
3.  Add the `api` app to your Django project:

    1.  Open `root/my_project/my_project/settings.py` in VS Code.
    2.  

    


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

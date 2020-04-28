# Nx Gatsby Plugin

Gatsby CLI supports the following commands for development:

* new
* develop
* build
* serve

See more [in the documentation](https://www.gatsbyjs.org/docs/gatsby-cli/). Here's how they are mapped to Nx commands.

## Generate an application

**Gatsby**

```
gatsby new [<app-name> [<starter-url>]]
```

**Nx**

```
nx g @nrwl/gatsby:app <app-name>
```

When using Nx, you can create multiple applications and themes in the same workspace.

Command parameters aren't yet supported by the plugin.

## Development server

**Gatsby**

```
gatsby develop [--host [--port [--open [--https ]]]]
```

**Nx**

```
nx develop <app-name>
```

Navigate to `http://localhost:8000/`. The app will automatically reload if you change any of the source files.

Command parameters aren't yet supported by the plugin.

## Build

**Gatsby**

```
gatsby build [--prefix-paths [--no-uglify [--profile [--open-tracing-config-file [--no-colors ]]]]]
```

**Nx**

```
nx build <app-name>
```

Command parameters aren't yet supported by the plugin.

To build the application and serve it, run:

```
gatsby build <app-name> --serve
```

## Using components from React library
You can use a component from React library generated using Nx package for React. Once you run:

```
nx g @nrwl/react:lib ui
```

the `libs/ui` directory with sample `Ui` component is added to the workspace. 
You can import it like this in your Gatsby files:

```jsx
import { Ui } from 'libs/ui/src';
```

## Further help

Visit the [Nx Documentation](https://nx.dev) to learn more.

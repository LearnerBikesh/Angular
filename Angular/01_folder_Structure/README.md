# What is Angular

Angular is an open-source, TypeScript-based front-end framework developed
and maintained by Google. It is used to build scalable, high-performance
single-page applications (SPAs) with a structured and maintainable architecture.

## Key Features of Angular

- Component-based architecture
- TypeScript support
- Two-way data binding
- Dependency Injection (DI)
- Built-in routing and lazy loading
- Angular CLI for fast development

## Angular vs Other Technologies

| Feature            | Angular     | React      | Vue              |
| ------------------ | ----------- | ---------- | ---------------- |
| Type               | Framework   | Library    | Framework        |
| Language           | TypeScript  | JavaScript | JavaScript       |
| Architecture       | Opinionated | Flexible   | Semi-opinionated |
| Enterprise Support | Strong      | Medium     | Limited          |

# FolderStructure

Folder structure of the Angular project in details

```my-angular-app/
├── .angular/
│ └── cache/
│
├── .vscode/
│ └── settings.json
│
├── node_modules/
│
├── public/
│ └── favicon.ico
│
├── src/
│ ├── app/
│ │ │ ├── app.config.ts
│ │ │ ├── app.css
│ │ │ ├── app.html
│ │ │ ├── app.routes.ts
│ │ │ ├── app.spec.ts
│ │ │ ├── app.ts
│ ├── index.html
│ ├── main.ts
│ └── styles.css
│
├── angular.json
├── package.json
├── package-lock.json
├── tsconfig.json
├── tsconfig.app.json
└── README.md

```

## node_modules

Contains all installed project dependencies required to run and build the application.

## public

Holds static public files that are served directly without Angular processing.

## src

Contains the complete Angular application source code including components, services, and assets.

## .editorconfig

Defines consistent code formatting rules across different editors and IDEs.

## .gitignore

Specifies files and folders that Git should exclude from version control.

## angualar.json

angular.json is the central configuration file for the Angular CLI.
It tells the CLI how to build, serve, test, and package your Angular application.

### What does angular.json contain?

- Project name and root folder

- Build configurations (development / production)

- Entry files (main.ts, index.html)

- Assets configuration (assets/, public/)

- Global styles and scripts

- Output path for build files

- Optimization and bundling settings

used by command like, **ng serve**, **ng build**, **ng test**

## package-lock.json

package-lock.json is an auto-generated file created by npm that records the exact dependency tree installed in your project.

_This file prevent "works on my machine issue" and guarantees same dependencies across all machine_

## package.json

What is package.json?

package.json is the core configuration file of an Angular (Node.js) project.
It defines project metadata, dependencies, scripts, and tooling configuration required to build and run the application.

Angular uses Node.js and npm, so package.json acts as the blueprint of the project. npm install all the dependencies and store it in node module folder

### Structure of package.json

```
{
  "name": "01_folder_Structure",
  "version": "1.0.0",
  "scripts": {},
  "dependencies": {},
  "devDependencies": {}
}

```

Important Sections

- name

  - Project name (01_folder_Structure in this case)
  - Used by npm and CI/CD pipelines

- version

  - poject version
  - follows semantic versioning(major.minor.patch)

- scripts
  - define command used in the
    dev and prod
  -
- dependencies

  - Used at runtime (when application is running)
  - in production

- dev-dependencies
  - Used only during development
  - only when we are developing in our system like angular cli, typescript etc

"dependencies are required to run the application in production, while devDependencies are only needed during development and build time."

## READE.md

Contains project documentation such as project overview, setup instructions, folder structure, and usage details.

**Angular uses multiple tsconfig files to separate application, test, and global TypeScript configurations for better control and optimization.**

## tcsonfig.json

tsconfig.json is the main configuration file for the TypeScript compiler (tsc).
It defines how TypeScript code is compiled into JavaScript across the Angular project.

Angular uses this file as the base configuration, which is then extended by:

- tsconfig.app.json

- tsconfig.spec.json

**Why tsconfig.json is Important**

- Controls TypeScript language features

- Enforces code quality and strictness

- Defines module system and target JavaScript version

- Improves compile-time error detection

- Ensures consistent compilation across environments

## tsconfig.app.json

Extends tsconfig.json and contains TypeScript settings specifically for compiling the Angular application source code.

## tsconfig.spec.json

Extends tsconfig.json and contains TypeScript settings used for compiling and running unit test files.

## .angular

What is the .angular/ folder?

The .angular/ folder is a hidden, auto-generated directory created by the Angular CLI.
It stores internal metadata, cache, and build-related information used to improve performance and tooling.

**Why is .angular/ important?**

- Speeds up ng serve and ng build

- Reduces recompilation time

- Improves developer experience

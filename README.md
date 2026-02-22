# <a href="https://github.com/dmarcoux/godot_templates">dmarcoux/godot_templates</a>

Templates for common files/configs in [Godot C#/.NET](https://godotengine.org/) projects.

## How to Use This Template

1. Create a new repository based on this repository:

- Go to this [repository's page](https://github.com/dmarcoux/godot_templates),
  click on the `Use this template` button and follow instructions.

  *OR*

- With [GitHub's CLI](https://github.com/cli/cli), run `gh repo create
  NEW_REPOSITORY_NAME --template=dmarcoux/godot_templates`.

2. Install tools to run the commands from the next steps:

   ```bash
   mise install
   ```

3. Generate `.gitignore` from `dotnet new` and append the content of [.gitignore](./.gitignore):

   ```bash
   dotnet new gitignore && cat .gitignore.template >> .gitignore && rm .gitignore.template
   ```

   _Note: By generating `.gitignore`, we don't have to keep track of the changes in the `dotnew new gitignore` template._

4. Generate `.editorconfig` to follow the default .NET code style:

   ```bash
   dotnet new editorconfig
   ```

   _Note: By generating `.editorconfig`, we don't have to keep track of the changes in the `dotnew new editorconfig` template._

5. Generate  `global.json` to enforce a specific .NET SDK version with .NET CLI commands and continuous integration.

   ```bash
   mise run generateGlobalJson
   ```

   _Note: By generating `global.json`, we don't have to manually enter the version number of the .NET SDK installed in the development environment._

6. Adapt this README to the project. This complete section can be deleted...

# Development Environment

Rely on [Mise](https://mise.jdx.dev/) to install tools, set environment
variables, and run tasks. Refer to [mise.toml](mise.toml) for details. The Mise
documentation is there to help you get started, there's no need to repeat it all
here. It boils down to activating Mise (_optional_), installing tools, and
running tasks.

Install tools with:

```bash
mise install
```

See available tasks with:

```bash
mise run
```

## JetBrains Rider

Use the IDE [Rider](https://www.jetbrains.com/rider/) from JetBrains with its
built-in support for C#, GDScript, and Godot. Install it via the [JetBrains
Toolbox](https://www.jetbrains.com/toolbox-app/).

To open script files in Rider instead of Godot, open Godot, then go to `Editor` >
`Editor Settings` > `Text Editor` > `External` and enable `Use External Editor`.
Set the `Exec Path` to the path of your Rider executable and the `Exec Flags` to
`{project} --line {line} {file}`. Toggle `Advanced Settings` to see all settings.

More settings/details in the [Rider documentation on
Godot](https://www.jetbrains.com/help/rider/Godot.html).

## Git LFS

1. Install [Git LFS](https://git-lfs.com/).
2. Set it up with:
   ```bash
   git lfs install
   ```

# vscode-scala-sbt
The tasks.json file will work in **vscode** for any **Scala** *sbt* project. It adds support for background compilation,
unit tests and running your **sbt** project.

Include the tasks.json file from this project in your .vscode directory.

Open up your SBT project and then invoke the Build Task (via command pallete or Shift + Cmd + B) - the compilation
process will start in the background and will listen for any changes to the source code. Errors and warnings are
reported in VSCode.

VSCode doesn't support concurrent background tasks yet. If you want to run another task, VSCode will prompt
you to terminate the background compilation process. To deal with this limitation, use the integrated terminal
in VSCode (Ctrl + ~) to launch your unit *test* or *run* commands, e.g. **sbt test** or **sbt run**

If you use *activator* to create your project (and sbt is not recognized), you may need to change
```"command": "sbt"``` to ```"command": "activator"``` or you may install **sbt** to make that command available
in your environment.

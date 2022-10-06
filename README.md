# manage-azure-vms-notebook
A set of step by step notebooks to create and manage virtual machines in azure

## Prerequisits
You need [Visual Studio Code](https://code.visualstudio.com/) with the [.NET Interactive Notebooks](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.dotnet-interactive-vscode) extension.

1. Open **0-requirements.ipynb** file with Visual Studio  and make sure you can connect to your Azure account.
2. Open the rest of the files as needed with Visual Studio Code

[Jupyter Notebooks in VS Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

### If you are not a .NET developer
Either:
- Install [.NET6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)

Or:
- `docker run -p 8888:8888 pocki/minimal-dotnet::20220210`
- Open the file in the JupyterLab.

## How to use

Again, make sure to follow the instructions in **0-requirements.ipynb**.

The rest should be auto explanatory, just fllow file names.

## Why this?

The main motivation is to start working in a virtual/remote/stateless way.

This means that instead of polluting your own machine every time you want or need to install something, configure omething or test something, you should:

1. Create a VM from an existing snapshot (normally a base image that contains whatever your working environment requires).
2. Connect to the VM.
3. Work on it as much as you need.
4. Create snapshots as you go (as checkpoints) and keep document steps.
5. When done:
   1. Finish documentation
   2. Create final snapshot (if necessary)
   3. Delete checkpoint snapshots.
   4. Delete VM.
6. If at some point something fails or is misconfigured:
   1. Delete VM
   2. Create VM from last checkpoint
   3. Goto 2.

## Workflow Recomendations

Most of the software you use will be updated regularly, so you should come up with a process for that. For example:

* Users should not update their Windows, Chrome, Ubuntu, Docker, etc.
* Someone should: Open the base VM, do 1 update. Verify it does not break anything. Create new snapshot. Notify everyone.
* Someone should try to automate that kind of updates.






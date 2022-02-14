# manage-azure-vms-notebook
A set of step by step notebooks to create and manage virtual machines in azure

## How to use
You need [Visual Studio Code](https://code.visualstudio.com/) with the [.NET Interactive Notebooks](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.dotnet-interactive-vscode) extension.

1. Open **requirements.ipynb** file with Visual Studio  and make sure you can connect to your Azure account.
2. Open the rest of the files as needed with Visual Studio Code

[Jupyter Notebooks in VS Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

### If you are not a .NET developer
Either:
- Install [.NET6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)

Or:
- `docker run -p 8888:8888 pocki/minimal-dotnet::20220210`
- Open the file in the JupyterLab.
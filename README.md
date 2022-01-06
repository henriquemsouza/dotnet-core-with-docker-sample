# DOTNET CORE WITH DOCKER SAMPLE



# SETUP
<p> Create  the files 'launch.json' and 'tasks.json'  and add the above code to launch.json</p>

```json
        {
            "name": "Docker .NET Core Launch",
            "type": "docker",
            "request": "launch",
            "preLaunchTask": "docker-run: debug",
            "netCore": {
                "appProject": "${workspaceFolder}/HelloApi.csproj"
            },
            "dockerServerReadyAction": {
                "uriFormat": "%s://localhost:%s/swagger"
            }
        }

```
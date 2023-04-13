Required packages to install prefect:

create a venv

```
python -m venv env
```

install prefect 

```
pip install prefect
```

start prefect server

```
prefect server start 

```

create a deployment

```
prefect deployment build hello.py:hello_world -n demo-deployment
```

upload deployment to server

```
prefect deployment apply <deployment_file>
prefect deployment apply hello_world-deployment.yaml
```

create an prefect agent ( polling flow to run on infrastructure)
multiple agents, work pools, manage concurrency

```
prefect agent start -q 'default'
```

Use prefect cloud server

```
prefect cloud login
```

Re-apply deployment
Everything you will run now, it won't run on localhost but on the cloud server
Re-add an agent ( separation of concepts, security )

Blocks for variables like secrets / etc.

Example with a block storing a string variable



Deployments 

Allow remote configuration and scheduling 
deployment - configuration
prefect api server - deployment 
localhost or prefect cloud server
# Directory Structure

In actual project development, the number of data models and management pages involved is generally large. `fastapi-amis-admin` recommends that the project adopts a directory structure similar to the django project.
Please refer to [fastapi_amis_admin_demo](https://github.com/amisadmin/fastapi_amis_admin_demo), but this is not a mandatory limit, you can also use your own familiar directory structure.

## Execute the initialization command

The initialization project file can be quickly generated by executing the following command

```bash
# Initialize a `FastAPI-Amis-Admin` project
faa new project_name --init

# Initialize a `FastAPI-Amis-Admin` application
faa new app_name
```

## Example project structure

```
│.
│  .gitignore
│  docker-compose.yml
│  Dockerfile
│ README.md
│  
├─backend
│  │  .env
│ │ alembic.ini
│ │ amisadmin.db
│ │ main.py
│  │  requirements.txt
│ │  
│ ├─apps
│ │ │ __init__.py
│ │ │  
│ │ ├─blog
│ │ │ │ admin.py
│ │ │ │ apis.py
│ │ │ │ views.py
│ │ │ │ models.py
│ │ │ │ schemas.py
│ │ │ │ jobs.py
│ │ │ │ settings.py
│ │ │ │ __init__.py
│ │ │ │  
│ │ │ ├─templates
│ │ │ ├─static
│ │ │  
│ │ │          
│ │ ├─demo
│ │ │ admin.py
│ │ │ __init__.py
│ │ │  
│ │ ├─templates
│  │     │      element.html
│  │     │      simple.html
│ │          
│ ├─core
│ │ │ adminsite.py
│ │ │ settings.py
│ │ │ __init__.py
│ │          
│ ├─migrations
│ │ │ env.py
│  │  │  README
│  │  │  script.py.mako
│ │ │  
│ │ ├─versions
│ │ │ bcd68ae939ea_add_url.py
│ │ │ c79e1785119e_init.py
│ │          
│ ├─upload
│ │          
│ ├─utils
│          
├─scripts
       run.sh

```
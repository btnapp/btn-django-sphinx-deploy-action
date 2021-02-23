# btn-django-sphinx-deploy-action
GitHub Action to build and rsync Sphinx JSON builder docs. 

The idea was to include this via `uses` as a `composite` action. 

This isn't currently supported by GHA. 
See https://github.com/actions/runner/issues/646 


```
Error: btnapp/btn-django-sphinx-deploy-action/v1/action.yml (Line: 6, Col: 7): Unexpected value 'uses'
28
Error: btnapp/btn-django-sphinx-deploy-action/v1/action.yml (Line: 6, Col: 7): Required property is missing: run
29
Error: btnapp/btn-django-sphinx-deploy-action/v1/action.yml (Line: 6, Col: 7): Required property is missing: shell
30
Error: btnapp/btn-django-sphinx-deploy-action/v1/action.yml (Line: 7, Col: 7): Unexpected value 'uses'
31
Error: btnapp/btn-django-sphinx-deploy-action/v1/action.yml (Line: 8, Col: 7): Unexpected value 'with'
...
```

As such, copy task into job, with the following secrets set. 

## Secrets: 

* `SSH_KEY`
* `SSH_KNOWN_HOSTS`
* `SSH_USER`
* `SSH_HOST`
* `RSYNC_TARGET_PATH`

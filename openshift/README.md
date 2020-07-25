# brief introduction

I make available a PGAdmin4 template focused on a development environment for the community. We start from an ephemeral configuration, so if the pod is restarted, all saved connections and sql files will be removed

## Basic usage

```
$ oc create -f pgadmin4-template.yaml
```

The previous step loads the template and its artefacts to the current namespace or project.

```
$ oc process pgadmin4-template -p NAME=pgadmin4 -p MAIL=admin@domain.local -p PASSWD=admin | oc create -f -
```

Finally we process the template and initialize the parameter, created each of the artifacts.

- - -

> I hope you find it useful.
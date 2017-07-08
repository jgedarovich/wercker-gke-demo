# Wercker GKE Demo: Get IP address HTTP API

A simple Python application that uses the Bottle framework to serve a JSON encoded client IP address of a user who makes a GET request to /.

Used as an example application for a tutorial on Wercker I am writing.

```
usage: get_ip.py [-h] hostname port

HTTP API for returning a visitor's IP address.

positional arguments:
  hostname    The host IP to listen on.
  port        The port to listen on.

optional arguments:
  -h, --help  show this help message and exit
```

Requires `Python 2` `pip` & `virtualenv` to run.


# weird
had to enable gcr and then run
`gcloud docker push gcr.io/wrecker-demo2/get_ip:bdd20912f3a55422f4653c6f89cb143b0d59c410`
before the kubernetes-deploy step (?) or part of pipeline would work, was
previously getting errors about not being able to pull the image when looking
at `kubectl get pods` and `kubectl describe pods`


As a warm-up exercise, we're having a look at how to access the Kubernetes API using the command line.

In one terminal, do the following (which proxies the API so that we can access it locally):

`kubectl proxy`{{execute T1}}

Now execute in a second terminal the following:

`curl 127.0.0.1:8001/apis/`{{execute T2}}

_Note that you can also create new terminals manually, using the `+` button next to the `Terminal` tab._

Alternatively, instead of `curl` you can also use the raw mode of `kubectl`, again in the second terminal:

`kubectl get --raw=/apis`{{execute T2}}

That was fun! Now it's time for switching gears and moving to Go: meet the `client-go` library.
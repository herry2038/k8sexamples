# k8sexamples

```
cd k8sexamples/operator/examples-inc

operator-sdk new app-operator

$ operator-sdk new app-operator
$ cd app-operator

# Add a new API for the custom resource AppService
$ operator-sdk add api --api-version=app.example.com/v1alpha1 --kind=AppService

# Add a new controller that watches for AppService
$ operator-sdk add controller --api-version=app.example.com/v1alpha1 --kind=AppService

# Build and push the app-operator image to a public registry such as quay.io
$ operator-sdk build herry2038/app-operator
$ docker push herry2038/app-operator
```

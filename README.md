# k8sexamples

```
cd k8sexamples/operator/examples-inc

operator-sdk new app-operator

$ operator-sdk new app-operator
$ cd app-operator

# Add a new API for the custom resource AppService
$ operator-sdk add api --api-version=app.example.com/v1alpha1 --kind=AppService

INFO[0000] Generating api version app.example.com/v1alpha1 for kind AppService. 
INFO[0021] Create pkg/apis/app/v1alpha1/appservice_types.go 
INFO[0021] Create pkg/apis/addtoscheme_app_v1alpha1.go  
INFO[0021] Create pkg/apis/app/v1alpha1/register.go     
INFO[0021] Create pkg/apis/app/v1alpha1/doc.go          
INFO[0021] Create deploy/crds/app_v1alpha1_appservice_cr.yaml 
INFO[0021] Create deploy/crds/app_v1alpha1_appservice_crd.yaml 
INFO[0024] Running code-generation for Custom Resource group versions: [app:[v1alpha1], ] 
INFO[0025] Code-generation complete.                    
INFO[0025] Api generation complete.                     

# Add a new controller that watches for AppService
$ operator-sdk add controller --api-version=app.example.com/v1alpha1 --kind=AppService

INFO[0000] Generating controller version app.example.com/v1alpha1 for kind AppService. 
INFO[0000] Create pkg/controller/appservice/appservice_controller.go 
INFO[0000] Create pkg/controller/add_appservice.go      
INFO[0000] Controller generation complete.   

# Build and push the app-operator image to a public registry such as quay.io
$ operator-sdk build herry2038/app-operator
$ docker push herry2038/app-operator
```

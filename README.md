# CRONJOB SAMPLE
Sample cronjob to list pods and send to MSTeams

# Command to process and create the cronjob.
```console
oc process -f cronjob.yaml | oc create -f -
```
### The Service Account "default"  was used and you must give the right permission to list pods on the namespace 

Run the command below on the namespace that you want to get the pods information
```console
oc policy add-role-to-user view -z default
```

# Additional Information
This job is not parameterized yet, if you want to list the pods in different namespace, you should update the cronjob with you desire namespace.

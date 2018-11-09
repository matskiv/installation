# Customising an Integreatly Cluster

# Prerequisites 

- Familiar with Ansible
- Have credentials to login as an admin in the Integreatly cluster
- Ensure logged into your cluster via oc


## Pull down your cluster's inventory file

Each Integreatly cluster has a secret in the integeratly namespace with an inventory file that
can be used to help you add customisations.

``` 
oc get secret manifest -n webapp --template '{{index .data "generated_inventory"}}'  | base64 -D > inventory

```

## Limitations 

You do not have ssh access to the cluster so all customisations are limited to what can be done by the user
via the OpenShift API.


## Example Customisation






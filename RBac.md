```md
# Kubernetes Authentication Commands

Here I will write some authentication-related commands.

## Check Current User
```sh
kubectl auth whoami
```

## Check Permissions  
Check if the current user can get pods:  
```sh
kubectl auth can-i get pods
```

Check if the current user can get pods in a specific namespace (`apache`):  
```sh
kubectl auth can-i get pods -n apache
```

## Retrieve Roles and Service Accounts  
Get roles in the `apache` namespace:  
```sh
kubectl get role -n apache
```

Get service accounts in the `apache` namespace:  
```sh
kubectl get serviceaccount -n apache
```

## Check Permissions as Another User  
Check if `apache-user` can get pods in the `apache` namespace:  
```sh
kubectl auth can-i get pods -n apache --as=apache-user
```
```


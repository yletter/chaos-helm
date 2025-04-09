
Commands:
```
kubectl auth can-i get pods/log --as=pod-reader -n app
kubectl auth can-i create pods/exec --as=pod-reader -n app
kubectl auth can-i create pods --as=pod-reader -n app
kubectl auth can-i get pods --as=pod-reader --namespace=app

kubectl auth can-i get pods/log --as=pod-executor -n app
kubectl auth can-i create pods/exec --as=pod-executor -n app
kubectl auth can-i create pods --as=pod-executor -n app
kubectl auth can-i get pods --as=pod-executor --namespace=app

```

Output:
```
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i get pods/log --as=pod-reader -n app
yes
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i create pods/exec --as=pod-reader -n app
no
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i create pods --as=pod-reader -n app
no
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i get pods --as=pod-reader --namespace=app
yes

[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i get pods/log --as=pod-executor -n app
yes
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i create pods/exec --as=pod-executor -n app
yes
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i create pods --as=pod-executor -n app
yes
[cloudshell-user@ip-10-136-50-229 ~]$ kubectl auth can-i get pods --as=pod-executor --namespace=app
yes
[cloudshell-user@ip-10-136-50-229 ~]$ 

```

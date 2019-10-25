## mysql-client

Minimal environment with MySQL client:

* built on top of `gliderlabs/alpine` base image
* ~16 MB in size (5 MB base + 11 MB)

### Example usage:

```bash
$ docker run -it --rm jbergknoff/mysql-client mysql -h... -u... -p
Enter password: 
```

### Testing it on a k8s cluster

```
kubectl run mysqlc --rm --tty -i --restart='Never' --image sentenza/mysql-client --command -- /bin/bash
```
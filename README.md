# flux-infra

## bootstrapping with git repo or GITHUB repo
### git repo
```bash
flux bootstrap git --url=https://xxx.aaa.com/xxx/xxx/fluxcd.git --username=xxx --password=xxx --timeout=30m
```
### github repo
```bash
export GITHUB_TOKEN=<your-token>
flux bootstrap github \
  --owner=my-github-username \
  --repository=my-repository \
  --path=clusters/my-cluster \
  --personal
```

## create source definition in fluxv2 (one git repo that flux will use to sync manifests in it)
### enter into bootstrap git local repo(scratch-infra)
### exec like below
<img width="736" alt="截屏2022-11-26 17 29 31" src="https://user-images.githubusercontent.com/57861564/204081911-7ee3688d-6130-432e-a76e-997d40298442.png">
<img width="777" alt="截屏2022-11-26 17 30 29" src="https://user-images.githubusercontent.com/57861564/204081958-15570dee-f04d-462c-9a71-252616cbb000.png">

## create kustonization (define that the kubernetes.kustomization that in which dir should be deployed to the target k8s)
<img width="764" alt="截屏2022-11-26 17 36 26" src="https://user-images.githubusercontent.com/57861564/204082171-db609ff2-965c-4ed5-83ff-01109602231d.png">
<img width="734" alt="截屏2022-11-26 17 36 50" src="https://user-images.githubusercontent.com/57861564/204082182-5dadd1c9-1adf-49de-973a-615ddae2be39.png">
<img width="763" alt="截屏2022-11-26 17 37 42" src="https://user-images.githubusercontent.com/57861564/204082221-adc1a005-0569-4125-ae8d-33e378ce08fb.png">


## bootstrapping one cluster with existing flux system
<img width="1026" alt="截屏2022-11-26 17 19 32" src="https://user-images.githubusercontent.com/57861564/204081585-b16652ac-9cc7-4c5e-80e7-d917fd653b68.png">
<img width="1067" alt="截屏2022-11-26 17 20 33" src="https://user-images.githubusercontent.com/57861564/204081618-aad341dc-7586-4498-8d44-f4c90f1f6d0b.png">
<img width="1079" alt="截屏2022-11-26 17 21 44" src="https://user-images.githubusercontent.com/57861564/204081659-6509105f-92ca-41d9-b91a-8ea10b7819c1.png">
### trigger sync manually
<img width="1025" alt="截屏2022-11-26 17 22 40" src="https://user-images.githubusercontent.com/57861564/204081684-f03e832b-5916-4140-883e-2c3320f0b9d5.png">

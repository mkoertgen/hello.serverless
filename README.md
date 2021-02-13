# hello.serverless

Evaluating [serverless](https://github.com/serverless/serverless) for abstracting serverless deployments over various providers

## Installation

See [QuickStart](https://github.com/serverless/serverless#quick-start)

### Kubeless

#### Install

#### Example kubeless function

```shell
cd kubeless-nodejs
$ kubeless function deploy hello -r nodejs14 -d package.json -f handler.js --handler handler.capitalize
INFO[0000] Deploying function...
INFO[0000] Function hello submitted for deployment
INFO[0000] Check the deployment status executing 'kubeless function ls hello'


$ kubeless function ls
$ kubeless function ls
NAME    NAMESPACE       HANDLER                 RUNTIME         DEPENDENCIES                    STATUS
hello   kubeless        handler.capitalize      nodejs14        lodash: ^4.17.20                1/1 READY
                                                                serverless-kubeless: ^0.11.2

$ kubeless function call hello --data 'Hello world!'
...


$kubeless function delete hello
...
$kubectl get functions
...
```

## References

- [Get Started with Serverless Computing on Kubernetes with Minikube and Kubeless](https://docs.bitnami.com/tutorials/get-started-serverless-computing-kubeless/)
- [kubeless/kubeless](https://github.com/kubeless/kubeless)
- [kubeless quick-start](https://kubeless.io/docs/quick-start/)

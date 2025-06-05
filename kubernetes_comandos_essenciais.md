# 📘 Cheatsheet: Comandos Essenciais Kubernetes

Este documento contém os comandos mais usados no dia a dia com Kubernetes, com explicações claras para cada um deles.

## `kubectl cluster-info`
Exibe informações básicas sobre o cluster Kubernetes (API server, DNS, etc).

## `kubectl get pods -n NAMESPACE`
Lista todos os Pods rodando em um namespace específico.

## `kubectl get all -n NAMESPACE`
Lista todos os recursos (Pods, Services, Deployments etc) em um namespace.

## `kubectl describe pod NOME_DO_POD -n NAMESPACE`
Mostra detalhes e eventos de um Pod.

## `kubectl logs NOME_DO_POD -n NAMESPACE`
Exibe os logs do container principal de um Pod.

## `kubectl apply -f arquivo.yaml`
Cria ou atualiza recursos Kubernetes a partir de um manifesto YAML.

## `kubectl delete -f arquivo.yaml`
Remove os recursos definidos no arquivo YAML.

## `kubectl exec -it NOME_DO_POD -- bash`
Acessa o terminal do container principal em um Pod.

## `kubectl scale deployment NOME_DO_DEPLOYMENT --replicas=3 -n NAMESPACE`
Altera a quantidade de réplicas de um deployment.

## `kubectl get pods -o wide -n NAMESPACE`
Mostra detalhes adicionais dos Pods (IP, node, imagem etc).

## `kubectl get pod NOME_DO_POD -o wide -n NAMESPACE`
Exibe o node onde o Pod está rodando.

## `kubectl set image deployment/NOME_DEPLOYMENT NOME_CONTAINER=imagem:versao`
Atualiza a imagem de um container em um deployment.

## `kubectl run -it --rm --image=alpine test -- sh`
Cria um Pod temporário para testes com Alpine.

## `kubectl get secret -n NAMESPACE`
Lista os secrets do namespace.

## `kubectl get configmap -n NAMESPACE`
Lista os configmaps do namespace.

## `kubectl get events -n NAMESPACE --sort-by=.metadata.creationTimestamp`
Mostra eventos recentes ordenados por tempo.

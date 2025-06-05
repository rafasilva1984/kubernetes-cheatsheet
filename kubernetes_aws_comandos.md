# ☁️ Comandos Kubernetes em Ambiente AWS (EKS)

Comandos úteis para operar clusters Kubernetes rodando na AWS com EKS:

## `kubectl config get-contexts`
Lista os contextos disponíveis (útil ao usar vários clusters, como dev, stage e prod da AWS).

## `aws eks --region REGIAO update-kubeconfig --name NOME_DO_CLUSTER`
Atualiza o kubeconfig local com acesso ao cluster EKS da AWS.

## `kubectl get svc -n kube-system`
Verifica os serviços rodando no namespace de sistema, como CoreDNS e metrics-server.

## `kubectl get nodes -o wide`
Verifica quais nodes EC2 fazem parte do cluster.

## `kubectl describe node NOME_DO_NODE`
Mostra detalhes da instância EC2 associada ao node (útil para debug de scheduling).

## `kubectl get pods -n kube-system -o wide`
Lista os pods do sistema e mostra em quais nodes EC2 estão rodando.

## `kubectl get events --sort-by=.metadata.creationTimestamp`
Monitora eventos recentes, importante para detectar falhas de node/pod no EKS.

## `kubectl top nodes`
Mostra uso de CPU/memória por node (precisa do metrics-server instalado).

## `kubectl top pods --all-namespaces`
Mostra uso de recursos por Pod em todos os namespaces.

## `kubectl logs POD -n NAMESPACE`
Consulta logs de aplicações, comum em troubleshooting na AWS.

## `kubectl rollout status deployment/NOME -n NAMESPACE`
Verifica se um deployment (ex: backend) foi aplicado com sucesso no EKS.

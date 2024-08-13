#Arquitetura

### Requisitos arquiteturais
- Confiabilidade
- Segurança
- Otimização de Custo
- Desenpenho


### O AKS oferece os seguintes SLA:

|SLA |Garantia|Camada|
|----|--------|------|
|None|99.9%| Standard e Premium|
|Tempo de inatividade| 99.95%| Availabilite Zone|



### Camadas e SKUs:

| |Free Tier |Standard Tier| Premium|
|-------|----------|-------------|--------|
|when to use|Experiment, Learn, POC|production, Mission Critical, SLA| Production, Mission Critical, SLA, version Suport 2 years|
|types suported| Cluster or small scale, fewer 10 nodes| Enterprise or Production, up to 5000 nodes| Enterprise or Production, up to 5000 nodes|
|Pricing| Free cluster managment, pay for resources you consume|pay cluster managment, Pay resources consume.|more expansive cluster managment, Pay resources consume.|
|Feature Comparison | Recommended cluster with fewer then 10 nodes, but can suport up to 1000 nodes. Include all AKS features| Uptime SLA is enable by default, Greater cluster reliability and resources, suport up 5000 nodes in a cluster, include all current AKS feature.| Inclusde all current AKS Feature, Microsoft maintenance|



- **All tiers (free, standard, premium) are availiable in all region where aks is supported**

### Lista de verificações:
- Para cargas de trabalho criticas, use zonas de disponibilidade para seus clusters do AKS.
- Planeje o espali de endereço IP para garantit que o cluster possa ser dimensionado de forma confiavel, incluindo o tratamento de trafego de failover em topologias de varios clusters.
- Habilite os monitoramentos (container insights) para monitorar o cluster e configurar alertas e eventos que afetam a confiabilidade.
-  Verifique  se os workloads foram criadas para dar suporte ao dimensionamento.
- Verificar se o workload esta com o tamanho certo, verificar e avaliar o SKU a escolher. No minimo, inclua 2 nós para pools de nós de usuario e 3 nós para o pool de nós do sistema.
- Use SLA de tempo de atividade para atender as metas de disponibilidade.


### Recomendações de configuração
- Controle o a gendamento de podes utilizando seletores de afinidade.
- Garanta a seleção adequada do plug-in de rede com base nos requisitos de rede e no dimencionamento do cluster.
- Defina sempre os solicitações e limites de recursos de pod em manifestos de implantação de aplicativo e imponha com Azure Police. 
- Os pools de nós do sistema exigem uma SKU de pelo menos 2VCpu e 4GB de memoria, mas 4 VCPU ou mais são recomendados.
- 


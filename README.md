# Red Hat OpenShift Monitoring Cluster Resources

This repository was created out of the need to **monitor resources in Red Hat OpenShift clusters** in a customized way.

Monitoring OpenShift cluster resources using Grafana is essential to ensure the environment's performance, stability, and operational efficiency.

This practice offers several benefits:

* **Real-time visibility:** Grafana provides an intuitive visual interface that allows for real-time cluster metrics monitoring.
* **Problem detection and resolution:** Continuous monitoring helps identify potential issues before they impact services.
* **Enhanced operational efficiency:** Detailed monitoring allows for optimized resource usage.
* **Support for data-driven decision-making:** With Grafana, decisions on scalability and resource allocation can be made based on real data and accurate metrics.


## Lab - How to implement observability dashboards


```bash
oc create serviceaccount grafana-sa -n openshift-observability
```


```bash
oc adm policy add-cluster-role-to-user cluster-monitoring-view -z grafana-sa
```


```bash
oc serviceaccounts get-token grafana-sa -n openshift-observability
```


```bash
oc create token grafana-sa --duration=8760h -n openshift-observability
```


![](images/dashboard-views-nodes.png)


![](images/dashboard-views-nodes-list.png)
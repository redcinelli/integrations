# kube-scheduler

## Metrics

### scheduler

This is the `scheduler` dataset of the Kubernetes package. It collects metrics
from Kubernetes Scheduler component.

An example event for `scheduler` looks as following:

```json
{
    "kubernetes": {
        "scheduler": {
            "name": "DynamicConfigMapCABundle-client-ca",
            "workqueue": {
                "retries": {
                    "count": 0
                },
                "depth": {
                    "count": 0
                },
                "unfinished": {
                    "sec": 0
                },
                "longestrunning": {
                    "sec": 0
                },
                "adds": {
                    "count": 12
                }
            }
        }
    },
    "orchestrator": {
        "cluster": {
            "name": "kind",
            "url": "kind-control-plane:6443"
        }
    },
    "agent": {
        "name": "kind-control-plane",
        "id": "ee1d778a-e607-4c29-b152-f6e83e606966",
        "type": "metricbeat",
        "ephemeral_id": "084bb5dd-df70-4127-9a52-47fae69de446",
        "version": "8.7.0"
    },
    "@timestamp": "2023-01-10T15:10:33.424Z",
    "ecs": {
        "version": "8.0.0"
    },
    "data_stream": {
        "namespace": "default",
        "type": "metrics",
        "dataset": "kubernetes.scheduler"
    },
    "service": {
        "address": "https://0.0.0.0:10259/metrics",
        "type": "kubernetes"
    },
    "elastic_agent": {
        "id": "ee1d778a-e607-4c29-b152-f6e83e606966",
        "version": "8.7.0",
        "snapshot": true
    },
    "host": {
        "hostname": "kind-control-plane",
        "os": {
            "kernel": "5.15.49-linuxkit",
            "codename": "focal",
            "name": "Ubuntu",
            "type": "linux",
            "family": "debian",
            "version": "20.04.5 LTS (Focal Fossa)",
            "platform": "ubuntu"
        },
        "ip": [
            "10.244.0.1",
            "10.244.0.1",
            "10.244.0.1",
            "172.20.0.2",
            "172.18.0.2",
            "fc00:f853:ccd:e793::2",
            "fe80::42:acff:fe12:2"
        ],
        "containerized": false,
        "name": "kind-control-plane",
        "id": "1c1d736687984c73b6a5f77c1464d4da",
        "mac": [
            "02-42-AC-12-00-02",
            "02-42-AC-14-00-02",
            "6E-87-97-B3-C4-A1",
            "7E-2B-73-DA-CF-B7",
            "F2-54-31-F4-76-AB"
        ],
        "architecture": "x86_64"
    },
    "metricset": {
        "period": 10000,
        "name": "scheduler"
    },
    "event": {
        "duration": 21808836,
        "agent_id_status": "verified",
        "ingested": "2023-01-10T15:10:37Z",
        "module": "kubernetes",
        "dataset": "kubernetes.scheduler"
    }
}
```

**Exported fields**

| Field | Description | Type | Unit | Metric Type |
|---|---|---|---|---|
| @timestamp | Event timestamp. | date |  |  |
| cloud.account.id | The cloud account or organization id used to identify different entities in a multi-tenant environment. Examples: AWS account id, Google Cloud ORG Id, or other unique identifier. | keyword |  |  |
| cloud.availability_zone | Availability zone in which this host is running. | keyword |  |  |
| cloud.image.id | Image ID for the cloud instance. | keyword |  |  |
| cloud.instance.id | Instance ID of the host machine. | keyword |  |  |
| cloud.instance.name | Instance name of the host machine. | keyword |  |  |
| cloud.machine.type | Machine type of the host machine. | keyword |  |  |
| cloud.project.id | Name of the project in Google Cloud. | keyword |  |  |
| cloud.provider | Name of the cloud provider. Example values are aws, azure, gcp, or digitalocean. | keyword |  |  |
| cloud.region | Region in which this host is running. | keyword |  |  |
| container.id | Unique container id. | keyword |  |  |
| container.image.name | Name of the image the container was built on. | keyword |  |  |
| container.labels | Image labels. | object |  |  |
| container.name | Container name. | keyword |  |  |
| data_stream.dataset | Data stream dataset. | constant_keyword |  |  |
| data_stream.namespace | Data stream namespace. | constant_keyword |  |  |
| data_stream.type | Data stream type. | constant_keyword |  |  |
| ecs.version | ECS version this event conforms to. `ecs.version` is a required field and must exist in all events. When querying across multiple indices -- which may conform to slightly different ECS versions -- this field lets integrations adjust to the schema version of the events. | keyword |  |  |
| host.architecture | Operating system architecture. | keyword |  |  |
| host.containerized | If the host is a container. | boolean |  |  |
| host.domain | Name of the domain of which the host is a member. For example, on Windows this could be the host's Active Directory domain or NetBIOS domain name. For Linux this could be the domain of the host's LDAP provider. | keyword |  |  |
| host.hostname | Hostname of the host. It normally contains what the `hostname` command returns on the host machine. | keyword |  |  |
| host.id | Unique host id. As hostname is not always unique, use values that are meaningful in your environment. Example: The current usage of `beat.name`. | keyword |  |  |
| host.ip | Host ip addresses. | ip |  |  |
| host.mac | Host mac addresses. | keyword |  |  |
| host.name | Name of the host. It can contain what `hostname` returns on Unix systems, the fully qualified domain name, or a name specified by the user. The sender decides which value to use. | keyword |  |  |
| host.os.build | OS build information. | keyword |  |  |
| host.os.codename | OS codename, if any. | keyword |  |  |
| host.os.family | OS family (such as redhat, debian, freebsd, windows). | keyword |  |  |
| host.os.kernel | Operating system kernel version as a raw string. | keyword |  |  |
| host.os.name | Operating system name, without the version. | keyword |  |  |
| host.os.name.text | Multi-field of `host.os.name`. | text |  |  |
| host.os.platform | Operating system platform (such centos, ubuntu, windows). | keyword |  |  |
| host.os.version | Operating system version as a raw string. | keyword |  |  |
| host.type | Type of host. For Cloud providers this can be the machine type like `t2.medium`. If vm, this could be the container, for example, or other information meaningful in your environment. | keyword |  |  |
| kubernetes.annotations.\* | Kubernetes annotations map | object |  |  |
| kubernetes.container.image | Kubernetes container image | keyword |  |  |
| kubernetes.container.name | Kubernetes container name | keyword |  |  |
| kubernetes.deployment.name | Kubernetes deployment name | keyword |  |  |
| kubernetes.labels.\* | Kubernetes labels map | object |  |  |
| kubernetes.namespace | Kubernetes namespace | keyword |  |  |
| kubernetes.node.hostname | Kubernetes hostname as reported by the node’s kernel | keyword |  |  |
| kubernetes.node.name | Kubernetes node name | keyword |  |  |
| kubernetes.pod.ip | Kubernetes pod IP | ip |  |  |
| kubernetes.pod.name | Kubernetes pod name | keyword |  |  |
| kubernetes.pod.uid | Kubernetes pod UID | keyword |  |  |
| kubernetes.replicaset.name | Kubernetes replicaset name | keyword |  |  |
| kubernetes.scheduler.client.request.count | Number of HTTP requests to API server, broken down by status code, method and host | long |  | counter |
| kubernetes.scheduler.client.request.duration.us.bucket.\* | Requests latency distribution in histogram buckets, broken down by verb and host | object |  |  |
| kubernetes.scheduler.client.request.duration.us.count | Number of request duration operations to API server, broken down by verb and host | long |  | counter |
| kubernetes.scheduler.client.request.duration.us.sum | Sum of requests latency in microseconds, broken down by verb and host | long | micros | counter |
| kubernetes.scheduler.client.request.size.bytes.bucket.\* | Requests size distribution in histogram buckets, broken down by verb and host | object |  |  |
| kubernetes.scheduler.client.request.size.bytes.count | Number of requests, broken down by verb and host | long |  | counter |
| kubernetes.scheduler.client.request.size.bytes.sum | Requests size sum in bytes, broken down by verb and host | long | byte | counter |
| kubernetes.scheduler.client.response.size.bytes.bucket.\* | Responses size distribution in histogram buckets, broken down by verb and host | object |  |  |
| kubernetes.scheduler.client.response.size.bytes.count | Number of responses, broken down by verb and host | long |  | counter |
| kubernetes.scheduler.client.response.size.bytes.sum | Responses size sum in bytes, broken down by verb and host | long | byte | counter |
| kubernetes.scheduler.code | HTTP code | keyword |  |  |
| kubernetes.scheduler.event | Scheduling event | keyword |  |  |
| kubernetes.scheduler.host | HTTP host | keyword |  |  |
| kubernetes.scheduler.leader.is_master | Whether the scheduler instance is leader | boolean |  |  |
| kubernetes.scheduler.method | HTTP method | keyword |  |  |
| kubernetes.scheduler.name | Name for the resource | keyword |  |  |
| kubernetes.scheduler.process.cpu.sec | Total user and system CPU time spent in seconds | double |  | counter |
| kubernetes.scheduler.process.fds.max.count | Limit for open file descriptors | long |  | gauge |
| kubernetes.scheduler.process.fds.open.count | Number of open file descriptors | long |  | gauge |
| kubernetes.scheduler.process.memory.resident.bytes | Bytes in resident memory | long | byte | gauge |
| kubernetes.scheduler.process.memory.virtual.bytes | Bytes in virtual memory | long | byte | gauge |
| kubernetes.scheduler.process.started.sec | Start time of the process since unix epoch in seconds | double |  | gauge |
| kubernetes.scheduler.profile | Scheduling profile | keyword |  |  |
| kubernetes.scheduler.queue | Scheduling queue | keyword |  |  |
| kubernetes.scheduler.result | Attempt result to schedule pod | keyword |  |  |
| kubernetes.scheduler.scheduling.attempts.duration.us.bucket.\* | Scheduling attempt latency distribution in histogram buckets, broken down by profile and result | object |  |  |
| kubernetes.scheduler.scheduling.attempts.duration.us.count | Number of scheduling attempts, broken down by profile and result | long |  | counter |
| kubernetes.scheduler.scheduling.attempts.duration.us.sum | Sum of scheduling attempt latency in microseconds, broken down by profile and result | long | micros | counter |
| kubernetes.scheduler.scheduling.pending.pods.count | Number of current pending pods, broken down by the queue type | long |  | gauge |
| kubernetes.scheduler.scheduling.preemption.attempts.count | Total preemption attempts in the cluster so far | long |  | counter |
| kubernetes.scheduler.scheduling.preemption.victims.bucket.\* | Number of preemption victims distribution in histogram buckets | object |  |  |
| kubernetes.scheduler.scheduling.preemption.victims.count | Number of preemption victims | long |  | counter |
| kubernetes.scheduler.scheduling.preemption.victims.sum | Preemption victims sum | long |  | counter |
| kubernetes.scheduler.verb | HTTP verb | keyword |  |  |
| kubernetes.scheduler.workqueue.adds.count | Workqueue add count, broken down by workqueue name | long |  | counter |
| kubernetes.scheduler.workqueue.depth.count | Workqueue current depth, broken down by workqueue name | long |  | gauge |
| kubernetes.scheduler.workqueue.longestrunning.sec | How many seconds has the longest running processor been running, broken down by workqueue name | double |  | gauge |
| kubernetes.scheduler.workqueue.retries.count | Workqueue number of retries, broken down by workqueue name | long |  | counter |
| kubernetes.scheduler.workqueue.unfinished.sec | How many seconds of work has done that is in progress and hasn't been considered in the longest running processor, broken down by workqueue name | double |  | gauge |
| kubernetes.selectors.\* | Kubernetes Service selectors map | object |  |  |
| kubernetes.statefulset.name | Kubernetes statefulset name | keyword |  |  |
| orchestrator.cluster.name | Name of the cluster. | keyword |  |  |
| orchestrator.cluster.url | URL of the API used to manage the cluster. | keyword |  |  |
| service.address | Address where data about this service was collected from. This should be a URI, network address (ipv4:port or [ipv6]:port) or a resource path (sockets). | keyword |  |  |
| service.type | The type of the service data is collected from. The type can be used to group and correlate logs and metrics from one service type. Example: If logs or metrics are collected from Elasticsearch, `service.type` would be `elasticsearch`. | keyword |  |  |

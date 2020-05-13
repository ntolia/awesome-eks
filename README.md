![EKS logo](images/eks-logo.png)

A curated list of awesome tools for Amazon EKS 🌊

Want to add something? Open a PR! 🙂

## What is EKS
Amazon Elastic Kubernetes Service (Amazon EKS) is a managed service that makes it easy for you to run Kubernetes on AWS without needing to stand up or maintain your own Kubernetes control plane. Kubernetes is an open-source system for automating the deployment, scaling, and management of containerized applications.

Amazon EKS runs Kubernetes control plane instances across multiple Availability Zone to ensure high availability. Amazon EKS automatically detects and replaces unhealthy control plane instances, and it provides automated version upgrades and patching for them.

Amazon EKS runs up-to-date versions of the open-source Kubernetes software, so you can use all the existing plugins and tooling from the Kubernetes community. Applications running on Amazon EKS are fully compatible with applications running on any standard Kubernetes environment, whether running in on-premises data centers or public clouds. This means that you can easily migrate any standard Kubernetes application to Amazon EKS without any code modification required.


## Table of content
- [Cluster management tools](#cluster-management-tools)
- [Data plane management](#data-plane-management)
- [CLI tools](#cli-tools)
- [Package managers](#package-managers)
- [Security](#security)
- [Networking](#networking)
- [Compliance](#compliance)
- [Container runtime security](#container-runtime-security)
- [Audit](#audit)
- [Monitoring](#monitoring)
- [Logging](#logging)
- [Tracing](#tracing)
- [CI and CD tools](#ci-and-cd-tools)
- [Scaling](#scaling)
- [Chaos testing](#chaos-testing)
- [Storage](#storage)
- [Ingress](#ingress)
- [API gateways](#api-gateways)
- [Service meshes](#service-meshes)
- [Backup](#backup)
- [Cost allocation](#cost-allocation)
- [Machine learning](#machine-learning)
- [Self-paced learning](#self-paced-learning)
- [Miscellaneous](#miscellaneous)
- [re:Invent 2019 sessions](#re-invent-2019-sessions)
- [Twitter](#twitter)
- [Books](#books)
- [Contributors](#contributors)

---


## Cluster management tools

* [eksctl](https://eksctl.io)
* [AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)
* [CDK Amazon EKS Construct Library](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-eks-readme.html)
* [Terraform](https://www.terraform.io/docs/providers/aws/guides/eks-getting-started.html)
* [Pulumi](https://www.pulumi.com/docs/tutorials/kubernetes/eks/)
* [Octant](https://github.com/vmware-tanzu/octant) - A highly extensible platform for developers to better understand the complexity of Kubernetes clusters.

## Data plane management
* [Managed nodes groups](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html)
* [AWS Node Termination Handler](https://github.com/aws/aws-node-termination-handler)

## CLI tools
* [Krew](https://krew.sigs.k8s.io) - a plugin manager for kubectl
* [kubectl-plugins](https://github.com/jordanwilson230/kubectl-plugins)
* [kubectx](https://github.com/ahmetb/kubectx) — Faster way to switch between clusters and namespaces in kubectl 
* [kui](https://github.com/IBM/kui/) - A hybrid command-line/UI development experience for cloud-native development

## Package managers
* [Helm](http://helm.sh) - The Kubernetes Package Manager

## Security
* [Using EKS encryption provider support for defense-in-depth](https://aws.amazon.com/blogs/containers/using-eks-encryption-provider-support-for-defense-in-depth/)
* [Bane](https://github.com/genuinetools/bane) - Custom & better AppArmor profile generator for Docker containers.
* [IAM Roles for service accounts](https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html)
* [eksuser](https://github.com/prabhatsharma/eksuser/) - Utility to manage Amazon EKS users
* [Sysdig Falco](https://sysdig.com/opensource/falco/)
* [cert-manager](https://github.com/jetstack/cert-manager) — Automatically provision and manage TLS certificates in Kubernetes
* [Pod security policy](https://docs.aws.amazon.com/eks/latest/userguide/pod-security-policy.html)

## Networking
* [AWS VPC CNI](https://github.com/aws/amazon-vpc-cni-k8s)
* [CNI metrics helper](https://docs.aws.amazon.com/eks/latest/userguide/cni-metrics-helper.html)
* [Calico network policy engine for Kubernetes](https://docs.aws.amazon.com/eks/latest/userguide/calico.html)
* [Cluster VPC considerations](https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html)
* [ksniff](https://github.com/eldadru/ksniff) - Kubectl plugin to ease sniffing on kubernetes pods using tcpdump and wireshark


## Compliance
* [kube-bench](https://github.com/aquasecurity/kube-bench)
* [docker-bench-security](https://github.com/docker/docker-bench-security)
* [actuary](https://github.com/diogomonica/actuary)
* [AWS Inspector](https://aws.amazon.com/inspector/)
* [Sysdig Secure](https://sysdig.com/products/kubernetes-security/)

## Container runtime security
* [Aqua](https://www.aquasec.com/products/aqua-cloud-native-security-platform/)
* [Qualys](https://www.qualys.com/apps/container-security/)
* [Amazon ECR container image scanning](https://docs.aws.amazon.com/AmazonECR/latest/userguide/image-scanning.html)
* [Twistlock](https://www.twistlock.com/platform/runtime-defense/)

## Audit
* [Logging Amazon EKS API calls with AWS CloudTrail](https://docs.aws.amazon.com/eks/latest/userguide/logging-using-cloudtrail.html)
* [kubeaudit](https://github.com/Shopify/kubeaudit)
* [MKIT](https://github.com/darkbitio/mkit)
* [kubesec.io](https://kubesec.io/)
* [polaris](https://github.com/FairwindsOps/polaris)

## Monitoring
* [Kubernetes Metrics Server](https://github.com/kubernetes-sigs/metrics-server) — Cluster-wide aggregator of resource usage data
* [kube-state-metrics](https://github.com/kubernetes/kube-state-metrics) — Add-on agent to generate and expose cluster-level metrics.
* Prometheus + Grafana
* [CloudWatch Container Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ContainerInsights.html)
* [Using Prometheus Metrics in Amazon CloudWatch](https://aws.amazon.com/blogs/containers/using-prometheus-metrics-in-amazon-cloudwatch/)

## Logging
* [Amazon EKS control plane logging](https://docs.aws.amazon.com/eks/latest/userguide/control-plane-logs.html)
* [Fluentd](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-logs.html) — Set Up FluentD as a DaemonSet to Send Logs to CloudWatch Logs
* [Kubernetes Logging powered by AWS for Fluent Bit](https://aws.amazon.com/blogs/containers/kubernetes-logging-powered-by-aws-for-fluent-bit/)
* [Cloudwatch Container Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-EKS-quickstart.html)

## Tracing
* [AWS X-Ray](https://aws.amazon.com/xray/)
* [Jaeger](https://github.com/jaegertracing/jaeger)

## CI & CD tools
* [Flux](https://github.com/fluxcd/flux) - The GitOps Kubernetes operator
* [Flagger](https://flagger.app) - Progressive Delivery Operator for Kubernetes
* Jenkins
* Travis
* Circle CI
* Gitlab
* Shippable

## Scaling
* [Goldilocks vertical-pod-autoscaler](https://github.com/FairwindsOps/goldilocks/)
* [kube-metrics-adapter](https://github.com/zalando-incubator/kube-metrics-adapter)
* [right-size-guide](https://github.com/mhausenblas/right-size-guide) — A CLI tool providing memory & CPU recommendations for containerized apps

## Chaos testing
* [Chaos Mesh](https://github.com/pingcap/chaos-mesh)
* [PowerfulSeal](https://github.com/bloomberg/powerfulseal)

## Storage
* [Amazon EBS CSI driver](https://github.com/kubernetes-sigs/aws-ebs-csi-driver)
* [Amazon EFS CSI driver](https://github.com/kubernetes-sigs/aws-efs-csi-driver)
* [Amazon FSx for Lustre CSI driver](https://github.com/kubernetes-sigs/aws-fsx-csi-driver)

## Ingress 
* [ALB Ingress Controller](https://github.com/kubernetes-sigs/aws-alb-ingress-controller) - AWS ALB Ingress Controller for Kubernetes
* [Gloo](https://github.com/solo-io/gloo) - The Feature-rich, Kubernetes-native, Next-Generation API Gateway Built on Envoy
* [Traefik](https://containo.us/traefik/) — Cloud Native Edge Router

## API gateways
* [Ambassador](https://github.com/datawire/ambassador)
* [Kong](https://github.com/Kong/kong)
* [Amazon API Gateway](https://aws.amazon.com/blogs/containers/api-gateway-as-an-ingress-controller-for-eks/)

## Service meshes
* [AppMesh](https://aws.amazon.com/app-mesh/)
* [Istio](http://istio.io)
* [Linkderd](http://linkerd.io)
* [Consul](http://consul.io)

## Backup
* [Velero](https://velero.io)

## Cost allocation
* [Ocean by spot.io](https://eksworkshop.com/beginner/190_ocean/showback/)
* [kubecost](https://kubecost.com)
* [Kubernetes Opex Analytics](https://github.com/rchakode/kube-opex-analytics)


## Machine learning
* [Kubeflow](https://github.com/kubeflow/kubeflow) — Machine Learning Toolkit for Kubernetes
* [Optimizing Spark performance on Kubernetes](https://aws.amazon.com/blogs/containers/optimizing-spark-performance-on-kubernetes/)
* [__Video__ AWS re:Invent 2019: Building machine-learning infrastructure on Amazon EKS with Kubeflow (CON306-R1)](https://www.youtube.com/watch?v=ULlqukKVKBo)

## Self-paced learning
* [EKS Workshop](https://eksworkshop.com)

## Miscellaneous 
* [AWS container services roadmap](https://github.com/aws/containers-roadmap/projects/1)
* [Container content ideas for AWS](https://github.com/awslabs/container-content-ideas-for-aws/projects/1)
* [Amazon EKS Kubernetes versions](https://docs.aws.amazon.com/eks/latest/userguide/kubernetes-versions.html#kubernetes-1.16)
* [Windows support](https://docs.aws.amazon.com/eks/latest/userguide/windows-support.html)
* [ARM Support](https://docs.aws.amazon.com/eks/latest/userguide/arm-support.html)
* [Amazon EKS on AWS Outposts](https://docs.aws.amazon.com/eks/latest/userguide/eks-on-outposts.html)

## re:Invent 2019 sessions
* [AWS re:Invent 2019: Running Kubernetes at Amazon scale using Amazon EKS (CON212-R1)](https://www.youtube.com/watch?v=M-Fh0OzliJI)
* [AWS re:Invent 2019: Running Kubernetes Applications on AWS Fargate (CON326-R1)](https://www.youtube.com/watch?v=m-3tMXmWWQw)
* [AWS re:Invent 2019: Amazon EKS under the hood (CON421-R1)](https://www.youtube.com/watch?v=7vxDWDD2YnM)
* [AWS re:Invent 2019: Building machine-learning infrastructure on Amazon EKS with Kubeflow (CON306-R1)](https://www.youtube.com/watch?v=ULlqukKVKBo)


## Twitter
* [Nathan Peck](https://twitter.com/nathankpeck) - AWS Developer Advocate
* [Massimo Re Ferre'](https://twitter.com/mreferre) - AWS Developer Advocate
* [Michael Hausenblas](https://twitter.com/mhausenblas) - AWS Developer Advocate

## Books
* Container Security by Liz Rice
* Kubernetes Patterns by Roland Huß
* Kubernetes Best Practices by Lachlan Evenson, Dave Strebel, Eddie Villalba, Brendan Burns
* Programming Kubernetes by Michael Hausenblas
* Kubernetes Cookbook by Sébastien Goasguen and Michael Hausenblas
* Mastering Kubernetes by Gigi Sayfan

## Contributors
[@realvz](https://twitter.com/realz)


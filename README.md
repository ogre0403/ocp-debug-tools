# OCP-Debug-Tools

This is a kubectl plugin for capture packet using tcpdump in OpenShift. 

`NOTE:` This plugin is only tested in OCP. 


## Install

Copy `kubectl-tcpdump_node` & `kubectl-tcpdump_pod` into $PATH. 


## Usage

* TCPDUMP for node interface
    ```
    $ oc tcpdump-node -h <NODE> -i <INTERFACE> [ -t <TO-NAMESAPCE> ]
    ```
    If pods are located on `different` node, capture primary interface packet can get useful information. 

    If pods are located on `the same` node, capture `tun0` interface. This will includes pod ip and svc ip information. 

* TCPDUMP for Pod

    ```
    $ oc tcpdump-pod -n <NAMESPACE> -p <POD>  [ -t <TO-NAMESAPCE> ]
    ```


## Reference
1. [tcpdump from a RHEL CoreOS OpenShift node](https://access.redhat.com/solutions/5074041)
2. [tcpdump inside OpenShift v4 Pod](https://access.redhat.com/solutions/4569211)
3. [Collecting a tcpdump from a pod
](https://openshift.ktz.cloud/troubleshooting/collect-tcpdump/)





path-kubernetes

This is the k8s configuration for deploying NVIDIA Triton on the PATh facility.

General Notes:

    Because PATh runs OSPool jobs on the same hardware. Replicas need to be incremented slowly, i.e. one needs to change replica acount from 1->2->3->..., to allow for the OSPool jobs to be evicted. If you don't do that the cluster will claim it doesn't have the resources. Incrementing the replica count will give k8s to evict the OSPool jobs.

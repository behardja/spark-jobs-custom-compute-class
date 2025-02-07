# spark-jobs-custom-compute-class

## Objective

The contents of this repo includes notebooks meant to test custom compute classes on GKE for Spark workloads. Execute Spark workloads on a GKE cluster that uses custom compute classes. Users would define ComputeClass.yaml with a list of resource preferences. GKE would attempt to fulfill resources according to this list (e.g. L4 > T4 > CPU), and when a preferred resource is unavailable, a fallback strategy would shift to the next suitable resource. Custom Compute Class is set as the default for the namespace that runs the spark workload.

The demo notebooks were designed to be run in sequence.

## Getting started
Refer and navigate to the sections:
- **Build image to run and submit Apache Spark applications on Kubernetes**
    * [00_build_spark_images.ipynb](./00_build_spark_images.ipynb): Notebook builds images to run and submit Apache Spark applications on Kubernetes. Steps include downloading files from Nvidia and Spark into a local src/ folder. In this example, no operators are required.
- **Spark workloads Executed using GKE Custom Compute Classes**
    * [01_vertex_gke_custom_compute_job.ipynb](./01_vertex_gke_custom_compute_job.ipynb) : Notebook that demonstrate creation of a GKE cluster, defines custom compute classes, and submits the workload.
    
    
## References

Resources:
## Additional References
* [About Custom Compute Classes](https://cloud.google.com/kubernetes-engine/docs/concepts/about-custom-compute-classes)
* [Running Spark on Kubernetes](https://spark.apache.org/docs/latest/running-on-kubernetes.html)
* [Getting Started with RAPIDS and Kubernetes](https://docs.nvidia.com/ai-enterprise/deployment-guide-spark-rapids-accelerator/0.1.0/kubernetes.html)
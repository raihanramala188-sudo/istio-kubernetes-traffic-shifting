# Istio Kubernetes Traffic Shifting



## Project Overview



This project demonstrates traffic management using Istio and Kubernetes through the Bookinfo sample application.



The objective is to implement traffic shifting between two versions of the Reviews service using Istio VirtualServices.



## Technologies Used



- Kubernetes

- Minikube

- Istio Service Mesh

- YAML

- PowerShell



## Project Objectives



- Understand Istio VirtualServices and DestinationRules.

- Configure traffic routing between application versions.

- Implement weighted traffic shifting.

- Test traffic distribution using HTTP requests.

- Understand Canary Deployments.



## Traffic Shifting Implementation



| Stage | Reviews v1 | Reviews v2 |

|---|---|---|

| 1 | 80% | 20% |

| 2 | 50% | 50% |

| 3 | 20% | 80% |

| 4 | 0% | 100% |



## Testing



Traffic distribution was tested by sending 20 HTTP requests to the Bookinfo product page.



Final test result:



- Reviews v1: 0 requests

- Reviews v2: 20 requests



All 20 requests were served by Reviews v2 in the final test.



## How Traffic Shifting Works



An Istio VirtualService defines how traffic is routed to different service subsets.



A DestinationRule defines subsets such as v1 and v2 using Kubernetes workload labels.



Traffic weights determine the proportion of requests routed to each subset.



This technique is commonly used in Canary Deployments to gradually introduce a new application version.



## Author



Mohamed Ramalaawie



MSc Data Engineering for Artificial Intelligence



Data ScienceTech Institute (DSTI), France



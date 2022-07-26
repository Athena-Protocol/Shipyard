#Athena Protocol Shipyard Grant Milestone 2-4 Submission#
---



[See the Project Master Doc for a more in depth description of this phase of our development.](https://docs.google.com/document/d/1x0ZD3mcTe9pJD9TnN0ufBMbk5Zj9ZTatD5TTlHJj6ns/edit?usp=sharing)

[See the Milestone Timeline For an updated projection of our deliverables from now until July 15th ](https://docs.google.com/spreadsheets/d/1VQMLs-ONgZZUVKIQaUMwMlbsIjY73pPVB-AxtxIiIow/edit?usp=sharing)

Overview

Provider / Operator 
Our Team encountered several challenges while configuring the Operator & Provider that extended development time, namely;

1. The choice to run our test using the Ocean Market Place introduced issues with the UI that required work around. The most important of which is that Free Assets are not usable with Compute to data. Issues are being created by Spirinova over the next few days.
2. The recent exploit and subsequent changes made to the Ocean Market regarding liquidity pools required a redesign of our admin panel, marketplace, and the design of our credentials and accreditation procedure.

As of 2022/07/05 we have a successfully configured our servers to run operator and provider which;

1. Automate the deployment of Operator clusters using minikube. 
2. Runs configured with a local IPFS node
3. Successfully executes a C2d job using local configuration of Operator & Provider , and Ocean Protocol Foundations Aquarius 

* Complete
 * [Scope signed claims and credentials](https://docs.google.com/document/d/1Qw80dr4oZY4Mr6omlCsfPwbcSgHVO82jUCq3A_ZMGuo/edit?usp=sharing)
 * Minikube Cluster Deployment
 * [PFS Hosting](http://15.206.100.41:5001/webui)
 * Set Up Provider
 * Configure Local Provider With Local Operator 
 * Run successful c2d using local components
    
* In Progress
  * Admin Panel- Undergoing redesign due to the removal of liquidity pools. 
  * Using Provider/encrypt endpoint for IPFS file content Encrypt/ Decrypt 
  * Design & Implement Signed Claims
    * We experienced some set backs with the design process after the recent decision to remove liquidity pools to prevent further exploits. 


## Operating Athena Middelware 


[Configured Market Fork](http://15.206.100.41:8000/)

[Provider](http://15.206.100.41:8030/)

*Operator* : Minikube Dashboard

1. Execute below step in your command line –

ssh -i c2d-mumbai.pem -L 8081:localhost:<port> ubuntu@15.206.100.41

To get the port number you will have to execute this in EC2 -
minikube dashboard –url

2. Once done –

http://127.0.0.1:8081/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-
dashboard:/proxy/#/pod?namespace=_all

We will later put this in Kubernetes so it can be directly accessible.





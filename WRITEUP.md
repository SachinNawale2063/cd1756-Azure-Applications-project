# Write-up  

### Analyze, choose, and justify the appropriate resource option for deploying the app.  

**Virtual Machine (VM):**  
- **Cost:** Running a VM incurs higher costs because you pay for the compute instance continuously, whether the app is used heavily or not. You are also responsible for managing OS updates, security patches, and scaling.  
- **Scalability:** Scaling on a VM is manual and requires provisioning additional instances or upgrading the VM size. This can be time-consuming and less flexible compared to App Service.  
- **Availability:** Availability depends on how the VM is configured. For high availability, you must manually configure load balancers and multiple VM instances, increasing complexity and cost.  
- **Workflow:** A VM gives you complete control over the environment, but deployment, monitoring, and updates are more complex and require additional DevOps overhead.  

**App Service:**  
- **Cost:** App Service is cost-effective because it offers consumption-based or tiered pricing. You only pay for what you use, and infrastructure management is handled by Azure.  
- **Scalability:** Scaling is simple and can be done automatically with autoscaling rules. Horizontal and vertical scaling are supported with minimal effort.  
- **Availability:** Azure App Service provides built-in high availability and manages redundancy without requiring extra configuration.  
- **Workflow:** The workflow is streamlined with integrated deployment slots, CI/CD support, and simplified management, allowing faster development and release cycles without managing infrastructure.  

**Chosen Solution – App Service:**  
I chose **App Service** because it is more cost-efficient, provides built-in scalability, and ensures high availability out of the box. It also simplifies the deployment workflow by eliminating the need for manual server management, making it an ideal solution for the CMS app. Compared to VMs, App Service reduces operational overhead and allows developers to focus on the application rather than infrastructure management.  

---

### Assess app changes that would change your decision.  

If the application required more control over the underlying infrastructure (such as installing custom software, managing OS-level dependencies, or handling non-standard configurations), then a **VM** would be more suitable. Similarly, if the app needed specialized networking setups, complex background services, or legacy software compatibility, shifting to a VM might be required.  

Additionally, if the CMS app were to evolve into a system with high-performance computing needs or stateful workloads not easily managed by App Service, using a VM could provide more flexibility. In such cases, the infrastructure control offered by VMs would outweigh the ease and automation provided by App Service.  

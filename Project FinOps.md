# "Hey there! 
# I’m Dhanesh Kumar, a DevSecOps and Cybersecurity Analyst.
### Think of this GitHub profile as a live look into my digital workshop. Right now, I’m focused on building automated, secure-by-design deployment pipelines.
### I bridge the gap between development and security—meaning I don't just build pipelines to ship code faster, I make sure they are bulletproof against vulnerabilities and optimized to save cloud costs.
<img width="1408" height="768" alt="Gemini_Generated_Image_d1u2xqd1u2xqd1u2" src="https://github.com/user-attachments/assets/573fa6d2-ebb2-470d-8597-f6b17ed6c105" />

## Section 1: PLAN  Create a Kanban project in Jira
<img width="1909" height="818" alt="image" src="https://github.com/user-attachments/assets/8217b14d-edc3-46d9-905c-6467c0d5bb80" />

### FIN-101: Define Corporate FinOps Compliance Policy and DevSecOps Pipeline Security Gates

### Description:

- [ ] **Requirement 1:** Staging deployments must carry the label 'tier=non-prod' to be targeted for cost optimization.
- [ ] **Requirement 2:** Integrate security scanning checkpoints (SonarQube SAST, Trivy Container/SCA, GitGuardian Secrets) into the automation engine.
- [ ] **Requirement 3:** Enforce Java Maven compilation and TestNG validation gates.

## Section 2 : CODE Transition to Phase 2 
### Now that Jira shows the task is active, your engineering responsibility is to write the code that matches this ticket.
### Lets use Powershell and execute these commands to build your corporate folder structure and initialize your Git repository
<img width="794" height="230" alt="image" src="https://github.com/user-attachments/assets/364eaea5-75c2-4717-b0de-e1606616b8f4" />

### Part 1: Initializing Version Control and Developer Identity
### We used Git to spin up a secure, empty tracking database directly on our local laptop to ensure absolute code version traceability.
### ▪ git init - This command created a hidden database folder on the laptop to watch file changes live.
### ▪ git config --global user.name - This operation securely signs every code update with your verified corporate engineer identity.
<img width="1000" height="275" alt="image" src="https://github.com/user-attachments/assets/04969708-f89d-4d53-ad3e-0e8f4db99a61" />


### Part 2: Constructing the Modular Directory Framework
### We built isolated workspace directories to decouple our infrastructure automated backend engine from user-facing application services.
### ▪ New-Item -ItemType Directory - This command generated our structured microservices layout for separate frontend and backend deployment.
### ▪ Get-ChildItem - This verification operation displays our fresh directory tree structure to prove that all workspace folders are created.
<img width="1000" height="464" alt="image" src="https://github.com/user-attachments/assets/ec1086a1-cd25-4a42-8347-beaa3cfbb8a2" />

### Part 3: Engineering the Core FinOps Engine File
### We injected our automated Python script directly into the cluster optimizer folder to programmatically control scaling workflows.

```powershell
# Write the FinOps optimization engine script
@'
import os
from kubernetes import client, config

def scale_staging_environments():
    try:
        config.load_incluster_config()
    except config.ConfigException:
        config.load_kube_config()

    apps_v1 = client.AppsV1Api()
    print("[FINOPS] Scanning cluster namespaces for idle environments...")
    deployments = apps_v1.list_namespaced_deployment(namespace="staging")
    
    saved_cores = 0
    for dep in deployments.items:
        labels = dep.metadata.labels or {}
        if labels.get("tier") == "non-prod":
            name = dep.metadata.name
            print(f"[FINOPS-ACTION] Scaling down idle deployment: {name} to 0 replicas.")
            saved_cores += len(dep.spec.template.spec.containers)
            dep.spec.replicas = 0
            apps_v1.patch_namespaced_deployment(name=name, namespace="staging", body=dep)
            
    os.makedirs("/tmp/metrics", exist_ok=True)
    with open("/tmp/metrics/cost_metrics.txt", "w") as f:
        f.write("# HELP finops_saved_cpu_cores Estimated CPU cores saved by optimization\n")
        f.write("# TYPE finops_saved_cpu_cores gauge\n")
        f.write(f"finops_saved_cpu_cores {saved_cores}\n")
        
    print(f"[FINOPS-SUCCESS] Optimization complete. Saved {saved_cores} container instances.")

if __name__ == "__main__":
    scale_staging_environments()
'@ | Out-File -FilePath "src/optimizer/optimizer.py" -Encoding utf8
```
 
### ▪ Out-File -FilePath - This script injection command generated our complete Python automation code file instantly inside its proper directory.
### ▪ config.load_kube_config - This specific operation handles the secure credentials handshake with the Kubernetes cluster APIs.
<img width="967" height="336" alt="image" src="https://github.com/user-attachments/assets/92c1df22-c18b-4085-9014-aa3db8c785ad" />

## Section 3 : BUILD Entering the Build and Test Lifecycle Phase
### We transition from the local coding workspace into the automated compilation and software validation phase.
<img width="1236" height="930" alt="image" src="https://github.com/user-attachments/assets/b17c0528-e4cb-4908-99cc-4ee401d53339" />

### ▪ pom.xml - This configuration file explicitly instructs our automation engine how to download third-party libraries and safely compile our microservice components.
### ▪ Maven Gateway - This build platform standardizes compilation requirements so that the application behaves identically on your laptop and the production cloud.

## Section 4 TEST : Launching the Automated Maven Build and Test Suite
### We executed the command-line Maven build engine to compile our Java frontend source code and trigger our TestNG validations.
### ▪ Compiling 1 source file - This process automatically parses our Java classes and maps them to target machine bytecode assemblies.
### ▪ BUILD SUCCESS - This terminal confirmation proves our system architecture constraints passed all quality gates before containerization.
<img width="1330" height="983" alt="image" src="https://github.com/user-attachments/assets/dc259e04-faa7-442c-959f-1884ae172785" />


### Part 1: Embedding DevSecOps Security Gates & Shift Left Strategy
### We shift security validations to the absolute earliest stages of our software lifecycle instead of waiting until code hits production.
### ▪ Shift Left Mindset - This industry strategy means moving testing and security gates to the 'left' (earlier) in our workflow timeline to catch bugs cheaply before code is containerized.
### ▪ SonarQube & Snyk Dashboards - Our command-line pipeline scanners automatically package scan results and upload them to visual web consoles for real-time risk reporting.
<img width="801" height="215" alt="image" src="https://github.com/user-attachments/assets/f1b4ee1f-ea77-4d4b-afbd-a2d48feb1e1e" />

## Section 5 : RELEASE 
### We are creating the Python Optimizer Docker Container Configuration (src/optimizer/Dockerfile)
<img width="1075" height="431" alt="image" src="https://github.com/user-attachments/assets/e45eed7e-998f-415d-9eeb-b8296449716d" />




















# About me -- introduction
Hi, I'm Prashanth. I have around 9 years of professional experience as a .NET Developer and Cloud Engineer, primarily focused on building, maintaining, and optimizing scalable web applications and backend services.
I'm highly proficient in C#, ASP.NET Core, ASP.NET MVC, and Razor Pages, and have worked extensively on both Web Forms and .NET Core console applications. On the frontend, I’ve built responsive, user-friendly interfaces using HTML, CSS, JavaScript, jQuery, and Angular, and leveraged Bootstrap for mobile-first design.
I’ve implemented and consumed RESTful and SOAP APIs, handled custom SDK integrations, and used JSON extensively for data exchange. I also bring strong experience with OAuth2 and Azure Active Directory for secure authentication and authorization, aligning with enterprise IAM standards.
My database expertise includes SQL Server, Oracle, and MongoDB, where I’ve written complex stored procedures, joins, aggregations, and optimized query performance. I’m comfortable working with ETL workflows and handling large data sets.
In terms of DevOps, I’ve worked deeply with Azure DevOps to build CI/CD pipelines, automate deployments to both App Services and AKS, and manage version control with Git and Bitbucket. I’ve also integrated Terraform to provision Azure infrastructure as code.
I have hands-on experience supporting live production systems, troubleshooting performance issues, and documenting solutions for cross-functional collaboration. I’m very comfortable working independently or as part of Agile teams, and I’m quick to pick up new technologies.
Overall this is about me on a high level and I will be open for any questions.

### .NET and C# Core Concepts
### What is the difference between .NET Framework , asp.net and .NET Core? And how did you used it in your projects?

The .NET Framework is the original Windows-only platform used to build and run desktop and server-based applications. It supports technologies like ASP.NET Web Forms, Windows Forms, and WCF(Windows Communication Foundation).
ASP.NET is a web development framework that runs on top of the .NET Framework (and also on .NET Core as ASP.NET Core). It allows building dynamic websites, APIs, and services.
.NET Core is a cross-platform, open-source, and high-performance successor to .NET Framework. It supports building cloud-native, containerized apps and is used in modern development. Now, it's unified under .NET 5/6/7+.
### Usage in My Projects:
In my current role at Fiserv, I use .NET Core with Razor Pages and Web API to build modular, scalable web applications and microservices, deployed via Azure DevOps pipelines to AKS. I’ve also migrated legacy ASP.NET MVC(Model-View-Controller) apps (on .NET Framework) to .NET Core for better performance and platform independence.
In earlier roles like at NYPD, I worked with ASP.NET Web Forms on the .NET Framework, maintaining and enhancing existing enterprise apps before we moved to .NET Core and container-based deployments.

### what version of .net are you using?
Currently, I'm working with .NET 6 and .NET 7 in my projects, especially for ASP.NET Core and Razor Pages apps. I no longer use WCF in newer projects; instead, I use RESTful APIs and gRPC for inter-service communication. Previously, I worked with ASP.NET MVC on .NET Framework 4.6/4.8 before migrating those apps to .NET Core.

### What are Razor Pages and how do they differ from MVC? 
Razor Pages are page-centric and simplify building UI-focused web apps. Unlike MVC, which separates controller and view logic, Razor Pages use a single file model (.cshtml + PageModel) for cohesive development.

## Security & IAM
### How do you secure .NET web applications? 
By implementing OAuth2, OpenID Connect, HTTPS, input validation, anti-CSRF tokens, and role-based access control (RBAC). I’ve integrated Azure AD and SailPoint for centralized identity governance.

### How do you create and consume a RESTful API in .NET Core?  
I use ASP.NET Core Web API to expose endpoints, apply attributes like [HttpGet], [HttpPost], and return IActionResult or Typed Results. I consume APIs using HttpClient, manage headers, and deserialize JSON.

### What’s the difference between REST and SOAP?  
REST is lightweight, stateless, uses HTTP and JSON/XML. SOAP is a protocol using XML and WS-* standards, suitable for enterprise systems. REST is preferred for web/mobile APIs.

### Azure and DevOps
### How have you used Azure DevOps in your projects?  
I’ve configured pipelines (YAML and Classic), set up CI/CD for .NET apps, triggered builds from Git commits, deployed to App Services and AKS, and integrated with Terraform for IaC.

And in my recent projects I have used azure services like App Services, Azure SQL, Cosmos DB, Functions, Storage Accounts, Azure Monitor, AKS, Azure AD, and Resource Groups. I also use ARM templates and Terraform for provisioning.

### Explain a CI/CD pipeline you built and what different stages it has?
In my current role, I’ve built and managed complete CI/CD pipelines using Azure DevOps for .NET Core applications deployed to AKS.
## For CI (Continuous Integration): My CI pipeline has 6 stages -
1. Code Checkout – Triggered on Git commits or PRs.
2. SCA & SAST – We scan for vulnerabilities using tools like SonarQube and WhiteSource.
3. Build – We use dotnet build and dotnet publish to compile and generate artifacts.
4. Artifact Publish – The build output is published to Azure Artifacts or stored in a secure feed.
5. Docker Image Creation – We build a Docker image from the published code using a Dockerfile.
6. Push to ACR – The image is tagged and pushed to Azure Container Registry.
## For CD (Continuous Deployment): My CD pipeline has 5 key stages - 
1. Download Artifact – Pulls the image from ACR or the build package from Azure Artifacts.
2. Validate Infra & Inject Secrets – Validates AKS setup and injects secrets using Azure Key Vault.
3. Deploy to AKS – We use Helm charts or YAML to deploy containers to Kubernetes.
4. Health Checks – We run rollout status checks and API smoke tests.
5. Approval & Notifications – For prod, there's a manual approval step and Teams/email notifications post-deploy.

This setup helps us ensure secure, automated, and reliable deployments across environments, with traceability and rollback options in place.

## SQL and Data Management
### How do you optimize a slow SQL query?  
By analyzing execution plans, using indexes, reducing nested queries, avoiding SELECT *, using joins appropriately, and updating statistics. I’ve also written complex stored procedures and functions.

### What is ETL and how have you used it?  
ETL is Extract, Transform, Load – used to consolidate and clean data. I’ve implemented ETL logic in SQL Server and integrated it with Power BI and backend systems for reporting.

##  Frontend & UI Technologies
### How do you ensure a responsive design?  
Using Bootstrap’s grid system and utility classes. I test on different devices and browsers. I also follow mobile-first principles and accessibility guidelines.

### What’s your experience with JavaScript frameworks?  
I’ve used Angular for building SPAs, handling services, components, and RxJS. I’ve also used jQuery for DOM manipulation and AJAX, and TypeScript for structured scripting.

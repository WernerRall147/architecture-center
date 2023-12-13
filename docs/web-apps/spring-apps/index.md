---
title: Azure Spring Apps (ASA) architecture design
description: Get started on your Azure Spring Apps journey by reviewing guidance ranging from &quot;just starting out&quot; to production.
author: PageWriter-MSFT
ms.author: prwilk
ms.date: 06/06/2023
ms.topic: conceptual
ms.service: architecture-center
azureCategories: web
categories: web
products:
  - azure-spring-apps
---

# Azure Spring Apps (ASA) architecture design

Azure Spring Apps manages Spring-based applications on Azure. The service offers lifecycle management using comprehensive monitoring and diagnostics, configuration management, service discovery, CI/CD integration, blue-green deployments, and more.

## Get started

If you're just starting to explore Spring applications on Azure, start with these **training modules** on the Learn platform. This free online platform provides interactive training that includes knowledge checks to evaluate your learning. 

> [!div class="nextstepaction"] 
> [Learning Path: Run Java applications in Azure Spring Apps](/training/paths/deploy-run-java-applications-azure-spring-apps/)

For product documentation, see [Azure Spring Apps](/azure/spring-apps/).

## Design your first architecture

Now that you have a good understanding about deploying a Spring Apps application, apply your skills in designing a simple solution. Refer to this **baseline architecture** that deploys Spring Apps instance in a single region with zone redundancy. 

> [!div class="nextstepaction"] 
> [Reference architecture: Azure Spring Apps baseline architecture](./architectures/spring-apps-multi-zone.yml)

## Add complexity 

Build on the baseline architecture and extend the design to address a **multiregion availability** that can withstand a regional outage. You'll need to change the baseline load balancer to a global router. Also, you have extra considerations related to your choice distribution mode such as active-active, active-passive with hot standby, or active-passive with cold standby mode. 

> [!div class="nextstepaction"] 
> [Reference architecture: Deploy Azure Spring Apps to multiple regions](./architectures/spring-apps-multi-region.yml)


## Integrate with landing zones

Suppose, your organization wants you to **deploy the solution a part of an enterprise setup**. The architecture will change and there will be a shift in responsibilities. For example, the solution will use federated resources managed by central teams. You need to communicate your requirements with those teams so there aren't any disruptions. 

Refer to this architecture that deploys the baseline in an enterprise deployment that's design as per the design principles of Azure Landing Zones. Some sample requirements that should be communicated with central teams are annotated with "Platform team" notes.

> [!div class="nextstepaction"] 
> [Reference architecture: Azure Spring Apps integrated with landing zones](./architectures/spring-apps-landing-zone.yml)


## Sample implementations

The preceding reference architectures are all illustrated by implementations that you can reference to validate your design choices. They're available on GitHub.

- [Azure Spring Apps multizone deployment](https://github.com/Azure-Samples/azure-spring-apps-multi-zone)
- [Azure Spring Apps multiregion deployment](https://github.com/Azure-Samples/azure-spring-apps-multi-region)
- [Azure Spring Apps landing zone accelerator](https://github.com/Azure/azure-spring-apps-landing-zone-accelerator#azure-spring-apps-landing-zone-accelerator)


## Related links

- [Product documentation: Azure Spring Apps](/azure/spring-apps/)
- [Azure landing zones](/azure/cloud-adoption-framework/ready/landing-zone/)
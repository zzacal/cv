# Zac Zacal

Senior Software Engineer, Seattle

[github](https://github.com/zzacal), [linkedin](https://www.linkedin.com/in/zac-zacal)

## Senior Software Engineer - Alaska Airlines

Sep 2020 - Present

Contributed to the modern Alaska Lounge memebership system that helps guests sign up and pay for their lounge membership.

I was a main contributor and architect for migrating the lounge membership backend and front end applications from the legacy monolith to microservices running in docker containers on Azure Kubernetes Service with the help of the org helm charts. This allowed the team to deploy changes within minutes of approval instead of up to a week in the monolith. We used express on nodejs for the backend, which was written in typescript, and react with js for the front end.

I was the main architect of the redesign of the lounge checkin applications which tracked guest entry into Alaska's airport lounges. Based on the needs of the lounge and loyalty organizations, I designed an async system that's load-balanced between two different regions using Azure Functions and Azure Service Bus topics, which are queues with multiple subscribers. This allowed us to be resilient to a range of disruptions from network connectivity issues to region-wide outages. I chose to split the duties of storage between a document db and a sql db. The document db allowed us to add fields quickly as the business changed, while the data was copied over to sql stores so that we could create impactful reports that related lounge admission data with other parts of the business. When we want to make changes, we can quickly update our applications and save data to our document dbs, while we requested changes to our sql tables so that we could add the updated data to our reports.

Lead the modernization of Reservation Management that helps guests view and update their trip. It is a system that serves around 3.5 million requests a day.

I was the main contributor and architect for migrating the Reservation Management system from the legacy monolith to a distributed system of microservices and microsites using dotnet and dotnet mvc with csharp and razor and running on managed Azure App Services across two regions. By using auto-scaling, loadbalancing across instances and regions, and slot-swapping during deployments, Reservation Management is one of the most reliable applications at Alaska Airlines ecommerce. Beyond keeping our services available, I also worked closely with our partner teams who owned systems we depend on to help them prepare for our traffic. We held regular sync-ups and gave them metrics about how many users we were expecting and how many calls we were expecting to make to their systems as we ramped up deployment.

I also contributed to reservation update microsites written in svelte and improved user experience by fixing bugs.

Lead the modernization of Payments by establishing a single payment experience across different products on web and native mobile apps.

I architected and contribute to the replacement of disparate vendor-provided payment pages to a single payment experience system written in dotnet using csharp and react using typescript and deployed on managed Azure App Services across two regions. We use trusted vendors to provide credit card tokenization to maintain a level of PCI scope that allows other teams at Alaska Airlines ecommerce to operate outside of PCI scope. This allows us to scrutinize a few instead of many applications for PCI compliance, which helps us protect our guests' payment journey. I designed the system to be able to use the guest's authentication on the monolith Alaska application so that guests could use their saved credit cards during payment. Saved credit cards were previously only available to guests on checkout flows within the monolith.

I designed the workflows for integrating Apple Pay into the payment experience by partnering with our PCI experts, payment authorization team, and ticketing team. By adding Apple Pay, we will guests will be able to make purchases with fewer taps even if they're not logged in or if they don't have saved credit cards. This work also lays the foundation for adding other digital wallets.

Started workshops where experienced engineers shared their areas of expertise with newer engineers. I've personally led workshops on what to expect in a career in software engineering, and how to prepare to work after the internship. I currently mentor one intern and one senior software engineer.

## Software Engineer - Socrata/Tyler Technologies, Data and Insights

Aug 2019 - Sep 2020

Contributed to and maintained the data discovery platform, which helped users search through their organization's datasets.
Improved the search bar by adding suggestions as users typed search terms.

**Tools**: scala, java, ruby on rails, react with typescript, aws, mesos

## Owner, Software Engineer - Zacal Consulting

Dec 2016 - May 2019

### Senegence

Designed and built an ecommerce solution for MakeupRescue.com that uses .NET Core and MongoDB on Azure and Mongo Atlas.

Lead the expansion of the Senegence ecommerce application QuickOrder into international markets using .NET Framework, Angular 5, and MSSQL. These applications were deployed to Azure App Services and Azure-hosted VMs.

Integrated PayPal and Square Payments into the Senegence hosting application, Senesite, with a solution built with .NET Core and deployed as a Docker container on Azure Kubernetes Service.

**Tools**: dotnet, react, c#, javascript, azure, azure devops

### STR Helper

Designed and built an ETL solution for STR Helper that cleansed data from disparate sources using .NET Framework MVC, and MongoDB. This shortened the ETL process from a week per client to one or two days.

Designed and built a geojson-powered data-gathering solution for STR Helper that queried external systems based on a city or a county's geojson polygon. This application used .NET Framework MVC and MongoDB's gis features to automate what was an intense manual process.

**Tools**: dotnet, react, c#, javascript, azure, azure devops

### Alergan

Lead the Allergan rebuild and redesign of the reward program Brilliant Distinctions. The application was built on Sitecore CMS which is implemented on .NET Framework. I implemented scrum methodologies for the development team. This resulted in better tracking of work from the previous process and contributed to meeting due dates.

**Tools**: dotnet, c#, javascript, azure, azure devops

## Senior Software Engineer Renovate America

Jan 2016 - Dec 2016

Lead the development of the marketing content management system built on Sitecore.
Partnered with marketers and content authors to build a dynamic and flexible content platform that empowered content authors to publish rich promotional and informational pages within minutes.

**Tools**: dotnet, angular, c#, javascript, azure, azure devops

## Web Application Developer
Apr 2013 - Dec 2015

Contributed to flagship brand marketing web applications BrilliantDistinctions.com, BotoxCosmetic.com, Juvederm.com using ASP.NET MVC.

## Education

Cal State Fullerton, College of Business and Economics
BA Information Systems and Decision Science
2010-2013

## Side Projects

### SchemeIdol

[schemeidol](https://www.schemeidol.com/)

A web version of Strategem Hero

### Tilda

[tilda](https://github.com/zzacal/tilda)

A mocking tool to help me work without relying on dependency services

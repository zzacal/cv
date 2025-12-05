# Zac Zacal - Achievements

## Technically Adept

- Achieved 2025 PCI Compliance Improvements on Payment Page allowing Alaska to continue to collect around $1M in ancillary revenue daily from guests using credit cards all while allowing the rest of the team to focus on business initiatives.
- Improved guest experience by investigating and fixing an issue where Perimeter X was inadvertently blocking some guests from making payments.
- Led discovery with Mobile, In-Flight, and Seats development engineers to architect a payment fulfillment workflow that served different teams with different needs, which is now the most-used post-book ancillary payment workflow.
- Helped the guest communications team to find the root cause of an outage for a service that queued emails that went out to guests including an email for ancillary receipt. Unknown IPs were blocked at the network, and APIM IPs were not on the allow list.
- Architected the payment page to gracefully fail for the unavailability of Credit Card on File, Apple Pay, Bluefin, and Cybersource so that any one of our payment methods could fail to load, and guests could still continue to purchase for their ancillaries. We had an incident where Apple Pay did not load on the page in June, but guests were able to use credit card on file or manual card entry to complete their payment. We also had an incident where the Cybersource form was failing to load for part of the day, but we did not see a significant impact because of the availability of other payment methods.

## Modernization

- Worked with Ready-To-Fly team, and Irregular Ops team to adopt a payment process with improved control flow that handles edge cases that could not previously be handled.
- Worked with Ready-To-Fly team to create stronger scopes of responsibility from the Atlas team. Ready-To-Fly previously relied on Atlas to fulfill bag OSIs. This makes it easier to improve guest experience. After this change, we were able to offer guests Apple Pay as a payment method, which 1/3rd of guests who pay for bags prefer to use.
- There was an issue with authorization on the native mobile apps' authentication workflow where opening an authenticated web-based experience required multiple redirects resulting in the guest seeing a blank screen for a long time. 
    - In collaboration with other engineers, I planned and implemented an improvement to native app users' experience by allowing mobile apps to load the payment page without redirects using Auth0.
    - This was done without any interruption to the guests by maintaining compatibility with pervious app versions.
    - According to the mobile engineers the implementation on payment webview is currently the gold standard for stability.
- Implemented a backend for front end for the payment page that allowed the payment page to handle secrets, authorization, more securely.
- Worked with Atlas and Promos and Discounts team to create a path towards replacing Bluefin microform with the Cybersource microform without changing the systems' PCI scope. This is important to contain PCI scope within the company to minimize the impact of PCI DSS requirements.


## Automation

- Using Azure health monitoring, scaling rules, and automatic recovery, the payment page is resilient to any of our cloud-hosted instances becoming unavailable. This results in the Payment Page system not causing any outages for since we've adopted our automatic recovery strategies.
- Started and continue to contribute to the team pipelines that is able to check the code for build errors and quality issues, deploy the application, deploy secrets, set health rules, etc.
- Coached our newest engineer to move secrets from the pipeline into a shared library to make reuse easier.
- There was an issue with the Level Access accessibility automation tool where a CVE in the library's dependency prevented us from having clean security reports. This caused our repository and any other repository at Alaska to have Github Dependabot alert noise for a CVE. This could lead unclear signals about actual problems, and even the prevention of deployment. I solved the CVE by overriding dependencies and shared the solution so other teams can quickly fix the CVE in their repos. The solution is in the Alaska Level Access implementation guide.

## Continuous Improvement

- Coaching team on git tools especially around good commit history and messages.
- Developed a data mocking tool to make iterations faster and make development less reliant on live data. This allows front-end development to happen even if there are some outages in lower environments.
- Developed a tool to allow developers to quickly view a reservation in cert with a web UI using middleware APIs
- These tools are intentionally made with tech stacks adjacent to the team's tools to understand the larger environment better. Our apps are hosted on Azure web apps, and written in dotnet and react. Tools are made with containers, nodejs, svelte, svelte kit.

## Leadership/Strategic Skill

- Brought solutions to the PCI Governance team for problems with PCI compliance that were nuanced and needed more scrutiny especially the case with Tealium's utag.js. This allowed us to come up with a tactical solution to continue operating, while working on a long-term fix with the Analytics Team
    - Collaborated on PCI compliance best practices with Lounge and Inflight teams
    - Shared all relevant info across Booking, Lounge, and Inflight teams to help the org prepare for the next audit and prevent the days worth of meetings to discover and solve shared issues
- Prioritize quality of documentation to enable client teams to integrate with the payment system efficiently.
- Led a tech debt triage process to prioritize improvements in collaboration with EM and Principal Engineer and operationalized that process with the engineering team
- Created and continue to maintain an Ancillary Payment dashboard for at-a-glance info that has been used to identify opportunities like:
    - Lower conversion rate for Apple Pay when upgrading seats that has now been corrected
    - The order of the fields for credit card entry that improved guest success when entering their credit card manually
    - Rough estimates of dips in revenue from ancillaries from system or global outages
    - Failures during testing due to invalid test credit cards
- Architected and executed on long-term upgrades to the Payment Page to enable purchases on the Seats 2.0 launch. The features implemented extended to other teams allowing everyone to deliver even better guest experiences. 
- To help implement localization safely, I brought together team leaders and contributors from different teams to discuss the dependencies across multiple teams' applications. 
    - This prevented any team from implementing localized outbound links before applications were ready for them, which would have caused guests to see broken pages.
- Worked with Engineering Manager and Product Manager to establish an MVP for the Payment Page's redesign.
    - This allowed us to iteratively deliver a post-book payment experience that is cohesive with the booking payment page.
- Created a pattern for the team to be able to iteratively add new credit card networks by documenting and implementing one payment gateway at a time. This allows us to enable new networks quickly in small releases.

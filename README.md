# docs
This repository contains all [full-stack-conversation](https://github.com/full-stack-conversations/docs/edit/master/README.md)  (***this***)  Github organization's documents. Simply stated, this **[docs](https://github.com/full-stack-conversations/docs)** repository contains documents describing all other repositories in this _organization_.

These documents are organized in the form of markdown based tutorials created and maintained by Vue and Vuepress. Note that the role of Vuepress is to facilitate a lot better MarkDown documents -  just being able to use **["Medium Zoom like"](https://github.com/francoischalifour/medium-zoom/tree/master/examples/react-markdown)** handling of images is quite sufficient to build the whole docs repository based on **[VuePress](https://vuepress.vuejs.org/guide/)**.

Simply stated, this repository contains the tutorials and other types of documents related to the content of the **[full-stack-conversations](https://github.com/full-stack-conversations/docs/edit/master/README.md)** organization. This relationship was choosen as the simpler technique than using [Monorepo](https://medium.com/@johnclarke_82232/mono-or-multi-repo-6c3674142dfc) approach.

The initially chosen topic is that of **[IAM (Identity and Access Management)](https://en.wikipedia.org/wiki/IAM)** in the context of JavaScript full-stack applications - spefically full-stack applications where the back end application is based on [Strapi](https://strapi.io/). Our development plan keeps Strapi as the only invariant - we vary front-end frameworks of interest to many as well as IAM services that are implemented as a **[PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service)**. Examples of such services include [Auth0](https://auth0.com/), [AWS IAM](https://aws.amazon.com/iam/), [Okta](https://www.okta.com/), etc. (see the [The 30 Best Identity Management Companies For 2020](https://solutionsreview.com/identity-management/the-30-best-identity-management-companies/) for more information.

### Important notice

In a very recent blog [Announcing Strapi 3.1 - Administrator Roles & Permissions](https://strapi.io/blog/announcing-3.1-role-based-access-control), Strapi's [Alexandre Bodin](https://www.notion.so/7870e243b38a44798c84a4498ff01707?v=3efa4ca59dec4b1eb445722327fb03fc&p=74de59b4c67d464ea7e04826c4a9a8f1) introduces **[Role-Based Access Control (RBAC)](https://en.wikipedia.org/wiki/Role-based_access_control)** as the next most often demanded feature by Strapi customers.

While RBAC is a standard feature of a typical IAM provider, Strapi decided to implement RBAC using the [PassportJS](http://www.passportjs.org/), which is a well known authentication middleware for Node.js based application. This decision is a well thought through optimization - instead of creating Strapi IAM model on say Okta, Strapi team needed a relatively small RBAC subset, using PassportJS. 

A key difference between "real" IAM and Strapi's current "mini" IAM is the "ownership" of users. In Strapi, it is the Administrator's console (as well as Strapi API, "behind" the scene) that creates and manages users. If Strapi were to use an IAM PaaS service, all "user related tasks" are farmed out to the service provider, resulting with the claim that all security issues are handled by a proven entity - IAM PaaS provider. This claim is of extreme importance to any future Fortune 500 Strapi customer, so samples and tutorial we plan to create will serve as a peek into Strapi's future. Please check the **[How to Securely Manage Users in Your Node App](https://github.com/full-stack-conversations/managing-users-node-app)** explaining this concept of leaving the users management to the Okta PaaS. 

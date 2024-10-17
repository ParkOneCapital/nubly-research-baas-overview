# Beyond the API: The Accounting of BaaS (FBO vs. On-Core)

While APIs are the technical backbone connecting BaaS providers to banks, the ecosystem can use various accounting structures to interface as BaaS partners. The most common types are the For-Benefit-Of and the On-Core accounts. There are technical, regulatory and business implications depending on the type of accounting structure chosen.

“What is the difference between FBO and on-core banking?

At a high level, on-core accounts allow you to leverage the bank’s existing infrastructure in a meaningful way and lead to potentially less work or obligations to open and maintain. However, the clear offset to this is a potentially limited ability to customize certain features of a product offering. A great on-core use case could be a white-labeled or co-branded non-fintech embedding bank accounts in their product as a side perk, or just offering one or a couple of peripheral financial tools. 

FBO accounts, on the other hand, require more responsibility from the company managing the account, but also allow for greater customization. The FBO route can be attractive for companies offering bank accounts and various financial tools as central features in their product.”

source: https://www.treasuryprime.com/blog/whats-an-fbo

## The For-Benefit-Of Accounting Model

[![FBO Example](./assets/fbo_1.png "FBO Example")](https://www.moderntreasury.com/questions/what-are-the-benefits-of-an-fbo-account)

“An FBO account, or a For Benefit Of account, allows a company to manage funds on behalf of—or for the benefit of—one or more of their users, without assuming legal ownership of the account.

What does that mean for business owners? At a high level, FBO accounts enable businesses to manage their clients’ money without the costly regulations that can come with certain types of money transmission. 

While FBOs now include the digital transfer of funds, the concept dates back to fiduciary agreements around feudal land ownership in the twelfth century. Since then, managing an asset of value on someone else’s behalf has evolved into many modern legal arrangements, including bank accounts for children on behalf of their parents, wills, trust funds, and more. 

Before a company decides to open an FBO account, it’s important that they do their due diligence. This includes clarifying their needs with legal counsel first and more.

### How do FBO accounts work?

Imagine your FBO account as a hotel building. From the outside, there are many windows that represent your different clients with their own sub-accounts, also known as virtual accounts.

For example, say you want to send money to Olivia in the penthouse suite by attaching a check to a paper airplane and sending it through Olivia’s window. Think of her floor and room number as her account and routing number—in other words, they’re unique to her virtual account under the FBO.

Now imagine that all the money that comes through these separate windows exists in a large pile on the lobby floor, in what’s known as a pooled account. Olivia is only concerned with the money she receives in her virtual account. From the bank’s perspective, however, all the money from these different virtual accounts is available in one place. In other words, all the money in the FBO account is fungible.

That said, it’s the bank’s responsibility to track money that comes and goes from this pooled account. This tracking system is like a doorman, who functions as a ledger, by organizing funds and providing visibility. If funds are distributed to any one room, or virtual account, the doorman makes a deduction. He knows how much money is coming and going from the entire hotel, or the account at large.

### What does an FBO account look like in practice?

Let’s say a neobank, Peanut Butter, opens an FBO account at a bank called Jelly. Jelly is holding the money on behalf of Peanut Butter. Think of it as Peanut Butter managing the hotel, while Jelly technically owns the hotel, or the FBO account. 

Now, Peanut Butter can provide individual virtual accounts to all of their clients. Each client has their own unique room and floor number, or virtual accounts complete with individual account and routing numbers. Peanut Butter is able to stay organized and keep track of their clients’ payment operations with a ledger software.”

source: https://www.moderntreasury.com/learn/what-is-an-fbo-account, https://www.moderntreasury.com/questions/what-are-the-benefits-of-an-fbo-account

## Types of FBO Accounts
“There are two ways to operate an FBO setup depending on your BaaS provider. 

[![Dedicated FBO](./assets/fbo_2.png "Dedicated FBO Example")](https://www.moderntreasury.com/questions/what-are-the-benefits-of-an-fbo-account)

Traditional "dedicated FBO" approach: The traditional and less risky approach is for the BaaS provider to open a discrete FBO account for each company it partners with. Under this approach, you have your own dedicated FBO account from which to carve virtual accounts for your customers. This is the approach Treasury Prime uses.

[![Intermingled FBO](./assets/fbo_3.png "Intermingled FBO Example")](https://www.moderntreasury.com/questions/what-are-the-benefits-of-an-fbo-account)

Alternative “intermingled FBO” model: Some BaaS providers offer an intermingled FBO model. In this alternative model, the BaaS provider opens one FBO account to service all of its company clients, rather than have each company open an FBO account with the partner bank directly. This arrangement basically means you are sharing risk with other companies, and also that you are all subject to the same one-size-fits-all KYC and compliance operations. In short, this second option can come with higher risk. 

### FBO Data flow

In an FBO setup, users interact with their accounts through the user-facing app you have built. The app connects to a banking API layer, which contains a ledger where records of user account activity are held. The ledger is built on top of an FBO account. That FBO account exists on the bank’s core and attaches to the bank’s services.”

[![FBO Data Flow](./assets/fbo_4.png "FBO Data Flow")](https://www.treasuryprime.com/blog/whats-an-fbo)


### “Benefits of an FBO account

More control over KYC & account approvals: In an on-core setup, your partner bank performs essentially all typical bank services. That means the bank decides whether to approve certain customers, not you; and the bank decides what forms of identification it will accept for KYC. This can limit who you can accept as a customer. In an FBO model, those services can be performed by you with support from the BaaS provider and other compliance partners, and you have more flexibility based on your specific user base and customer risk profiles.

Faster account opening: Because you have control over the process for opening your customers’ virtual accounts, you can do so faster. 
Can be less expensive than on-core 
More latitude to customize and innovate: Your FBO account holds your customers’ virtual accounts, which means you and your BaaS provider can collaborate on what features you want to offer. 
Easier to mitigate bank partner risk: No one wants to pick a bank partner and build a successful program with them just to rip it all down to move banks. However, sometimes this hard truth is a reality for many reasons that you may not always be able to control.  Treasury Prime accounted for this possibility and built its technology to be bank agnostic. So if you need to switch banks you would not need to rebuild your tech stack, change bank account numbers or learn new procedures.  While some things just can’t be automated, like a change in routing number or end-client acknowledgment of the change, we have made it as painless as possible. 

### Drawbacks to FBO account

Increased support responsibility: Because your FBO account holds your customers’ virtual accounts, you are responsible for servicing them. If your customers opened accounts directly on your partner bank’s core, the bank could fully service them. 

Increased reporting requirements: Similar to having increased responsibility for supporting customers’ accounts, you will also be responsible for staying in compliance by reporting information and activity to authorities such as the FDIC.

Greater responsibility for fraud prevention: Your partner bank can’t see what’s happening within your customers’ virtual accounts. That means it’s up to you to monitor accounts for potential fraudulent activity.”

source: https://www.treasuryprime.com/blog/whats-an-fbo

## The On-Core Accounting Model
### How on-core accounts work

“When you opt to offer on-core accounts in your app, the accounts exist directly on the bank’s back-end system for processing daily transactions. That means accounts can potentially do everything the bank’s core allows — and also only what that core allows. Some examples of settings that are commonly global across a bank's platforms are KYC decisioning, onboarding procedures, incoming funds holds times/rules, overdraft settings, account fees or incoming ACH decisioning. Additionally, the bank has greater visibility into account activity, which allows the bank to participate in customer support and simplifies compliance. Compliance refers to processes that help fintechs and banks stay in line with any number of laws, regulations, or rules imposed by regulators or industry self-regulating organizations. 

### On-core data flow

In an on-core setup, users interact with their accounts through the user-facing app you have built. The app connects to a banking API layer, which interfaces directly with the bank’s core and, in turn, the bank’s services.”

source: https://www.treasuryprime.com/blog/whats-an-fbo

“On-core accounts require less maintenance from you as an app developer and allow you out-of-the-box access to all of your partner bank’s account services. That said, your features may be limited with this setup. But if you’re embedding financial tools to enhance your app, rather than making them central, on-core accounts can get the job done with less hassle.”

source: https://www.treasuryprime.com/blog/whats-an-fbo

[![On-Core Data Flow](./assets/on_core.png "On-Core Data Flow")](https://www.treasuryprime.com/blog/whats-an-fbo)

### “Benefits of on-core accounts
- All of the bank’s account services out-of-the-box: Your customers essentially have traditional accounts with your partner bank, granting them all the bells and whistles that come with that, without you having to build out those features.   

- Bank-grade KYC and fraud detection: You can leave the process of approaching applicants for accounts and monitoring accounts for fraudulent activity up to your bank.

- Extra customer support: Because customers have accounts directly with the bank, they can go to the bank for customer support needs that involve account-level issues. 

- Maintained by the bank partner: The bank maintains accounts and updates them as needed. 

### Drawbacks of on-core accounts
- Inflexible: Customer accounts opened on-core must follow all bank policies, and can only offer features the bank permits. Ultimately account offerings are dependent on the bank’s existing services and processes. 

- Less control over KYC & account approvals: When customers open accounts directly with the bank on-core, it’s up to the bank what forms of identification to accept and which account applicants to approve. 

- Slower account opening: Whereas with an FBO account you can just issue a virtual account when ready or necessary, with an on-core account your customer must go through the full process your partner bank uses to open accounts. 

- Bank core technology limitations: When accounts are opened on-core, their features are limited to what the bank’s core can handle from a technology standpoint.”

source: https://www.treasuryprime.com/blog/whats-an-fbo
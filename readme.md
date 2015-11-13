#Cirlces
"Circles" will be a currency created from basic incomes only. In the system outlined in the following, new money is constantly distributed to every account participating in the system. The money in every individual account are uniquely identifiable and only gain in value if the account connects to other accounts and joins groups. This incentivizes every user to limit themselves to one account.

##Rules
Everyone can create a new account
An account will constantly generate an income (1000 units per week
The rate at which the income is generated will increase by g=2% per year
A new account starts with the income that will be generated in the next 3 months.
One month of income is for the account owner - the other two are reserved for people who trust this account, it is called the trustee reward.
Accounts can trust one another. This will allow both accounts holders to exchange their coins 1:1.
Trust can be revoked by both parties.
If an account trusts another account it is credited with half of the remaining trustee reward.
Arbitrary groups can be created.
Groups can verify accounts as members.
Groups can exclude accounts as members.
All members can convert their private money into group money (1:1 exchange rate). This exchange is irreversible.

##Design rationale

The main purpose of this project is to establish a world wide basic income.

Requirements are:
a. Decentralization
A world wide basic income is something so powerful that no single entity in the world should have control over it in order to preclude manipulation. Particularly, there should be no central authority that decides which person can get a basic income and which person cannot.

b. Smooth growth
The solution should support a smooth growth. If the only two equilibria are "no one participates" or "all people participate" then it is nearly impossible to change to the "all" equilibrium, especially if no central entity is involved. In the approach presented here, groups can grow locally, even starting at a single family level. However, there are no constraints on subsystem growth. All subsystems can merge into a global system at any time.

c. Resilience
The system can support something like a world currency. However - if this currency fails at some point, it is not the whole system that would collapse. Instead, the system would fall back on the group level underneath, for instance a country group. Even if the group currencies should fail at one point (because they accepted too many members that just consume their income and don't provide any goods or services for their income) it can still fall back on the personal level where the value of a currency is closely related to the personal relationship with the other person.

d. Incentives for organic growth
The trust reward should help to give a strong incentive to bring new people to the system. Adding new accounts to your circle is to some degree a risk. To balance the incentives and enable growth we introduced the trust reward. It creates common incentives for both the newcomer and the people already established in the network: Through the acknowledgment of the trust relationship, the newcomer gains network credibility and the first people to place their trust in the newcomer benefit financially. The risk inherent to trusting a newcomer are only out-weight by the benefits if the newcomer is be-known to the people who place their trust in them. If the newcomer does not turn into a viable member of the network the trust placed in the newcomer was misguided and the trust results in a financial loss.

e. Universality
Some people argue that Bitcoin was a one time shot. A currency has to be scarce to some degree to function as such. A single digital currency can have features that ensures the scarcity of this currency - however, if other digital currencies become successful, scarcity as a characteristic of digital currencies overall becomes questionable. This is especially true for a basic income. We strongly believe that a basic income currency can only be successful if it is the only one that is commonly used. This is why we keep this proposal as general as possible. The only free parameter crucial to the system is the growth rate g and needs to be discussed carefully. The trust reward is not strictly necessary, however, it does not affect the long term equilibria of this approach.

Detailed discussion.

6:
Transitive Transactions
If A and B trust each other, and B and C trust each other, then A and C can pay each other as long as B is liquid. If A is a customer and C is a merchant, A could send money to C. The network will automatically send a-coins from A to B and b-coins in exchange for the a-coins from B to C.

3:
The growth rate g = 2%.
The growth rate g determines the ratio between the total coin supply and the income per month. This number is subject to discussion. It should be chosen to maximize the value of the income.
Note that a high growth rate (inflation rate) destroys the capability of the currency as a store of value. Consequently, the potential dollar market cap is a function of the growth rate: market cap = f(g). (The market cap of the currency is a function of g that most likely will decrease sharply for bigger g like 5% or 10%). g should be chosen to maximize g*f(g).

The growth rate can be seen as a capital tax that finances the basic income. People with exactly the average wealth would pay the same amount of money in fees as they would get from their UBI.

9-12:
Groups
Groups are necessary to bring more stability into the system. Holding coins of a specific person always carries a certain risk. In some sense, the value of theses coins is always backed by the person. If the person dies or more broadly speaking the trust in this person sinks, these coins may become worthless. However, as long as a person is member of a group, the money can be converted irreversibly into group money. It is in the responsibility of the groups themselves to keep them tight on the one hand to not dilute the value, but on the other hand have a positive network effect. This makes it interesting for merchants to accept such group money.

##FAQ:
Q: Can I create 100 fake accounts that all trust each other and abuse the system?
A: You can create them but this will not create value. As long as nobody else trusts these accounts they can only exchange money with each other, rendering all the money worthless.

Q: Why should I add someone else to my trust network?

A. Your trust network is what gives your personal currency value beyond what you are willing to provide for this currency. Lets say 100 people are in your trust network, that means that 100 people are accepting your currency. Even for those who do not accept your currency directly, may accept it indirectly since they know they can use it to get goods or services from 100 people. Accepting money is all about network effects.
However, on the other hand accepting a new person bears some risk. If this person turns out to be a fake account you will end up having his worthless money and the scammer can spend your money. To make the incentive higher to be among the first to accept an new account nevertheless, the trustee reward was introduced. However, accepting a completely new account will and should be backed by a personal relationship of the two participants that ensures that the new person participates honestly in the system. If they don't the only person who loses money is the person who wrongly trusted them.

Q: What is the money of an account worth?
A: In theory it should be max(value(group1), value(group2), value(group3), ... , value(connection1), value(connection2), ...). Note that only connections to liquid people count. As long as the memberships in the groups and the connections are stable (or expected to be stable) there should be no incentive to convert money into group money.
This concludes in the assumption that it is not necessary to convert your money into group money or to exchange money with one of your trusted connections. Just having the ability to do so makes your money at least as worthy. This could stabilize the system and allow user A to connect to user B despite the fact that user B's coins are worth less. This connection could raise the value of user B's coins without changing the value of A's coins. However, this stops if B tries to abuse this connection, but in this case, A can cancel the trust relationship.
From time to time users could lose their connections because they create panic. This is the unlikelier the better the user is connected. This strengthens the incentive to concentrate all your social connections/ reputation into one account.

Q: How much of the group money is yours?
A: The amount that you've converted. Only difference is that now it's no longer tied to you as an individual. This means that if you do something bad, the group cannot do anything to revoke your group money. However, they can kick you out of the group.

With groups exchanges are mono directional with individuals. Only individual => group, NOT group => individual. However, exchanges are is bi-directional between groups. So Berlin <=> SF is OK.

Implementation:
The easiest way to implement Circles would be as contracts on Ethereum.
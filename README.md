# tarrie-planning

This repo will contain the textual planning in the `Wiki` and  design planning for various features in the actual repo. Design planning is any thing you see that an app does well and that we need to steal in some sense. See  `contact_search` for a sample feature design found online. 

# ToDo's 
**btw when I say `read up on` I usually mean watch the best tutorial you can find lol**
1. *(Anyone really)* Write a paragraph of what Tarrie is, like a description of Tarrie, and put it at the top of this `README.md` so we can explain it when mentioning it to people. 
1. *(Individually)* Finish Case Studies on competitor's (mark which case you are taking in the wiki)
2. *(Individually)* Read each others case studies & prepare for product management meeting in the next step.
    - Read anything you can on how to manage this product or UX design (they go in tandem) because we're just hacking it currently.  Use [libgen](http://gen.lib.rus.ec) to dowloadbooks for free. Below are some books I dont plan on reading except maybe the first one, they are rank ordered according to my 1second glance at user reviews. Just keep reading as project goes along because insufficient Ux design/product managment is why startup fails so we want to keep getting better as we progress, incorporating new knowledge continuously. This is a non-exhaustive list please contribute.
        - [UX STRATEGY](https://www.amazon.com/UX-Strategy-Innovative-Digital-Products/dp/1449372864/ref=pd_sbs_14_52?_encoding=UTF8&pd_rd_i=1449372864&pd_rd_r=bf2357a2-9ffc-11e9-a93c-6bb543d57023&pd_rd_w=hzgSQ&pd_rd_wg=iUFRZ&pf_rd_p=588939de-d3f8-42f1-a3d8-d556eae5797d&pf_rd_r=4RDMQ3M655SMAYQ82XS6&psc=1&refRID=4RDMQ3M655SMAYQ82XS6) | 300pages | misleading title ... its has walk through of lean methology + ux design
        - [INSPRIRED- HOW TO CREATE TECH PRODUCTS CONUMSERS LOVE](https://www.amazon.com/Things-Designer-People-Voices-Matter/dp/0321767535/ref=pd_sbs_14_3/147-3790180-3484262?_encoding=UTF8&pd_rd_i=0321767535&pd_rd_r=29f3e577-9ffe-11e9-9768-fd03c2f337af&pd_rd_w=4hVlc&pd_rd_wg=dNpq0&pf_rd_p=588939de-d3f8-42f1-a3d8-d556eae5797d&pf_rd_r=4ZW21Y3G7QYS3SQ6Q2TQ&psc=1&refRID=4ZW21Y3G7QYS3SQ6Q2TQ)| 350pages | top book in amazon business research + dev
        - [THE lean product playbook: How to Innovate with Minimum Viable Products and Rapid Customer Feedback](https://www.amazon.com/Lean-Product-Playbook-Innovate-Products/dp/1118960874)| 330 pages | people like it because it provides a clear guide
        - [DONT make me think](https://www.amazon.com/Dont-Make-Think-Revisited-Usability/dp/0321965515/ref=pd_sbs_14_1/147-3790180-3484262?_encoding=UTF8&pd_rd_i=0321965515&pd_rd_r=c89bf61d-9ffc-11e9-b61a-832b178781ff&pd_rd_w=Fw7nj&pd_rd_wg=s75Ay&pf_rd_p=588939de-d3f8-42f1-a3d8-d556eae5797d&pf_rd_r=0PCZHT6S284BSPW7QX9R&psc=1&refRID=0PCZHT6S284BSPW7QX9R) | 200pages
        - [100 things every designer needs to know about people](https://www.amazon.com/Things-Designer-People-Voices-Matter/dp/0321767535/ref=pd_sbs_14_3/147-3790180-3484262?_encoding=UTF8&pd_rd_i=0321767535&pd_rd_r=29f3e577-9ffe-11e9-9768-fd03c2f337af&pd_rd_w=4hVlc&pd_rd_wg=dNpq0&pf_rd_p=588939de-d3f8-42f1-a3d8-d556eae5797d&pf_rd_r=4ZW21Y3G7QYS3SQ6Q2TQ&psc=1&refRID=4ZW21Y3G7QYS3SQ6Q2TQ) | 250pages

2. *(Meeting)* Merge what we learned from competitors to finish up value proposition, customer segmentation, channels, and revenue. The case studies usually include tips on metrics to watch, things to highlight like `invite friends` or `share event`, and other knickknacks that seem important. Let's write these down as well and highlight things that are common. 
3. *(Individually)* Finish Agile Training
4. *(Individually)* Set up [Maven](https://maven.apache.org/)
    - Tarzia reccomends this for Java consistent configuration file that tells application to run the correct libaries. So basically in Python you might have the wrong version of Pandas or Numpy and so the code your working on is broken because the person who wrote the code used a very old version. With Maven it makes sure correct libaries installed so you don't have to worry about issues like this.  (btw in python this can be fixed with a virtualenv + requirements.txt with specific versions since default version of something is the latest)
5. *(Individually)* Know what a restAPI is, look into [Tomcat Webservices](http://tomcat.apache.org/), what a servlet + server model for Java. The key is to understand the direct connection between Tomcat and servlet. 
6. *(One Person Does this only)* Set up an AWS EC2 server. Keep password/login somewhere safe and share with others'
7. *(Individually)* Read up on [Elastic BeanStalk](https://aws.amazon.com/elasticbeanstalk/)
    - Basically a java server can only hold 1000 request. Elastic BeanStalk allows you delpoy multiple copies of the same java servers and all request will be load blanced. Meaning when someone request a service form our IP address associated with our AWS EC2 server, BeanStalk will choose a random random java server to route the traffic too. Now we can scale up easily and serve more customers. Also it a good programming principle to store passwords/logins in environment variables so we don't accidently upload them to github (For instance the password/login for a PostgreSQL server holding our data). Good software design will enable the javacode to call environment variables when accessing outside resources like server's and basically anything that takes a password via preset environment variables, so if we change from PostgreSQL to MySQL we wont have to touch code just change the environment variables. So....... BeanStalk has someway to save environment variables for each virtual java machine it is running. 
7. *(Meetup)* Draw out API protocols, create issues on github, set up our Kanban/Board full of tasks, assign issues to actual people. After this we sart coding our issues and we have finally started. 




##### Short Tarzia meeting (7.5.19)
- Gmail gives us access to Google Login API. Might be useful to see API connected to Google contacts App. Oh and also when searching a persons contacts we can just limit it to northwestern accounts when we show suggestions
- WHen a person signs up they get to add admins + members by email via gmail. When a person creates event and sends via email blast people. Both cases if person is outside network the email will provide a uplink to click that is essentially a hash/token. So,  when a person signs up through that token we automatically link the contact information in the inviter's contacts to the new profile created by the invitee.If the person visits the tocken link but does not sign up they get a cookie, now if they decide to sign up later we know who they are and can automatically link the contact information in the inviter's contacts to the new profile created by the invitee. However, this only works if the person doesn't clear their browser data. We can use cookies to check if a person is already logged in and direct them to the correct page. We can use cookies to find out if a person has two accounts and suggest for them to link the two if they want to (only suggest this once, this is an advanced nitpicky feature). 
- Think about using SQL-Lite. SQL-Lite is a very lightweight database usually used for embedded systems and applications. So say you are playing a local mobile game how does an app know the state of the game each time you login? SQLLite bro! Store things locally via SQL-Lite, push local changes to our main database when we want to. But SQLLite takes care of localdata so were not always calling the internet for data from our remote server. This is usually better than storing local files on a system. 

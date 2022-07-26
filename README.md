
# Cloud Native Video
- Make 3d comparative graph of architecture solutions - tech level, tech flavor, tech maturity (Gartner bracket) 

# Notes
- Replacing with SaaS allows coupling costs to usage much more effectively than hiring contractors to mange your IaaS.
- A great strategy to prevent ransomware attacks is to become cloud-native. Can't hack what isn't there. Reach out to me to learn more about reducing your attack surface while reducing costs and increasing flexibility.
- Cloud-native strategies are one way to couple tech profits and expenses more tightly. Reach out to me to find out how to reduce costs while increasing service speed.
- Where to incorporate shift left? 
- SaaS cost differential - This is part of where companies see massive savings from going to "the cloud" - in not having to patch (or rotate) fleets or herds of servers. Lift-and-shift is like a technical loan for your technical debt, and can help you keep expanding when you're in a tight spot, but it's the least efficient way to become cloud-based.

# Timeline
- Getting companies to stop operating like it's 2006 or 2014 and act like it's 2022. (messaging)
- 1990s model: LAMP stacks running on standard OSes on bare metal in a physical data center.
- 2001 VMWare ESX released (They got the letters mixed up, just like Toyota does with the XSE trim level.)
- 2001 model: LAMP stacks running on virtualized OSes on VMWare on bare metal in a physical data center.
- 2006 AWS EC2 released
- 2006 model: LAMP stacks running on virtualized OSes on an EC2 server.
- 2014 Containers & Kubernetes released
- 2014 model: containers on a managed EC2 server.
- 2018 AWS Lambda matures (AWS product offerings explode)
- 2018 model: Lambda functions behind API Gateways. (Suite of products arrayed to support eCommerce and Big Data backing the site.)
- 2019 AWS Control Tower released.
- 2019 model: Numerous AWS accounts nested under a main account.

# Levels of Windows Patching
- Manual patching (5 min per server is 12 servers per hour)
- Managed Patching / Managed OS - pay someone else to do it
- SCCM - package & deliver updates, have Group Policy install it, and verify with a tool like Qualys.
- Cattle not pets - build new servers from a patched image all the time.
- Containers - Abstract away the underlying OS.
- Serverless - use services where you don't interact with the underlying OS.

- To move away from the multi-network hydra of VPCs:

	1. Main
	2. Audit
	3. Logging
	4. Security Dev
	5. Security Prod
	6. Corp Dev
	7. Corp Test
	8. Corp Prod
	9. AppA Dev
	10. AppA Test 
	11. AppA Stage
	12. AppA QA
	13. AppA Prod
	14. AppB Dev
	15. AppB Test 
	16. AppB Stage
	17. AppB QA
	18. AppB Prod
	19. DevOps Dev
	20. DevOps Test
	21. DevOps Prod

- Remodel your workflow of Dev -> (Test -> Stage -> QA ->) Prod (a few stacks are optional in some applications)

- To a workflow more like Dev locally -> Commit -> CI/CD pipeline [automated unit Testing -> automated Build -> automated stack Validation -> automated Deploy] -> automated blue/green rebalancing (until only the new version is running).

Which reduces you down to:

	1. Main
	2. Audit
	3. Logging
	4. Security Prod
	5. Security is using entirely SaaS products.
		1. Security Dev - new sandbox accounts as needed
	- Corp is using entirely SaaS products.
		2. Corp Dev 
		3. Corp Test
		4. Corp Prod
	- CI/CD pipeline handles these steps. (i.e. Gitlab)
		5. App Dev - develop locally
		- App Repo - group code storage
		6. App Test - automated testing
		7. App QA - more automated testing
		8. App Stage - repo then blue/green deploy
	6. App Prod
		9. App Dev - as above
		- App Repo - as above
		10. App Test - as above
		11. App Stage - as above
		12. App QA - as above
	7. App Prod
	- CI/CD pipeline is entirely SaaS products.
		13. DevOps Dev
		14. DevOps Test
		15. DevOps Prod
(Can't get Markdown to indent correctly here.)

# Trends
[Video](https://www.youtube.com/watch?v=LOpFYMPXqE4)
- Metaverse - build integrations for nontech
- AI - Github copilot. Data science. Create an AI-driven psychic hotline where GPT-3 pretends to be the loved one.
- DB - Relational is popular again. AI in DB like MinesDB, planetscale and supabase make relational easier to work with. Mongo gains serverless and full text search. Redis gains graph, time-series, and full text search. Build a job board specialized for a hot market segment, and get email subscribers.
- JS - Frameworks (React, Angular, Vue) solidify, metaframeworks rise. NextJS and Vercel. React Server Components brings Hydrogen from Spotify. Vercel hires Rich Harris to work on Svelte full time.
	- meta-metaframeworks: WoodsJS built on Next, to build db apps. Astro lets you use multiple frameworks without sending any JS to the client(?).
	- Build tools improved - Vite is much simpler and faster than Webpack. Build a themeforest clone to create custom server-rendered templtaes for e-learning, small business, real estate, etc. 
	- Next already has a template, but you can vary on this. 
	- Since Next is server-based, you can add Stripe or Sendgrid.
- Jetbrains has new IDE
- VSCode.dev has vscode in the browser.
- TailwindCSS gained JIT
- Typescript gains popularity
- JS adds array[i].at() to get the last item or a negative index, standardized top-level await, and better way to check has own property.
- GraphQL won't replace REST and the hype has died off.
- WebAssembly isn't replacing JS, but has like Stackblitz which brings server capabilities to the browser. 
- Mobile: Flutter and React Native


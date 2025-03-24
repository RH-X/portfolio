---
layout: post
title:  "Customer Feedback Pipeline Service Design Project"
#date:   2024-10-18 18:38:16 -0600
categories: jekyll update
---

Introduction:
Case Study Title: TrendTuner / bespoke sentiment analysis tool for scaling user insights for client “Flex Rental Solutions”
Role: Research & UX Design, P.O.C. Web Developer
Timeline: March-April 2025
Context: Flex Rental Solutions inventory management software was initially designed in 2009 for its early adopters, now their higher profile clients. As the company gained wider adoption among the industry, the company scaled up its teams, but there remained no new way to scale the observing and tracking of customer feedback, with certainty that we were driving products with accurate customer data and specific qualitative insights, other than a solo UX Designer.
Goal: The project aimed to evaluate the current streams of qualitative customer insights available in the company and implement strategies that mitigate the risk of inaccurate insights and research synthesis bottlenecks alike, ensuring a more efficient, data-driven design process that can scale to more projects.
Business Opportunities:
Create a customer insights synthesis process that quickly surfaces available customer data to inform more projects, cutting down on the current time it takes to collect and prepare product research ahead of teams designing solutions.
Increase cross disciplinary awareness of customer supporting research by augmenting UX research synthesis expertise, making customer trends digestible, quickly accessible, and more synchronous, in anticipation for human intervention that decides what product decisions are derived from the trend findings. 
Propose something that is of low or no code on others, that also doesn’t pose a large financial burden to entry on the company. (Brief cost analysis surfaced that I could design something using Python libraries and AI prompt engineering to actualize features that are under paywalls of limited free tier tooling for automated user insights engines.)
![Airtable Research Repository Screenshot](/assets/images/your-image.jpg)
Current manually maintained UX Research Repository hosted in Airtable. (The future of catalogued insights that exceed 6 months.)
Vii. Research gathered to validate the problem and get to the root core of the problem; proposed improved service pipeline, iteration I.
	-Facilitated a team discussion to review potential solution to pain points I obtained from quick cross functional QnA sessions with internals involved in the current customer feedback process, and customers’ painpoints. Surfaced the fast points in this service design audit from the research, where I propose an improved no-cost solution to address key issues and had the product teams review and provide feedback. I obtained full team and external team players’ buy-in to inch toward implementation of this new feedback solution. 💡Here’s the kicker: an additional key sentiment was expressed and echoed across the team. I learned that while the improved service pipeline proposed was clocked as a helpful incremental improvement to our pipeline, there was much to be desired in the realm of automation and the team expressed a unanimous ultimate goal to have a more assistive process that freed up time they each currently spent manually obtaining customer research for their product implementations.

🤔This meant I needed to do more research. I now had the questions: “How could I help the team both access and process customer insights more quickly? Could there be a system that’s both attainable within our existing limited company resources that poses the potential scalability to integrate directly into our existing JIRA discovery board space?” 
(I may have omitted the contextual knowledge I have that our company works in agile sprints, creating work tickets using the paid JIRA software.)

Iteration II. Completely something different. I researched paid low code/no code solutions, even attended a meeting with execs at one nearby data tooling company, but found that limited freemium trials on the market would not allow me to create full, end to end proof of concept for my team to evaluate for potential use. I took my question to my own code base with my rusty Python bootcamp knowledge ca. 2018, along with my trusty coding co-pilot ChatGPT-4 to help decode errors.

![Trend Tuner Python Environment Screenshot](/assets/images/your-image.jpg)

Iteration II had begun with real code! This iteration, that I lovingly call “Trend-Tuner,” pulls in user transcripts produced from Google Meet recordings where I’ve conducted live user research sessions with key clients, all placed into my google drive folder. The project accesses my specified drive folder via google cloud API integration with my python project (seen in the screenshot above.) The program then converts the google drive file to a .txt file, so that Python can interpret the qualitative data. 

(At this stage, you see the error, chunking logic and SpaCy library need to be implemented in order for the program to handle more of the long form interview transcripts I had in my designated Google Drive Folder. Out of the box, this project can chunk only by 512 words at a time, and because we want to continue to avoid potential paid tool or API charges as well, we will solve for by just writing a little bit of code.)

This tool also has Monkeylearn LLM integration that has been tested with the sentiment string “I wish I could book my labor roles much faster with this tool.” A phrase from one of my research interview transcripts about our staffing tool. Once chunking logic is implemented, the idea would be to “sentimize” key customer phrases, prioritizing highly negative sentiment mappings. Monkeylearn LLM without further custom prompt engineering having been done, assigns “negative,” “neutral” or “positive” to phrases, then assign a number to communicate the level of severity of the sentiments. Chunking could allow for this type of simple sentiment analysis on longer form qualitative customer data, like these transcripts.

Next steps: solve for the chunking logic and begin mapping out what a topic modeling conversation would look like with the product team, in order to get at the core values, initiatives, and goals currently with the user insights, in addition to prepare my own knowledge base to train custom LLM that understand the information architecture of our software or other topic modeling that is of meaning to the product teams :) 

✨Final design and it’s projected impact pending, per planned team ideation :) Stay tuned.

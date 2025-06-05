# AI-Recommenders-Final-Project

# 🔁  **Feedback Loops in Recommender Systems: Bias, Diversity, and Solutions**

## Authors:
- **Elaina Longjohn**  
  GitHub: https://github.com/elongjohn
  
- **Mills Becouvarakis**  
  GitHub: https://github.com/millsbecouv
  
- **Shields Riggs**  
  GitHub: https://github.com/SWR22

- **Thokozile Munthali**  
  GitHub: https://github.com/Thokozile23
---
## 📊Project Scope

Our project explores the negative impacts of feedback loops in recommender systems, with a particular focus on how they reinforce and amplify popularity bias. A feedback loop occurs when a user's interactions such as clicks, ratings, and engagement are tracked and recorded as data to inform future recommendations.While this type of personalization can enhance user experience, it often creates self-reinforcing cycles where users are repeatedly exposed to similar content. This process tends to favor popular items, allowing the preferences of the majority to dominate while underrepresenting those of minority or niche groups. As a result, recommendation diversity is reduced, and lesser-known or emerging products struggle to gain visibility. 

This not only limits user discovery but also perpetuates existing inequalities in the marketplace.We seek to examine these challenges and propose strategies to reduce popularity bias, ultimately promoting a more equitable recommendation environment, enhancing customer experience, and supporting broader product engagement and long-tail monetization for businesses.We aim to explore this issue from both a technical and ethical standpoint. We will examine how algorithmic design contributes to biased outcomes through a detailed simulation. 

---
## Project Details 📋

### 🔍 Problem Statement
We investigate the major challenge feedback loops in recommender systems create by reinforcing **popularity bias**. Creating a cycle that limits exposure to diverse or niche content. This imbalance not only affects user satisfaction and engagement but also limits growth opportunities for lesser-known creators or products. Our project addresses this issue by simulating how popularity bias evolves and investigating ways to reduce it, with the goal of promoting fairer, more inclusive, and diverse recommendation systems.

The picture below illustrates the feedback loop cycle in recommender systems:

<img src="https://github.com/user-attachments/assets/8792d0c2-a92d-4fe1-af72-2f347b464e42" width="400"/>

**Image source: Zhang et al., 2021*




### 🧠 Research Foundation
Our project is based on a recent academic research focused on identifying and addressing bias in recommender systems. A key paper that informed our work is "**Feedback Loop and Bias Amplification in Recommender Systems**" (2020), published by the ACM Web Conference. This study investigates how feedback loops where user interactions with recommended content, influence future recommendations and can enhance existing biases within the system over time. Several core issues caused by feedback loops are reduced diversity in recommendations, shifts in user preferences, greater homogenization of experiences, and disproportionate impacts on minority users—who often receive less personalized and more biased suggestions. This paper highlights that recommender algorithms often overemphasize popular items due to repeated exposure, reinforcing popularity bias and limiting content diversity.

Our focus was on key concepts particulary **popularity bias**, which arises from feedback loops that cause systems to over-recommend popular items while underexposing niche content. **Feedback loops** form when user interactions reinforce existing recommendations, gradually amplifying bias.

These concepts and challenges directly inspired our project and shaped our approach to identifying and driving change within recommendation systems.

[Link to Research Paper](https://dl.acm.org/doi/abs/10.1145/3340531.3412152)


### 💻 Simulating a Recommender System
To explore how recommender systems evolve and influence content visibility, we built a lightweight simulation that models product engagement over time using cereal brands.

Rather than tracking individual users, our simulation looks at **aggregate interactions**, where recommended products receive popularity "boosts" based on user clicks. This approach highlights how **algorithmic decisions**—even in simplified environments—can create powerful feedback loops.

We simulate and compare two common strategies:
- One that prioritizes high-performing items and reinforces existing popularity.
- One that occasionally introduces less popular items to encourage **exploration**.

This setup helps us visualize the impact of feedback loops on diversity, and explore how small interventions might **promote fairness** and reduce popularity bias in recommender systems.

[Go to Simulation Section](#simulating-a-recommender-system)


### 🌐 Website Demo (GenAI)

We developed an interactive movie recommendation website using ClaudeAI to visually demonstrate how feedback loops in recommender systems contribute to popularity bias. The simulation mimics a user engaging with various types of movie content—especially niche or lesser-known films. Despite this engagement, the "For You" feed continues to prioritize already popular titles, showing how recommender algorithms often override individual preferences in favor of widespread trends.

This behavior highlights how feedback loops restrict content diversity, reinforce the visibility of mainstream items, and make it increasingly difficult for underrepresented or new content to gain traction. The website serves as both a learning tool and a prototype environment to explore interventions that could promote fairer, more inclusive recommendation outcomes.

Link to our website can be found below:

[Go to Website Section](#website-demo-popularity-bias-in-action)


### 🗂️ Project Management: GitHub Kanban Board

To effectively manage and track the progress of our project, we utilized a GitHub Project Board. This tool allowed us to break down our tasks into clear, actionable categories, helping ensure transparency, collaboration, and accountability throughout the project. Our board was organized into several key sections, each representing different stages of the project workflow:

[View our Kanban board](https://github.com/users/Thokozile23/projects/8)


### 💼 Business Implications
Recommender systems have a significant impact on business by enhancing personalization, boosting customer engagement, and driving sales. However, they also present challenges, including popularity bias, reducing content diversity, and ethical concerns around data privacy. To use them effectively, businesses must understand how these systems work and ensure their implementation aligns with strategic goals.

[Go to Business Implications Section](#Business-Implications)


### 🤖 Responsible AI Considerations
Recommender systems can unintentionally reinforce popularity bias, limit content diversity, and raise ethical concerns around user privacy and manipulation. We explore these risks and highlight simple strategies like boosting diversity, improving transparency, and minimizing data use.

[Go to Responsible AI Section](#Responsible-AI-Considerations)

### 🚀 Future Developments

- Improve diversity in recommendations.
- Let users customize recommendation settings.
- Explore privacy-first AI (e.g., federated learning).
- Show transparent metrics on how suggestions are made.

[Go to Future Developments Section](#Future-Developments)


### 📚 References

Our project is grounded in recent work highlighting how recommender systems amplify bias through feedback loops. These systems tend to favor popular content, often at the expense of diversity and fairness.

We explored multiple peer-reviewed studies, including:
- A simulation framework for bias amplification in recommender systems
- Guidelines for aligning recommender design with European AI regulations
- A tutorial on identifying and mitigating common algorithmic biases

[See full References](#References)

---
## Simulating a Recommender System

To explore how feedback loops influence recommender systems—especially in reinforcing popularity bias and limiting diversity—we designed two contrasting models that simulate different algorithmic behaviors. These models help illustrate how small design decisions can significantly impact the visibility and variety of recommended content.

### 1. Dataset & Setup

We use a simulated dataset of cereal brand "products," each assigned a randomized popularity score at initialization. This abstract representation allows us to mimic user-item interactions without relying on real-world user identifiers or behavior logs. The controlled setup isolates the effects of algorithmic feedback loops, giving us clearer insight into how certain recommendation strategies can either narrow or expand content diversity over time.

### 2. Feedback Loop Simulations

We created two models to compare behavior:

- **Model A: No Exploration**  
  - Recommends the top 4 products repeatedly based on their score.  
  - Reflects a pure exploitation strategy, where popular items are reinforced through repeated exposure.  
  - Simulates how recommender systems naturally favor already-popular content, limiting visibility of lesser-known items.

- **Model B: With Exploration Boosts**  
  - Recommends the top 4 products, but also adds small temporary boosts to 2 low-performing products each round.  
  - Encourages exploration by breaking the cycle of popularity reinforcement.  
  - Simulates efforts to promote diversity by periodically surfacing less popular or emerging items.

➡️ **[Run the simulation → Final Project Sample Code.py](./Final_Project_Sample_Code.py)**

### 3. Visualization

The simulation plots how each product's score evolves over 20 iterations.  
- In **Model A**, the same few products dominate over time due to constant reinforcement.  
- In **Model B**, more products stay in circulation thanks to occasional boosts, resulting in a more balanced and diverse recommendation landscape.

### Model A: Feedback loop without exploration
<img src="https://github.com/Thokozile23/Final-Project/blob/9792dc84ddb20e6288ccb672ad4979e9873934b6/feedback%20loop%20without%20exploration.png?raw=true" alt="Alt Text" width="700"/>

### Model B: Feedback loop with exploration 
<img src="https://github.com/Thokozile23/Final-Project/blob/5ffa8a2cdf6237d209c1a92abf7588b606756a5d/exploration%20picture%20improved.png?raw=true" alt="Alt Text" width="700"/>


---

## Website Demo: Popularity Bias in Action

We developed an interactive simulation using **ClaudeAI** to showcase how popularity bias manifests in recommendation systems. To initiate the build, we provided ClaudeAI with a structured prompt detailing the desired functionality and user experience. The prompt included specific instructions for simulating a movie recommendation system and highlighting popularity bias:

"Create a simple interactive website simulation for movie recommendations. Use real movie titles in a grid layout. Each movie has an initial "popularity" (views or likes). Users can click to "like" movies. The system then updates the user's profile and shows more popular movies in recommendations, reinforcing a popularity bias. Include a visual feedback loop showing how user interactions shape the recommendations over time. Add a bar graph tracking popularity changes of popular vs. niche movies. Also, show how niche movies get recommended less even if they match the user profile. Include simple controls to set how many likes a user gives, and simulate different user profiles (mainstream vs. niche). Keep the UI and logic very simple, ideal for a simulation or classroom demo."

The simulation operates as follows:

- Users simulate interacting with movies by clicking on them.
- Despite repeated clicks on niche movies, the system heavily favors **popular content** in its "For You" feed.
- Niche items take a long time—and significantly more engagement—to surface in recommendations.
- This demonstrates how feedback loops reinforce already-popular items, making it harder for diverse or underrepresented content to gain visibility.

🔗 [Try the Demo – Popularity Bias & Feedback Loops Simulation](https://claude.site/artifacts/ccbba4e1-d462-4835-a628-b096dd31fec1)

The tool highlights how recommender systems can unintentionally limit discovery and diversity, even when user preferences shift toward niche interests.

---

## Business Implications

### Role of Recommenders 
Recommender systems play a vital role in modern business, influencing everything from online shopping and entertainment choices to chatbots and fantasy sports. As technology continues to advance, their significance in daily life and business strategy cannot be overstated. Companies depend on these systems to deliver personalized, data-driven suggestions that help users make informed decisions—whether about purchases, customer engagement, or even lifestyle changes. 

### Business Applications
Exceptional recommender systems are the foundation of some of the biggest businesses in the world including Amazon, Netflix, and Google, which help them generate a combined market cap of over $4.16 trillion. Companies use recommender systems to understand customers, their preferences, and their tendencies, so that they can enhance the services they provide to that customer. These insights enable businesses to deliver personalized experiences, increase customer retention, and drive revenue growth through more targeted offerings. Knowing how to use recommenders and what they do can be a game-changing tool for businesses, big or small. Understanding how recommender systems work and how to leverage them can be a transformative asset for businesses of any size. However, it's important to recognize their limitations. 

### Limitations of Recommenders 
Recommenders aren’t always fair, they inadvertently reinforce existing biases, shaping perceptions that can change how a person sees a product or business, leading to favoritism or exclusion. Therefore, businesses must carefully weigh the benefits against the risks and make thoughtful decisions about their implementation. Recommenders are here to stay and regardless of the challenges that they propose. To remain competitive and customer-focused, businesses need to understand what recommenders are, how they function, and how best to use them in alignment with their goals. 


### Keys to Successful Business Utilization and Integration: 
  1. **Understand the Technology:** Have a clear understanding of how recommender systems work in order to leverage them effectively.

  2. **Strategic Alignment:** Determine how you want to use recommenders in ways that align with broader business and organizaional goals.

  3. **Data-Driven Insights:** Use recommender systems to deliver tailored, insightful suggestions that enhance customer decision-making and engagement.

  4. **Be Aware of Bias and Limitations:** Recognize and address the inherent biases and consumer concerns in recommender systems to avoid bias and ethical issues.

  5. **Balanced Evaluation:** Thoughtfully weigh the advantages of recommenders versus the potential risks to ensure effective and ethical implementation.




<img src="ChatGPT%20Image%20Apr%2013%2C%202025%2C%2011_23_35%20PM.png" alt="Simulation output showing business implications" width="500"/>

*Figure: Visualization generated using ChatGPT to illustrate business implications in recommender systems.*

---

## Responsible AI Considerations

### System Biases

Understanding the biases present in recommender systems (RSs) is crucial, as these biases can significantly impact the fairness, accuracy, and trustworthiness of recommendations. The biases within RSs can be categorized into four main types: data biases, cognitive biases, position/presentation biases, and algorithmic/model biases.

- **Data Bias:**
Data bias occurs when training data is unbalanced or not fully representative of all users. This can lead to recommendations that overlook certain demographic groups and reinforce existing inequalities.

- **Cognitive Bias:**
Cognitive biases stem from human mental shortcuts that shape how users interact with the system. Effects like anchoring or recency can cause users to favor initial or recent items over more relevant ones.

- **Position/Presentation Bias:**
This bias arises from how recommendations are displayed, with top-listed items receiving more attention. Even if less relevant, their placement can skew user choices and overall system effectiveness.

- **Algorithmic/Model Bias:**
Algorithmic bias is rooted in how models are built and trained, often reflecting the flaws in their data. These biases can reinforce stereotypes or overemphasize certain user patterns, limiting diversity in recommendations.


![image](https://github.com/user-attachments/assets/13ef7933-f24c-44c1-8fe7-18e8f9aefaed)

**Image Source: Di Noia et al., 2022, p. 70*

### Ethical Concerns

-  **Balance Between Diversity and Relevance:**
Striving for diversity might lead to recommendations that feel irrelevant or forced, potentially frustrating users.

-  **Algorithmic Manipulation:**
Overcompensation for popularity bias could be exploited by other people or businesses to artificially amplify niche or low-quality content.

-  **Transparency Issues:**
Users may not fully understand adjustments made to recommendations, raising concerns about opacity in how content is prioritized.

- **Bias Trade-Offs:**
Correcting one form of bias (popularity) might unintentionally introduce new biases, such as favoring specific minority groups over others.

---

## Future Developments

### 1. **Integrate Enhanced Diversity Algorithms**
Continued refinement of algorithms to ensure even greater inclusion of underrepresented or niche content, allowing for tailored recommendations that go beyond mainstream preferences.

### 2. **Implement User Customization Options**
Provide users with more tools to adjust recommendation settings (e.g., adjusting for diversity or prioritizing specific interests) to empower individual agency.

### 3. **Explore Ethical AI Practices**
Lead by example by integrating cutting-edge, privacy-preserving machine learning techniques, such as federated learning, to minimize invasive data collection.

### 4. **Offer Transparent Metrics**
Develop a dashboard to display how recommendations are generated, showcasing the balance between popularity, diversity, and user preferences.


---
### What's Next? Help us Envision the Future of Recommenders!

---
---

## References

- **Mansoury, M., Abdollahpouri, H., Pechenizkiy, M., Mobasher, B., & Burke, R. (2020).**  
  *Feedback Loop and Bias Amplification in Recommender Systems*.  
  In *Proceedings of the 29th ACM International Conference on Information & Knowledge Management (CIKM '20)*, pp. 2145–2148.  
  [https://doi.org/10.1145/3340531.3412152](https://doi.org/10.1145/3340531.3412152)  
  **Summary:** Explores how recommender systems amplify bias through feedback loops, and proposes a simulation framework for offline analysis.

- **Di Noia, T., Tintarev, N., Fatourou, P., & Schedl, M. (2022).**  
  *Recommender Systems under European AI Regulations*.  
  *Communications of the ACM*, 65(4), 69–73.  
  [https://doi.org/10.1145/3512728](https://doi.org/10.1145/3512728)  
  **Summary:** Discusses the impact of European AI regulation on recommender systems, highlighting transparency, fairness, and accountability.

- **Chen, J., Wang, X., Feng, F., & He, X. (2021).**  
  *Bias Issues and Solutions in Recommender System: Tutorial on the RecSys 2021*.  
  In *Proceedings of the 15th ACM Conference on Recommender Systems (RecSys '21)*, pp. 825–827.  
  [https://doi.org/10.1145/3460231.3473321](https://doi.org/10.1145/3460231.3473321)  
  **Summary:** Provides a tutorial-style overview of biases in recommendation systems and outlines methods for mitigating them to improve fairness.

### Supplemental Information
- **CBC: Does AI Actually Make Money** -- https://www.cbc.ca/news/business/ai-generative-business-money-revenue-1.7264014
- **Bain: Which Countries & Industries Are Getting the Most Out of Generative AI** -- https://www.bain.com/insights/which-industries-and-countries-are-getting-the-most-out-of-generative-ai-snap-chart/
- **American Marketing Association: When to Trust AI Recommenders** -- https://www.ama.org/2020/11/24/when-consumers-trust-ai-recommendations-or-resist-them/ 
- **Forbes: How Recommenders Elevate Support Experiences** -- https://www.forbes.com/sites/sap/2024/11/26/how-ai-driven-recommenders-elevate-support-experiences/
- **Mordor Intelligence: Fantasy Sports Market** -- https://www.mordorintelligence.com/industry-reports/fantasy-sports-market 
- **Fortune Business Insights: FinTech Market Overview** -- https://www.fortunebusinessinsights.com/fintech-market-108641
- **Mordor Intelligence: FinTech Market** -- https://www.mordorintelligence.com/industry-reports/us-fintech-market 



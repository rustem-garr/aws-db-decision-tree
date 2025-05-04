# AWS Database Service Selection

Visual decision tree to help choose the right AWS database service based on use case requirements such as production vs. prototype, need for transactions, scaling, and more.

![AWS DB Options Diagram](./AWS%20DB%20Options%20diagram%20image.png)

## 📺 YouTube Explanation

Walkthrough of the diagram:  
👉 [YouTube video](https://www.youtube.com/watch?v=3N7nU8ip-nI)

---

## 🧭 Step-by-Step Explanation

1. **Prototype or Production?**  
   - If you're just testing or building a quick demo: choose **Prototype** → go with **RDS MySQL or PostgreSQL** (unmanaged).
   - If you're launching a live application: choose **Production** → continue to next question.

2. **Need Relations?**  
   - If your data is relational (tables with foreign keys, SQL): choose **Yes** → go to next step.
   - If not: choose **No** → go to *Text-Based Search* decision.

3. **Unmanaged or Managed?**  
   - **Unmanaged**: You want to manage the database yourself (e.g., EC2-hosted DB) → go with **RDS MySQL or PostgreSQL**.
   - **Managed**: Let AWS handle updates, backups, etc. → continue.

4. **Consistent Traffic?**  
   - **Yes**: Pick **Aurora RDS** – great for high performance with steady load.
   - **No**: Choose **Aurora Serverless** – good for variable or unpredictable workloads.

---

5. **Need Text-Based Search?**  
   - **Yes**: Choose **Elasticsearch or CloudSearch**.
   - **No**: Continue to next question.

6. **Need Transactions?**  
   - **No**: Choose **ElastiCache** – best for caching and real-time data access.
   - **Yes**: Continue to next step.

7. **Ease of Use or Scale?**  
   - **Ease of Use**: Choose **DocumentDB** – MongoDB-compatible, easy for developers.
   - **Scale**: Choose **DynamoDB** – serverless, ultra-scalable key-value NoSQL DB.


---

Elasticsearch, CloudSearch, and ElastiCache alone are usually not enough, so in real-life use cases you need a primary data store (NoSQL or relational) as well - which isn’t shown in the diagram.

Feel free to fork, contribute, or suggest improvements.  
Happy building on AWS!

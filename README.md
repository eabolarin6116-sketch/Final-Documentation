# Final-DocumentationMIT 8103 Advanced Database Systems — Final Portfolio Summary
Academic Session: 2026/2027
Semester: First Semester
Case Study: Bank/Fintech Platform
Student Name:  Abolarin  Emmanuel  Temitope
GitHub Repository: [Insert your repository URL]

1. Introduction and Project Overview

This portfolio explores database design, query optimisation, transaction management, NoSQL data modelling, and cloud database concepts through a Bank/Fintech Platform case study. The system models customers, accounts, deposits, withdrawals, transfers, and transaction logs.
The main objective was to apply database concepts to a financial application where data integrity, transaction correctness, performance, and reliable access to information are important. PostgreSQL was used for the relational implementation, while MongoDB was used to demonstrate a document-oriented data model. Hosted database services allowed the practical exercises to be completed through web-based environments.

2. Summary of the Five Portfolios

Portfolio 1: Database Design and Modelling

The first portfolio established the database design for the Bank/Fintech Platform. It documented the case study, entities and attributes, relationships, entity-relationship diagram, relational schema, keys, constraints, and normalisation.
The relational design includes customers, accounts, transactions, transaction logs, and transfers. Primary keys identify records, foreign keys represent relationships, and constraints enforce selected business rules, such as valid transaction types and non-negative account balances.
This portfolio provided the foundation for implementing and testing the database.

Portfolio 2: Query Processing and Optimisation

The second portfolio explored SQL queries, execution plans, indexes, and query performance. Queries were executed against the PostgreSQL database, and EXPLAIN (ANALYZE, BUFFERS) was used to inspect execution plans.
Single-column and composite indexes were created and evaluated. The recorded plans did not show clear use of the newly created indexes for the tested queries, and the measured execution times did not establish a performance improvement. The small demonstration dataset limits the conclusions that can be drawn.
The exercise demonstrated the importance of examining execution plans and using measured evidence rather than assuming that adding an index will automatically improve performance.

Portfolio 3: Transactions and Concurrency
The third portfolio examined transaction control, rollback, isolation, and concurrency management. Practical exercises included checking transaction outcomes, testing rollback, using row locks with SELECT ... FOR UPDATE, and demonstrating repeatable-read isolation with two database sessions.
During the repeatable-read exercise, one session continued to observe its earlier balance while another session committed an update. The balance was subsequently restored to the intended test value.
These exercises demonstrated how transaction boundaries, isolation levels, and locking can help manage concurrent operations. Financial transfers require particular care to ensure that related debit and credit operations are handled consistently.

Portfolio 4: NoSQL and Advanced Data Models
The fourth portfolio used MongoDB Atlas to implement a document-oriented model. A bank_fintech database and transactions collection were created, and sample documents representing a deposit, withdrawal, and transfer were inserted.
Queries were used to retrieve successful transactions and filter deposit transactions. The accompanying documentation evaluates the flexibility of document storage and compares it with the relational PostgreSQL design.
The project recommends PostgreSQL for core account and financial transaction operations, with MongoDB as a possible complementary store for flexible transaction-history data where the application's requirements justify it.

Portfolio 5: Distributed and Cloud Database Exercise
The fifth portfolio documented the use of hosted PostgreSQL on Neon and MongoDB Atlas. It examined the potential roles of replication, sharding, availability, and consistency in a financial database system.
The project demonstrates the use of hosted database environments. It does not claim that replication, sharding, failover, or disaster recovery were independently configured and tested. These mechanisms are discussed as design considerations requiring further verification.

3. Evidence and Repository Organisation
The GitHub repository contains the five portfolio folders and a main README. Each portfolio contains supporting documentation and, where applicable, implementation evidence.

The evidence includes the ER diagram, schema and constraints documentation, SQL query and execution-plan screenshots, transaction and isolation test results, MongoDB documents and query results, and cloud deployment documentation.

Repository URL: [Insert your full GitHub repository URL]


4. Individual Reflection
Working on this project helped me develop my understanding of how database theory applies to a financial application. I progressed from designing a relational model to implementing SQL operations, testing transaction behaviour, examining execution plans, and exploring document-oriented storage.

One important lesson was that database behaviour must be verified using actual results. For example, creating indexes did not automatically produce a measurable performance improvement in the tested queries. The transaction exercises also showed why rollback, isolation, and concurrency control matter when account balances are updated.

The project improved my practical familiarity with PostgreSQL and MongoDB and helped me recognise that different database models have different strengths and limitations.

Personal reflection to complete: 

The major challenge was understanding what was expected and how to use the various platforms required because i have not familiar with the platforms. The task helped me understand how to interact with the various platforms and if i am to repeat the project,i will be faster in term of execution.

5. References and AI-Use Declaration
List the documentation, learning resources, and other sources actually consulted during the project. Use the referencing style required by the course.

AI-use declaration: 
ChatGPT - helped plan the portfolio, draft the case study, entities, business rules, ER diagram, SQL and helped troubleshoot execution.

6. Conclusion
The five portfolios collectively demonstrate database design, SQL implementation, query-plan analysis, transaction and concurrency exercises, NoSQL data modelling, and cloud database concepts within a consistent Bank/Fintech Platform case study.
The practical results and supporting documentation provide evidence of the work completed, while the analysis identifies limitations and areas for further investigation. Together, these exercises demonstrate the importance of sound database design, data integrity, evidence-based optimisation, transaction correctness, and careful consideration of database deployment choices.

## Requirements -- Business Requirements

In the eyes of business stakeholders, all decisions are justified by their return on investment. The company's KPIs for the implementation of AI are as follows;
Reduced manual processing time. By deploying a Retrieval Augmented Generation system with human focus on safety and monitoring, the time saved on manual content safety checks and filtering scales with the size of operations and data output. This accelerates the time-to-market for any product enabled by AI or ML processes. 
Increased operational efficiency. By optimizing prompt construction and data retrieval systems, the correct insights can be arrived at faster, leading to better decision making capabilities by both employees and those charged with governance

## Requirements -- Functional Requirements 

The company wants to deploy a self-hosted model for the following reasons:
    Greater degree of control and customization 
    Security of clientele and customer data 
    Storage and operations scalability 
    Lower costs in the long run (5 years onwards) as recurring subscription fee waived
Specific hardware requirements depends on stakeholder specifications, but will need four areas of consideration 
    GPU server (inference) hardware (Primary Config)
    CPU Servers for orchestration and processing
    Storage and networking infrastructure 
    Environmental requirements for power, cooling, and physical space 

## Requirements -- Non-functional Requirements 

1. Performance!
    Response time > 2 seconds for standard requests 
    Support for concurrent users 
    Minimal latency for Real Time operations 
    Efficent resource utilization 

2. Scalability 
    Ability to handle peak loads
    Ability to improve operations as simultaneous user presence increases 

3. Security 
    Presence of end-to-end encrption 
    Auditing presence (external party or local staff)
    Data masking and anonymization where necessary 

## Requirements -- Tooling 

Choice of tooling corresponds directly to company needs. They want to ensure increased productivity and decreased costs, yet a high level of reproducibility in output. 
As such, Partial Automation is used with AutoML tools 
Platform selected will automate the process of model selection, hyperparameter tuning, and training. ML actions will include huamn oversight with data related activity, like wrangling, labelling, augmentation, and engineering. 
This ensures fast, accurate, and safe insights for company usage. Prevents potential AI Bias or hallucinations, as well as data drift. 

## Risks 
We have three prime concerns with regards to AI implementation risk 
1. Data privacy: Poor protection of sensitive information can endanger the project and the sanctity of the company. This can be mitigated with the appropriate use of caches, guardrails, and wise infrastructure architecting. 
2. Performance degradation: Under high load, performance of the GenAI model can deteriorate. Concurrent usage, potential peak usage, number of requests a day, and average request size must be considered when designing the infrastructure. Company to consider leveraging on cloud platforms, or opening access to specialized hardware.
3. Unfair outcomes/Bias: Open source models tapping into the internet can pull misleading data, causing the output to be inaccurate

## Assumptions 

During implementation, we would assume that the model will maintain a certain level of repeatability to its queries. 
However, any attempts to train the model on new data may skew outputs away from its original quality. 
Even on the same training data set, consistency of output depends on a number of variables that might be difficult to control in a fast-paced office environment. 
For example, complexity of input, degree of context construction from user, domain specific nuances, insufficient data for outlier use-cases, or even differences in interpretation of output. 
With this in mind, we should probably train the model on a wide variety of use cases in varied scenarios before deployment, and monitor it closely after deployment. 


## Constraints

Based on the GenAI architecturing provided in GenAI Architecturing.png, the company might face a few non-negotiable restrictions. The largest one being compliance with local data protection laws and jurisdictions that limit the degree of data transfer, processing, storage, and model operations. For example, private information from a user cannot be fed into the LLM. 
Response latency constraints might also be an issue, supposing 
# FedLearn | Hackmos 2024
**Privacy-preserving ML Model Training on Warden.**

## Problem Statement
Large amounts of data remain untapped in machine learning due to pressing privacy concerns. While federated learning addresses this issue by allowing data to stay with users, its substantial hardware requirements often render participation economically unviable for many. Consequently, valuable data across various domains, including healthcare, finance, and personal information, goes unused. This not only hinders advancements in critical fields but also highlights the urgent need for solutions that enable secure data utilization without compromising privacy.

## FedLearn Non-technical Overview

**FedLearn** is an innovative federated learning platform designed to facilitate the secure and efficient training of machine learning models using decentralized technologies. Leveraging the Warden Protocol and the Akash network, FedLearn empowers ML Model Owners to offer their ML tasks in a marketplace, allowing users to submit data for training without compromising privacy. FedLearn combines cutting-edge technology with robust privacy measures, offering a scalable solution for collaborative ML model training in a decentralized environment.

**Notable Features:**

- **Decentralized Marketplace:** FedLearn provides a transparent marketplace for model owners and users, enhancing collaboration and accessibility in the ML ecosystem.

- **Asynchronous Compute Provisioning:** Utilizing Warden Protocol's FUTURES, FedLearn can asynchronously provision compute environments on the Akash network, allowing long-running ML training processes to occur without burdening the blockchain.

- **Enhanced Privacy:** By employing federated learning principles, FedLearn ensures that user data remains on local devices, only sharing model updates, thus maintaining strict privacy standards.

- **Automated Workflows:** The integration of the x/act module enables automated execution of tasks based on predefined triggers, streamlining operations and improving overall efficiency.







### FedLearn Components and Users

- **ML Model Owners:** ML Model Owners aim to train machine learning models that often require large amounts of sensitive data. They seek access to diverse datasets to enhance their models' performance and effectiveness across various applications.
- **Fed Users:** Fed Users are participants in federated learning systems who possess sensitive data but prefer not to disclose it. They receive ML models from Model Owners, train these ML models using their data, and submit the enhanced ML models back to the ML Model Owners.
- **FedLearn Marketplace:** The FedLearn Marketplace enables ML Model Owners to list federeated learning jobs that Fed Users can select to train the ML models and earn rewards.
- **FedLearn Pods:** FedLearn Pods are open-source Kubernetes pods for ML model training that can be verified by Fed Users through Cosign. Fedlearn Pods provide a trusted compute environment on the Akash Network, allowing Fed Users to confidently submit their data. Fed Users can select the compute provider on the Akash Network hosting their FedLearn Pod to further ensure trust.
- **FedLearn Commons:** FedLearn Commons are publicly available base ML models (e.g., LLMs) collaboratively trained by the community, offering ML Model Owners high-quality models and reducing individual training costs.

## FedLearn Technical Overview

### Principal Workflow
![alt text](/concept/01_technical_overview.png)

### Detailed Workflow
![alt text](/concept/02_workflow.png)

### Warden Integration
- **x/act:** Using the x/act module, FedLearn executes actions—such as instantiating secure compute instances and managing model updates—on connected chains based on triggers like training initiation, data submission, and task completion. This automation ensures efficient and timely responses to reduce computation costs.
- **x/warden:** FedLearn uses the x/warden module is used to manage keys that trigger transactions on the Akash Network, enabling the asynchronous commissioning and decommissioning of compute environments when federated ML model training is initiated or completed.
- **Warden Futures Handler:** FedLearn leverages Warden's FUTURES to asynchronously provision compute environments on the Akash network and conduct ML model training. This  enables FedLearn to initiate long-running training processes while receiving callbacks upon completion to verify the improvements in the ML models.



### Frequently Asked Questions (FAQs)

1. **What is FedLearn?**  
   FedLearn is a federated learning platform that enables secure and efficient training of ML models while preserving user data privacy. It operates on the Warden Protocol and integrates with the Akash Network.

2. **How does FedLearn ensure data privacy?**  
   FedLearn allows users to maintain full control over their data by processing their data on verified open-source FedLearn Pods that are operated on user-choosen and trusted compute environments. Only ML model updates are shared, ensuring sensitive data is never disclosed.

3. **What are FedLearn Pods or trusted compute environments?**  
   FedLearn Pods are trusted compute environments on the Akash Network that users can choose and verify for training ML models based on their data. This ensures that their data is handled securely and reliably.

4. **Do I need to invest in hardware to use FedLearn?**  
   No, FedLearn eliminates the need for expensive compute hardware. FedLearn leverages the Akash Network for scalable and affordable computing resources.

5. **How does the payment system work?**  
   FedLearn utilizes micropayments, allowing users to be rewarded for ML model training in small increments. This makes it cost-effective and scalable, accommodating various data amounts, even small amounts.

6. **Who can benefit from using FedLearn?**  
    FedLearn is advantageous for organizations and individuals across various fields, including healthcare and finance, who wish to train ML models while keeping their data private. By doing so, FedLearn can access a vast amount of data that would otherwise remain untapped.

7. **How is ML model training executed in FedLearn?**  
   Users receive ML models from model owners, train them using their private data in a trusted environment, and then submit the improved models without sharing their data. The process of creating FedLearn Pods, awaiting model training, and verifying ML model improvements is handled by FedLearn smart contracts on Warden.

8. **Can I verify the security of the compute environments?**  
  Yes, users can verify the security of trusted compute environments through Cosign. FedLearn Pods are open-source and signed by the FedLearn Foundation, ensuring the integrity of the FedLearn Pod. Users can verify these signatures to confirm that the environments are trustworthy and compliant for processing sensitive data. This process provides confidence in the security of the compute setup.
  
9. **How does FedLearn handle model updates?**  
    Upon completing ML model training, FedLearn utilizes the FUTURES Handler of the Warden Protocol to submit the updated models back to the ML Model Owners. This process allows for the evaluation of model improvements while rewarding Fed Users for their contributions to successful ML model enhancements.












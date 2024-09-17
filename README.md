# RAGSync: All in one solution for all rag based usecases for log Files!

## Setup: 

### 1. Clone to the repo and install the requirements: 
```
git clone https://github.com/YaeshwanthUrumaiya/RAGSync.git

pip install -r requirements.txt
```

### 2. Select between GROQ and AWS Bedrock. 

#### 2.1. AWS Bedrock:
2.1.1. Go to the aws console and select AWS Bedrock. (Note: Make sure your region is in a region that supports the models that you want to use. By default, I'm using ap-south-1)

2.1.2. Under Bedrock configurations tab, select Model Access. 

2.1.3. Mulitple models are present. Press "Available to request" of the model of choice and then you should be able to access the model. (By default, using Amazon Titan Text G1 Lite and Llama3 8B Instruct)

2.1.4. Go to IAM, create a user with AmazonBedrockFullAccess Permission. 

2.1.5. Get the secret and access key of the user and store it in a .env file within the working directory under the names: AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY

#### 2.2. GROQ:
2.2.1. Go to site: console.groq.com/key

2.2.2. Make an account and create an api key and store it in a .env file within the working directory under the name: GROQ_API_KEY

### 3. To Include Documents: 
Create a folder named "Data" within the working directory and within that, create two folders named "SupportingDoc" and "RawData" and drop your supporting documentation into the "SupportingDoc" folder and drop the log files into the "RawData" folder.

### 4. Run the code: 
Run the ipynb block by block. Several choices can be made within the ipynb file to fine tune the application to your needs. Read the comment blocks within the file to understand the codebase and make these choices!

# Versions: 
V.1 -> Basic RAG-LLM Application within the ipynb format. 
V.2 -> Adding Supporting Documentataion Support (Answering and Questioning) within the ipynb format.

# TO DO: 
1. To implement MultiQuery Retriever.
2. Include steamlit support maybe?
3. Include whl to ship it.

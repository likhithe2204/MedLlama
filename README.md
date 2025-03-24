# likhithe2204-End-to-End-Medical-Chat-Bot-using-Llama-2

## Steps to run the project 

```bash
conda create -n mchatbot python=3.8 -y
```

```bash
conda activate mchatbot
```

```bash
pip install -r requirements.txt
```

# Step 4: Set up Pinecone credentials (Create .env file)
```bash
echo 'PINECONE_API_KEY="your_pinecone_api_key"' >> .env
echo 'PINECONE_API_ENV="your_pinecone_api_env"' >> .env
```

# Step 5: Download Llama 2 quantized model
```bash
mkdir -p model
cd model
wget https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/resolve/main/llama-2-7b-chat.ggmlv3.q4_0.bin
cd ..
```

# Step 6: Store index
```bash
python store_index.py
```

# Step 7: Run the chatbot application
```bash
python app.py
```

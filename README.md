#!/bin/bash

# Create repository structure
mkdir -p IntegratedAI/data
touch IntegratedAI/core.py
touch IntegratedAI/JA1.py
touch IntegratedAI/OS1.py
touch IntegratedAI/EX1.py
touch IntegratedAI/run_demo.py
touch IntegratedAI/requirements.txt
touch IntegratedAI/data/long_term_memory.db

# Write requirements
cat > IntegratedAI/requirements.txt <<EOL
torch>=2.0.0
transformers>=4.30.0
sentence-transformers>=2.2.0
faiss-cpu>=1.7.0
numpy>=1.24.0
google-generativeai>=0.3.0
sqlite3>=3.0.0
nest_asyncio>=1.0.0
EOL

# Initialize git repo
cd IntegratedAI
git init
git add .
git commit -m "Initial commit - Integrated AI System"

echo "Repository setup complete. Install dependencies with:"
echo "pip install -r requirements.txt"

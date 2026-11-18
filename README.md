# HR Attrition DSS + RAG AI HR Consultant

Streamlit decision-support app that predicts employee attrition (XGBoost / Random Forest, SMOTE, SHAP)
and generates policy-grounded retention strategies using RAG (Groq Llama-3 70B + local HuggingFace embeddings + Chroma).

## Setup
```bash
pip install -r requirements.txt
export GROQ_API_KEY=gsk_...        # free key from console.groq.com
```
Put your policy PDF at `data_docs/hr_policy_manual.pdf`, and the trained model `.pkl` files next to `app.py`
(generate them by running the notebook in `notebooks/`).

## Run
```bash
streamlit run app.py
```

## Notes
- Requires Python 3.10+ (tested on 3.12 / Google Colab).
- Never commit your API key; use env vars or Colab Secrets.

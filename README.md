# Supabase PostgreSQL Python Tutorial (AWS SageMaker Edition)

A beginner-friendly, end-to-end tutorial for using **Supabase as your PostgreSQL backend**, and **AWS SageMaker Notebooks** as your Python frontend.

---

##  Goal

You’ll learn to:
- Set up a Supabase PostgreSQL database
- Connect to it from AWS SageMaker
- Create, query, and manage data in notebooks
- Deploy data workflows in a real cloud environment

---

##  Project Structure

```
supabase-postgresql-python-tutorial/
├── notebooks/                # Jupyter notebooks to run in SageMaker
├── config/                   # config.py holds your Supabase credentials
├── scripts/                  # helper setup + test scripts
├── data/                     # sample data (CSV)
├── docs/                     # setup guides
├── requirements.txt          # Python packages needed
├── README.md                 # You’re reading it
```

---

##  How to Run in SageMaker

###  Step 1: Launch a SageMaker Notebook Instance

1. Sign in to [AWS Console](https://console.aws.amazon.com/)
2. Open **SageMaker > Notebook Instances**
3. Click **Create notebook instance**
4. Fill in:
   - Name: `supabase-demo`
   - Instance type: `ml.t2.medium`
   - IAM Role: Create a new one with S3FullAccess
5. Wait for status to turn **InService**
6. Click **Open Jupyter**

---

###  Step 2: Upload This Project

1. Download the ZIP file from this repo
2. Upload and unzip inside Jupyter
3. Open `notebooks/01_getting_started.ipynb`

---

###  Step 3: Install Dependencies

Run in a new notebook cell:

```python
!pip install -r requirements.txt
```

---

##  Supabase Setup

Follow [docs/00_supabase_setup.md](docs/00_supabase_setup.md) to:
- Create Supabase project
- Get your API keys
- Paste them into `config/config.py`

---

##  Run the Tutorial

1. Start with `01_getting_started.ipynb`
2. Then explore future notebooks: CRUD, real-time, deployment

---

##  Troubleshooting

- See [docs/troubleshooting.md](docs/troubleshooting.md)

---

##  License

MIT

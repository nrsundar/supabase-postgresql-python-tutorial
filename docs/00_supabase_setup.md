# Step 0: Supabase Setup

This guide walks you through creating your Supabase project and configuring it for use with this tutorial.

---

## 🔧 1. Create a Free Supabase Account

Go to [https://supabase.com](https://supabase.com) and sign up using GitHub or email.

---

## 📦 2. Create a New Supabase Project

1. Click “New Project”.
2. Choose an organization (or create one).
3. Set:
   - **Project Name** (e.g., `demo_project`)
   - **Database Password** (remember this!)
   - **Region** (closest to you)
4. Click **“Create new project”**.

Wait 1–2 minutes for the project to be provisioned.

---

## 🔑 3. Get Your API Keys

Go to your new project's **Settings > API**:

- **Project URL** (e.g., `https://your-project.supabase.co`)
- **anon public key** (not the service role key!)

---

## 🔐 4. Enable Extensions (Optional but Recommended)

In the Supabase SQL editor, run:

```sql
create extension if not exists "uuid-ossp";
```

---

## 🔓 5. Enable RLS (Row-Level Security)

When creating tables, Supabase uses **Row Level Security** by default.

To test freely, run this policy after creating any table (via SQL editor):

```sql
-- Enable RLS
alter table users enable row level security;

-- Allow full access
create policy "Allow all" on users
  for all using (true);
```

---

## 🧾 6. Add Your Credentials

1. Go to the cloned repo directory
2. Copy the config template:

```bash
cp config/config_template.py config/config.py
```

3. Edit `config/config.py` and paste your:
   - `SUPABASE_URL`
   - `SUPABASE_KEY`

Done!

# Launching Our Capstone Website

Step-by-step guide: from purchased domain to a live signup site

**The situation:** Our sponsor bought the domain. We are building the pre-launch site for an app, and people will sign up, so we need a database. The domain is only the address; we still need a place for the site to live.

**Expected cost:** about \$0 while we build and demo, then roughly \$5 to \$25 per month once real users sign up. Confirm with the sponsor before spending anything.

## At a glance

| **\#** | **Step**                                   | **Who does it**                  |
|--------|--------------------------------------------|----------------------------------|
| **1**  | Find the registrar and get DNS access      | Sponsor + team                   |
| **2**  | Set up the code repository                 | Team                             |
| **3**  | Set up the database and signups (Supabase) | Team                             |
| **4**  | Deploy the site to a host                  | Team                             |
| **5**  | Connect the domain (DNS records)           | Sponsor or delegated team member |
| **6**  | Check HTTPS and test signups               | Team                             |
| **7**  | Plan for privacy, costs, and handoff       | Team + sponsor                   |

## Step 1: Find the registrar and get DNS access

Nobody remembers where the domain was bought, so start here. The registrar is the company that holds the domain (GoDaddy, Namecheap, Squarespace, Cloudflare, etc.).

### Find the registrar

- **Option A:** Ask the sponsor to search his email for the domain purchase receipt. It names the registrar.

- **Option B:** Look the domain up at lookup.icann.org. The result lists the registrar.

### Get access

- Ask the sponsor to add one team member as a delegate or admin on the registrar account, OR

- Have the sponsor make the DNS changes himself when we send him the exact records to enter (Step 5).

**Tip:** Do not ask for the sponsor's password. Use the registrar's delegate or share-access feature instead.

## Step 2: Set up the code repository

- Create a GitHub repository for the project. Ideally put it under the sponsor's or the team's GitHub organization, not a personal account.

- Add every teammate and the sponsor (if he wants) as collaborators.

- Add a README that explains what the project is and how to run it locally.

- Never commit passwords or API keys. Keep them in environment variables (a .env file listed in .gitignore).

## Step 3: Set up the database and signups (Supabase)

Supabase gives us a Postgres database plus built-in login and signup, so we do not have to build accounts or store passwords ourselves. Firebase is a similar alternative.

- Create a free Supabase project.

- Create a table for waitlist signups. For a pre-launch site, an email address (plus a timestamp) is often enough.

- Turn on Row Level Security so visitors can add their own signup but cannot read other people's emails.

- Copy the project URL and the public (anon) key into the site's environment variables.

- Test locally: submit a signup and confirm the row appears in the table.

**Heads up:** Free Supabase projects pause after about a week of inactivity. Plan to upgrade (about \$25 per month) before launch so the site does not go to sleep.

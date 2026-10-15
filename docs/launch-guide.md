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

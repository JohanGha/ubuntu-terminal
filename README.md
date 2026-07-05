# Ubuntu Terminal (GitHub Actions + tmate)

An on-demand Ubuntu terminal running inside a GitHub Actions runner, accessed
via a tmate web/SSH session.

## How to use

1. Go to the **Actions** tab.
2. Select **Ubuntu Terminal** and click **Run workflow**.
3. Open the run, expand **Start tmate terminal session**, and use the printed
   web URL (`https://tmate.io/t/...`) or SSH command.

## Notes / limits

- Each job runs for **up to ~6 hours**, then the machine is **destroyed** —
  nothing is persisted.
- This repo is **public**, so the connection string appears in the **public
  logs**. Anyone who reads the logs during the session can connect. Do **not**
  put secrets/credentials into the session.
- Intended for CI debugging. Using GitHub Actions as a general-purpose VM may
  violate GitHub's Acceptable Use Policies.

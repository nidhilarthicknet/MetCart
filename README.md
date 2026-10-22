# MET-CART

**A Metxon Product** — standalone shopping storefront.

## Deploy
GitHub Actions publishes the repository root to GitHub Pages on every push to `main`. In **Settings → Pages**, select **GitHub Actions** as the build and deployment source.

## Account and payments
- Existing Metxon users sign in with their **Metxon username and password**.
- New users should create a Metxon account at https://nidhilarthicknet.github.io/metxon/.
- Forgotten-password recovery asks for a Met-Ail ID and directs the user to confirm ownership through their signed-in Met-Ail inbox / Metxon Care. MetCart does not directly reset a password.
- Checkout uses the existing shared Supabase project and the secure `metxon_purchase_metcart` RPC with a separate MetPay transaction password.
- Do not put Supabase service-role keys or MetPay passwords in frontend files.

## Supabase
Project URL: `https://brahcvovidgjjzpkxsms.supabase.co`

The storefront expects the existing `metcart-catalog-sync` and `metxon-auth-v2` Edge Functions and the secure purchase RPC to be deployed in that shared project.

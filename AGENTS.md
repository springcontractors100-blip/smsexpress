<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Mobile Money orders use authenticated TanStack server functions and Pesapal production checkout; this app does not use Edge Functions.
- Pesapal IPNs are unsigned notifications, never authorization: server-side status reads must confirm both COMPLETED and code 1, the stored reference, exact UGX amount and currency before a service-role-only atomic settlement.
- Payment orders are stored separately from completed transactions; unique tracking IDs and row-locked settlement prevent duplicate credit grants.
- Browser profile writes are limited to editable contact fields; transaction writes and payment settlement are server-only to prevent balance tampering.

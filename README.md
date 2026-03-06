<div align="center">

# Next.js + Stripe Checkout

![Next.js](https://img.shields.io/badge/Next.js_14-000?style=flat-square&logo=next.js&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=flat-square&logo=stripe&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Complete Stripe integration with Next.js 14 App Router — payments, subscriptions, webhooks, and customer portal.**

</div>

---

## Features

- **Checkout Sessions** — one-time payments with Stripe Checkout
- **Subscriptions** — recurring billing with multiple pricing tiers
- **Webhooks** — secure webhook handling with signature verification
- **Customer Portal** — self-service subscription management
- **Server Actions** — Next.js 14 Server Actions for Stripe API calls
- **Prisma + PostgreSQL** — persistent customer/subscription data
- **Type-safe** — full TypeScript coverage with Zod validation

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router) |
| Payments | Stripe API, Stripe.js, React Stripe.js |
| Database | PostgreSQL + Prisma ORM |
| Styling | Tailwind CSS |
| Validation | Zod |

## Setup

\`\`\`bash
git clone https://github.com/mykhayloyuminov/nextjs-stripe-checkout.git
cd nextjs-stripe-checkout
pnpm install
cp .env.example .env.local
pnpm db:push
pnpm dev
\`\`\`

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| /api/checkout | POST | Create Checkout Session |
| /api/webhooks/stripe | POST | Handle Stripe webhooks |
| /api/portal | POST | Create Customer Portal session |
| /api/subscriptions | GET | Get user subscriptions |

## Webhook Events

- checkout.session.completed — activate subscription
- customer.subscription.updated — plan changes
- customer.subscription.deleted — cancellations
- invoice.payment_succeeded — renewal confirmation
- invoice.payment_failed — payment failure handling

## License

MIT — see [LICENSE](LICENSE) for details.

---

<div align="center">
Built by <a href="https://github.com/mykhayloyuminov">Mykhaylo Yuminov</a> · <a href="https://complete-solution.eu">Complete Solution</a>
</div>

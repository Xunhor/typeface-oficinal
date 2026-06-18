# Typeface Platform Architecture

## Phase 1: Current Site

- Keep the existing single-page agency site
- Add pricing, testimonials, FAQ, and stronger CTAs
- Preserve current visual identity and animation language

## Recommended Next.js Structure

```txt
src/
  app/
    layout.tsx
    page.tsx
    globals.css
    sitemap.ts
    robots.ts
    (marketing)/
      pricing/
      portfolio/
      contact/
    (auth)/
      login/
      register/
    dashboard/
      layout.tsx
      page.tsx
      projects/
      tickets/
      billing/
      services/
  components/
    sections/
      hero.tsx
      services.tsx
      pricing.tsx
      portfolio.tsx
      testimonials.tsx
      faq.tsx
      contact-cta.tsx
    ui/
      button.tsx
      card.tsx
      section-heading.tsx
      container.tsx
  lib/
    supabase/
    seo/
    formatting/
  types/
```

## Dashboard Foundation

- `dashboard/projects` for delivery tracking
- `dashboard/tickets` for support and requests
- `dashboard/billing` for payment history and invoices
- `dashboard/services` for maintenance and upsells

## Migration Rule

- Keep marketing and app concerns separate
- Start with reusable section components
- Add Supabase auth only when dashboard features are ready

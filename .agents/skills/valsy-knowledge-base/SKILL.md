---
name: valsy-knowledge-base
description: >-
  Comprehensive architectural and feature-level knowledge base for the Valsy e-commerce platform (.NET 10 Clean Architecture/DDD backend and Next.js 16/React 19 App Router frontend). Use this skill whenever planning, implementing, debugging, or reviewing backend or frontend features, API contracts, domain models, database configurations, or UI flows in Valsy.
---

# Valsy Knowledge Base Skill

This skill provides progressive-disclosure access to the isolated **Valsy Knowledge Base** repository (`A:\Study\Valsy\valsy-knowledge-base`), covering both the **.NET 10 Backend** (`A:\Study\Valsy\Valsy`) and the **Next.js 16 Frontend** (`A:\Study\Valsy\valsy-frontend`).

---

## Workflow: How to Use This Skill

### Step 1: Load the Relevant Base Architecture Guide
Before writing or modifying code, read the base guide for the stack you are working on:
- **Backend Tasks (`.NET 10` / EF Core / MediatR / DDD)**:
  Read [backend/BASE.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/BASE.md) for solution layering (`Valsy.Domain`, `Valsy.Application`, `Valsy.Infrastructure`, `Valsy.Api`), `AggregateRoot`/`Entity`/`AuditableEntity` conventions, `ValsyDbContext` soft-delete & `RowVersion` concurrency rules, `ValidationBehavior`, and `ExceptionHandlingMiddleware`.
- **Frontend Tasks (`Next.js 16` / `React 19` / `Tailwind v4`)**:
  Read [frontend/BASE.md](file:///A:/Study/Valsy/valsy-knowledge-base/frontend/BASE.md) for App Router conventions, dark glassmorphic design tokens (`#0a0a0f`), shared DTOs (`types/index.ts`), the typed API client (`lib/api.ts`), and known frontend-backend contract nuances.

### Step 2: Load Only the Target Feature Documentation (Progressive Disclosure)
Read the specific feature documentation file(s) matching the user's request to understand existing domain invariants, CQRS commands/queries, API endpoints, and UI state flows:

#### Backend Features (`backend/features/`)
- **Products, Variants, Catalog Filtering & Admin Stock**:
  [backend/features/products-and-catalog.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/features/products-and-catalog.md)
- **Customer Profiles & Owned `Address` Value Object**:
  [backend/features/customers.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/features/customers.md)
- **Orders, Line Items, Stock Deduction & Order Status Lifecycle**:
  [backend/features/orders.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/features/orders.md)
- **Discounts & Promo Codes (`Percentage` / `FixedAmount`)**:
  [backend/features/discounts.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/features/discounts.md)
- **Shipping Quotes, Shipments & `IShippingProvider`**:
  [backend/features/shipping.md](file:///A:/Study/Valsy/valsy-knowledge-base/backend/features/shipping.md)

#### Frontend Features (`frontend/features/`)
- **Landing Page, Catalog Search/Filters, Product Detail & `VariantSelector`**:
  [frontend/features/storefront-and-catalog.md](file:///A:/Study/Valsy/valsy-knowledge-base/frontend/features/storefront-and-catalog.md)
- **Client Cart (`CartProvider`), 3-Step Checkout & Order Confirmation**:
  [frontend/features/cart-and-checkout.md](file:///A:/Study/Valsy/valsy-knowledge-base/frontend/features/cart-and-checkout.md)
- **Admin Dashboard KPIs, Low-Stock Alerts, Product Creation & Inline Stock Editor**:
  [frontend/features/admin-dashboard-and-inventory.md](file:///A:/Study/Valsy/valsy-knowledge-base/frontend/features/admin-dashboard-and-inventory.md)

### Step 3: Keep the Knowledge Base Synchronized
Whenever you add a new feature, modify a domain rule, change an API route/payload, or add a new page/component in Valsy:
1. Update the corresponding `backend/features/*.md` or `frontend/features/*.md` (or create a new feature file and index it in `BASE.md` and `README.md`).
2. Commit the documentation update inside the isolated repository (`A:\Study\Valsy\valsy-knowledge-base`).

# TOS Dashboard Concept: Product Discovery and Stop-Decision Case Study (2022)

> **Status - historical concept, not a product:** This repository preserves commissioned design direction and an incomplete Angular shell created in October 2022 for Trade with MAK. It never reached dashboard logic, authentication, API integration, or production use. It does not provide live positions, trading signals, account access, or investment advice.

The concept explored whether the member experience then spread across ThinkOrSwim screen sharing, Discord, and subscription tooling should become a dedicated web dashboard. The work stopped at the shell stage when the business consolidated around WordPress and MemberPress and the custom-build economics no longer justified continued delivery.

## Executive brief

| Area | Scope |
|---|---|
| Problem | Members had to follow live commentary, position context, community messages, and access status across separate tools |
| Concept | A responsive dashboard combining a positions/orders view, Discord activity, membership access, and the Trade with MAK brand |
| My role | Product concept, workflow definition, reference curation, vendor direction, Angular scaffold initiation, and stop decision |
| Discovery period | October 2022 |
| Delivery state | Design assets plus an Angular 14/Material navigation shell |
| Production state | Never integrated, authenticated, deployed, or used for live trading |

## My role

I framed the member workflow problem, selected and redacted real operating references, wrote the product concept, directed the commissioned design work, generated and began configuring the Angular scaffold, evaluated the integration and support burden, and made the decision to stop before partial release.

## Parent-program context and metric provenance

These figures describe Trade with MAK's subscription program. They do not describe this prototype's adoption or any investment performance.

| Metric | Figure | Scope/date | Basis |
|---|---:|---|---|
| Community footprint | Approximately 2,000 | Across channels over the program lifecycle | Founder-reported footprint |
| Paid subscribers | 1,200+ | Cumulative across the program lifetime | Founder-reported cumulative total; not concurrent or active subscribers |
| Monthly recurring revenue | $28,696.05 | Stripe screenshot marked 'Data as of Feb. 3'; source crop does not show the year | Documented point-in-time snapshot |
| Active subscriptions | 321 | Same Stripe snapshot | Documented point-in-time count |
| Gross and net sales volume | $98,999.95 gross / $89,093.60 net | One LaunchPass/Stripe account, Jan. 1, 2021-July 7, 2022 | Documented account-specific all-time snapshot; not profit |
| Customers and payments | 862 customers / 1,610 successful payments | Same account and period | Documented account-specific counts; payments are not unique subscribers |

## Product hypothesis

Members followed live sessions through Discord messages and a ThinkOrSwim screen share. The concept asked whether a single member-facing interface could reduce that fragmentation through:

- a positions and orders panel modeled on the information hierarchy of the ThinkOrSwim Activity and Positions monitor;
- a Discord panel surfacing the community trading-floor feed and alerts alongside position context;
- Stripe or membership integration so access reflected subscription status and administrators could see basic operating metrics; and
- a branded dark-terminal interface using the Trade with MAK mission statement and tagline.

These were product requirements, not completed capabilities.

## Discovery and delivery approach

### 1. Workflow references

The design engagement used annotated screenshots of the actual workflow: trading-account views, the member Discord environment, and the Stripe dashboard. Those references contained account and member information and are deliberately not public.

### 2. Commissioned design direction

The October 2022 third-party design engagement produced the shareable brand assets in `design/`:

- `mission-banner.jpg`;
- `tagline-banner.jpg`; and
- `hero-background-concept.png`.

Third-party work should be identified and included only where reuse rights are confirmed.

### 3. Angular shell

`prototype/` contains the implementation state at the stop decision:

- Angular 14.2 with TypeScript 4.7;
- Angular Material and CDK 14.2;
- routing and environment scaffolding;
- a responsive Material side-navigation component generated through the sidenav schematic;
- a custom Material theme; and
- approximately 360 lines of source in the retained scaffold.

There is no positions engine, market-data connection, Discord integration, Stripe integration, authentication, authorization, persistent data model, audit logging, or production deployment.

## Why the project stopped

By late 2022, Trade with MAK was consolidating its subscription and content stack on WordPress and MemberPress. Continuing a custom real-time dashboard would have added substantial integration, security, privacy, reliability, and support obligations. I stopped the experiment at the scaffold stage rather than allowing sunk cost to drive an unsupported product into partial release.

That decision is part of the portfolio evidence: product leadership includes defining when not to continue.

## Running the retained shell

The scaffold requires the Angular 14-era toolchain pinned in `prototype/package.json` and a compatible Node 16 environment.

```bash
cd prototype
npm install
npx ng serve
```

Open `http://localhost:4200/`. The expected output is a Material toolbar and empty responsive side-navigation shell. Any deprecation, dependency, or security warnings should be evaluated before running an older framework locally.

## Acceptance status

| Capability | Discovery intent | Retained state |
|---|---|---|
| Responsive application shell | Establish basic navigation and layout | Partial scaffold present |
| Positions and orders | Present member-readable position context | Not implemented |
| Discord activity | Co-locate community feed and alerts | Not implemented |
| Subscription access | Reflect membership status | Not implemented |
| Authentication and authorization | Protect member and account information | Not implemented |
| Admin metrics | Present aggregate subscription operations | Not implemented |
| Production readiness | Security, monitoring, support, and deployment | Out of scope; never attempted |

## What I learned

- Real workflow references make product discovery more concrete, but privacy-safe public evidence must be separated from internal references.
- Commissioning low-cost design direction before full implementation can test the information architecture without committing to a build.
- Integration scope must include security, support, reliability, and data governance, not only visible interface work.
- Stopping a project early can be the correct portfolio decision when the operating model changes.

## Limitations

- This is an incomplete historical scaffold built against an older Angular toolchain.
- No functional dashboard claim should be inferred from the design assets or navigation shell.
- No live account, member, payment, Discord, or market data is included.
- Program-level community and Stripe metrics do not represent prototype adoption.

## Authorship and provenance

I defined the product concept, selected and redacted workflow references, directed the design engagement, generated and began configuring the Angular shell, and made the stop decision. The design assets were commissioned through a third-party marketplace. This public documentation was assembled in 2026 with AI assistance under my direction.

Author: Sama Mushtaq

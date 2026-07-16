# TOS Dashboard Concept

A product concept from October 2022 for a ThinkOrSwim-style trading dashboard for my community, Trade with MAK: commissioned UI design direction (via Fiverr) plus an Angular scaffold I started myself. The build stopped at the shell stage when the business pivoted, and this repo presents it exactly as it was - a concept, not a product. That honesty is the point.

## The idea

Members followed my trades through Discord messages and a ThinkOrSwim screen share. The concept was a web dashboard that would make that experience first-class:

- **Live positions and orders panel** styled after the ThinkOrSwim Activity and Positions monitor (working orders, filled orders, position statement) so members could read my book at a glance instead of scrubbing a stream.
- **Discord integration** to surface the community trading-floor feed and alerts next to the positions panel.
- **Stripe/membership integration** so access mirrored subscription status, with basic growth metrics for the admin side.
- **Brand layer** using the tradewithMAK identity: dark trading-terminal aesthetic, mission statement hero, "Trade with the best" tagline.

## What was actually produced

1. **Design direction (commissioned, Fiverr, October 2022)** - `design/` contains the shareable brand assets from that engagement: the mission-statement banner, the script tagline banner, and a hero background concept. The working references for the dashboard, Discord, and Stripe panels were annotated screenshots of my real trading account, the live member server, and the live Stripe dashboard; those contain account and member data, so they are described here but not published.
2. **Angular prototype (mine)** - `prototype/` is the scaffold I generated and began wiring up: Angular 14 with Angular Material, a responsive side-nav shell (`nav` component via the Material sidenav schematic), routing module, and a custom Material theme. It is roughly 360 lines of source. There is no dashboard logic, no API integration, and no auth - it is the shell, and that is where it stopped.

## Why it stopped

By late 2022 the community's stack was consolidating on WordPress/MemberPress, and the effort a custom real-time dashboard demanded was not justified by the size of the business (peak 245 subscribers). I shut the experiment down at the scaffold stage rather than half-ship it.

## Running the prototype

```
cd prototype
npm install
npx ng serve
```

Requires Node 16+ and the Angular 14-era toolchain pinned in `package.json`. You will see a Material toolbar and an empty side-nav shell - that is the honest extent of it.

## What I would keep from this

- Designing from real screenshots of the actual workflow (trader screen, community feed, billing) kept the concept grounded in what members actually did.
- Buying design direction cheaply before writing code was the right order of operations.
- Killing the build early, in writing, with reasons, is a product decision too.

# data center co-location: how DMIT's carrier-neutral racks in LAX, HKG & TYO actually work, and what to ask before you sign

If you're reading up on data center co-location, you've probably hit the same wall as everyone else: provider pages full of "contact sales" buttons and almost no real numbers. That's not evasiveness — it's how colocation actually works. Space, power draw, bandwidth commitment, contract term, and city all change the math, so a flat rack rate would be misleading. What you can do is understand the variables, know what a provider's facilities actually give you, and walk into the quote conversation with the right questions. This article does that walk-through using DMIT's colocation offering as the concrete example, since it sits in three locations (Los Angeles, Hong Kong, Tokyo) that come up a lot for APAC-facing deployments.

## What data center co-location actually is

Co-location (usually written "colocation") means you own the hardware and rent the space, power, cooling, security, and network connectivity inside someone else's data center. You ship your servers; the facility racks them, powers them, cools them, and keeps them physically secure. You keep full control of the hardware and the OS layer. The provider controls the building, the power feed, the cooling, the cross-connects, and (optionally) IP transit.

This is different from cloud hosting, where the provider owns the servers and you rent compute by the hour or month. With colocation you make an up-front capital investment in hardware, but the ongoing monthly cost per unit of compute is usually lower once the hardware is amortized — especially if you need specialized gear (custom GPUs, storage arrays, network appliances) that no cloud provider stocks. The trade-off is that you're responsible for hardware failures, spares, and lifecycle, and you need someone to act as your hands in the facility if you're not local.

The other thing colocation gives you that cloud can't is **carrier-neutral interconnection**. In a carrier-neutral facility you can blend the provider's own IP transit with your own contracted carriers via cross-connects, peer at internet exchanges, and reach cloud on-ramps — all inside the same building. That's the actual reason most serious deployments end up in colocation rather than a single-cloud cage.

## Why people end up looking at DMIT for co-location

DMIT's colocation footprint is built around the Asia-Pacific corridor: **Los Angeles, Hong Kong, and Tokyo**, all carrier-neutral. If your users are in mainland China or the wider APAC region, that geography matters. DMIT operates inside CoreSite and Digital Realty in LA, Equinix HK2 in Hong Kong, and Equinix TY8 in Tokyo — all dense interconnection campuses with multiple carriers, IXes, and cloud on-ramps in the same building.

The piece that actually differentiates DMIT from a generic carrier-neutral cabinet is the **Premium Network**. It blends Tier 1 transit with China Telecom CN2 GIA (AS23764) and, in Hong Kong, CMI (AS58453). On the Premium Network, DMIT publishes ~15ms average latency from Hong Kong to Shenzhen with under 0.1% packet loss, and ~28ms from Tokyo to Shanghai. Standard Tier 1 transit into mainland China typically runs much higher latency and loss during peak hours, because international gateways congest. If China-facing performance is part of your requirement, that routing is the actual selling point — not the rack space itself.

## The three deployment tiers DMIT offers

DMIT structures colocation around three deployment sizes. Final specs and pricing vary by location and capacity, and everything is set in your signed order — but the structural choice is between these three:

- **Rack Units (1U–4U)** — shared, secured cabinet space billed per rack unit. Entry point for a single server, edge node, or appliance. You pay for what you occupy and can grow from there.
- **Half Cabinet** — a lockable half cabinet with dedicated power and bandwidth. The sweet spot for mid-size clusters, storage builds, or anyone who needs isolation from neighbors without paying for a full rack they'll only half-fill.
- **Full Cabinet** — a full cabinet with committed power and bandwidth, designed for dense, high-power deployments. Private cages are available on request if you need physical separation beyond a single cabinet.

Every tier sits on the same facility stack, so the difference is footprint and committed resources, not capability. You don't lose SLA or remote hands by starting at 1U.

## Full colocation tier comparison

The table below maps the three tiers DMIT publishes on its colocation page. Pricing is custom-quoted per deal because power density, bandwidth commitment, and contract term all change the number — that's standard for colocation, not specific to DMIT.

| Tier | Footprint | Power model | Bandwidth model | Best for | Get a quote |
| --- | --- | --- | --- | --- | --- |
| **Rack Units (1U–4U)** | Shared secured cabinet space, billed per U | Flexible (metered or fixed) | Flexible — 1G/10G/higher; 95th percentile, committed, or flat | Single servers, edge nodes, small deployments, pay-as-you-grow | [Request a custom colocation quote](https://bit.ly/DmiT) |
| **Half Cabinet** | Lockable half cabinet, dedicated resources | Dedicated power | Dedicated bandwidth | Mid-size clusters, storage, room to scale within the cabinet | [Get a half-cabinet quote](https://bit.ly/DmiT) |
| **Full Cabinet** | Full 42U cabinet; private cage on request | Committed power | Committed bandwidth | High-density, high-power racks, private deployments | [Get a full-cabinet quote](https://bit.ly/DmiT) |

If you already know which tier fits, the fastest path is to put together your hardware list, peak power draw, desired port speed and monthly transfer, and preferred city, then 👉 [open a colocation ticket with DMIT](https://bit.ly/DmiT) — they'll come back with a real number rather than another "contact sales" page.

## What sits underneath the rack

A colocation contract is only as good as the infrastructure beneath it. Here's what DMIT's three facilities actually provide, based on what's published on the location pages.

### Power and cooling

All three facilities run N+1 UPS with diesel generator backup, diverse utility feeds, and A/B power. Cooling is precision, hot/cold aisle, Tier III/IV class. LA is described as Tier IV-built, HK2 is Tier IV, TY8 is Tier IV. You can pick **metered or fixed power** — metered means you pay for what you pull (better for variable loads), fixed means a predictable bill (better for steady high-density racks). If you're planning a high-density deployment, confirm the per-cabinet power cap for your chosen city before shipping hardware, because density limits vary by facility.

### Network and interconnection

This is the part that actually justifies carrier-neutral colocation. DMIT's network options:

- **1G / 10G / higher port speeds**, billed by 95th percentile, committed, or flat
- **Cross-connects** to your own contracted carriers and to internet exchanges
- **Premium Network** combining Tier 1 transit with CN2 GIA and (in HKG) CMI for China-APAC-optimized routing
- **Tier 1 Network** for clean global routing without China-specific enhancements
- **Eyeball Network** (LAX/HKG) for a budget-aware balance between Tier 1 and China routing

Aggregate Tier 1 capacity is published as **3.8Tbps in LA, 2.4Tbps in HKG, and 1.4Tbps in TYO**, with 50+ carriers available inside Equinix TY8. Carrier density in HK2 and the LA campuses is similarly high. The point: you're not buying a single pipe, you're buying access to a dense interconnection ecosystem with the option to bring your own carriers.

### Physical security and compliance

Badge access, biometric controls, 24/7 CCTV, and on-site guards at all three locations. DMIT lists **ISO 27001, SOC 2, and PCI DSS** compliance on the LA page, with HKG citing ISO 27001 and PCI DSS. If you have specific compliance requirements, confirm which certifications apply to the specific facility you're deploying into — certifications are per-building, not per-provider.

### Facility SLA

DMIT's colocation product carries a **99.99% Facility Uptime SLA**. That's a facility-level guarantee — it covers power, cooling, and facility network, not your individual hardware. Read the signed contract for what's actually guaranteed and what the compensation structure is, since SLA terms are governed by your order, not the marketing page.

## Remote hands and rack-and-stack

This is the part that quietly saves you a plane ticket. DMIT's on-site engineers handle the install phase:

- Equipment receiving and inventory check
- Racking, structured cabling, and labeling
- Power-on, BIOS/IPMI setup, and testing
- Photos and documentation on completion

Once you're live, the 24/7 remote hands team covers reboots, part swaps, reseating, media handling, visual diagnostics, scheduled inspections, and emergency response. All of it is **ticket-driven and audited** — good for accountability, but it means you should expect to open a ticket for any on-site action rather than calling someone directly. For anyone managing gear from another continent, which is most of DMIT's audience given the LAX/HKG/TYO spread, this is the difference between a colocation contract that works and one that doesn't.

## How colocation pricing actually works

Since DMIT doesn't publish flat rates, it helps to know what's driving the quote you'll get back. Colocation pricing is built from a few variables, and understanding them lets you ask for a real quote instead of a generic one.

**Space** is priced per rack unit up through half and full cabinets. Industry-wide, small per-U deployments run roughly $79–$150/month, quarter racks around $300–$500, half racks $500–$800, and full 42U racks higher — but those are market averages, not DMIT's figures. DMIT's LAX/HKG/TYO pricing will land where supply and demand put it, which is exactly why they quote per deal.

**Power** is the real cost driver in 2026. Market-wide, per-kW rates have climbed into the $130–$150/kW/month range in tight markets, with averages around $98–$196/kW depending on region and deal size. High-density racks cost more per kW than low-density ones. DMIT's metered vs. fixed choice lets you match the billing model to your load profile.

**Bandwidth** is billed by port speed and model. A 1Gbps dedicated internet connection typically runs $500–$1,000/month on the open market depending on carrier, but DMIT's bundled transit (including Premium Network with CN2 GIA for China-APAC routing) is a different value proposition than raw carrier pricing. Cross-connects to your own carriers or IXes are additional.

**Support and remote hands** are included in DMIT's colocation product. That's not universal — many providers charge per-touch after a small monthly allowance, so include-or-extra is worth confirming.

**Contract term** moves the per-month number. Longer commitments almost always lower the rate.

The short version: when you reach out for a colocation quote, come with your hardware list, peak power draw, desired port speed and monthly transfer, and preferred city. That's what turns a "contact sales" page into a real number in your inbox.

## Who DMIT co-location actually fits

DMIT colocation makes the most sense for a fairly specific buyer. It's not the right answer for everyone.

- **APAC-focused operators** who need presence in LAX, HKG, or TYO with routing optimized for China and the wider Asia-Pacific region. The Premium Network with CN2 GIA is a genuine differentiator if your users are in mainland China — it's the kind of routing you can't just buy from any carrier-neutral facility.
- **Own-hardware operators** running purpose-built or specialized servers that no cloud provider offers — custom storage, GPUs, network appliances, telecom gear.
- **Hybrid and DR builders** pairing colocation with DMIT's cloud and bare metal for hybrid architectures or off-site disaster recovery.
- **Network edge operators** who want routers, caches, and edge gear physically near IXes and carriers to shave latency.

If you're a small team that just needs a single app online and has no APAC routing requirement, a VPS or cloud instance will be cheaper and simpler. Colocation earns its keep when you need hardware control, specific geography, carrier flexibility, or density that cloud pricing can't justify.

## What to ask before you sign

A few items from DMIT's published terms and the colocation page that are worth flagging before you commit:

- **Refund policy** leans strict. DMIT's published refund rules cover virtual services — full refund within 3 days and under 30GB transfer, partial within 30 days. Colocation, being a contracted service with custom terms, is governed by your signed order. Read the cancellation clause before committing.
- **Remote hands scope** is ticket-driven and audited. Good for accountability, but expect to open a ticket for any on-site action rather than calling someone directly.
- **Power density limits** vary by facility and cabinet. If you're planning a high-density rack, confirm the per-cabinet power cap for your chosen city before you ship hardware.
- **Bandwidth overage** on metered plans can be billed at adjusted rates, and DMIT reserves the right to adjust pricing. Locked-in rates apply to your specific term, not indefinitely.
- **OFAC restrictions**: DMIT does not accept orders from Cuba, Iran, Lebanon, Libya, Myanmar, North Korea, Somalia, Sudan, or Syria. Confirm eligibility before going deep on a quote.

## A note on coupons and promotions

DMIT runs coupon codes periodically, and a few tend to circulate on deal sites. The ones worth knowing about generally target VPS and cloud products — recurring percentage discounts on annual billing for Hong Kong and Tokyo network tiers, that kind of thing. Colocation deals, because they're custom-quoted, typically aren't covered by public coupon codes. The discount shows up in the negotiated rate when you commit to a term, not as a code you paste at checkout.

DMIT's terms note that discount codes are generally for new customers and that misusing codes tied to other accounts can get your service suspended, so don't try to stack a code you found on a coupon site if it wasn't issued to you. When in doubt, ask the colocation team what's currently available when you request your quote — that's also the right moment to ask about term-length discounts.

## Choosing between LAX, HKG, and TYO

The three locations aren't interchangeable. Each one has a distinct profile, and the right choice depends on where your users are and what routing you need.

**Los Angeles** is the Pacific Rim interconnection point — it bridges submarine cable systems from APAC with the core internet infrastructure of North America. DMIT's LA presence spans CoreSite and Digital Realty campuses, with 3.8Tbps aggregate Tier 1 capacity and dedicated high-capacity peering with China Telecom (AS4809), China Unicom (AS9929), and China Mobile International (AS58807). Premium Network routes leverage CN2 GIA. Good for cross-region deployments bridging APAC and the Americas, and for serving China-facing traffic from a US-based deployment.

**Hong Kong** is the gateway to mainland China and APAC. DMIT operates inside Equinix HK2 in Kwai Chung, with 2.4Tbps Tier 1 bandwidth and dual China-optimized connectivity via CN2 GIA (AS23764) and CMI (AS58453). The published ~15ms latency to Shenzhen with under 0.1% packet loss is the standout number. This is the node to look at first if mainland China user experience is your primary concern.

**Tokyo** sits in Equinix TY8 in Shinagawa, with 1.4Tbps Tier 1 transit and 50+ network carriers. Tokyo's geographic proximity to mainland China gives ~28ms latency to Shanghai via CN2 GIA on the Premium Network, the lowest among DMIT's APAC nodes for China-facing workloads. Tokyo also has direct interconnects with major Japanese domestic ISPs and low-latency routing to Korea, Taiwan, and Southeast Asia — a strong pick for pan-East-Asia deployments.

If you're unsure which location fits, the practical move is to test latency from your actual user base to each region before committing. DMIT's sales team can also advise based on your traffic profile.

## The bottom line

DMIT co-location is best understood as a **carrier-neutral, APAC-optimized colocate-your-own-gear service** across Los Angeles, Hong Kong, and Tokyo, backed by N+1 power, Tier III/IV facilities, 24/7 remote hands, and a 99.99% facility uptime SLA. Pricing is custom-quoted because that's how colocation actually works — space, power, bandwidth, and term all change the number. The value isn't in a published rack rate; it's in the combination of three strategically placed facilities, real carrier choice with cross-connects, China-APAC-optimized transit via the Premium Network, and an on-site team that acts as your hands in three cities you probably aren't flying to.

If that matches what you're trying to build, put together your hardware list, power and bandwidth needs, and preferred location, then 👉 [request a tailored colocation quote from DMIT](https://bit.ly/DmiT). The quote comes back as a real number — not another "contact sales" page — and that's the point at which you can actually compare it against the alternatives.

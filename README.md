# cheapest vps: what $3.98/month really buys, the renewal trap to avoid, and where Sharktech's Smart VPS fits

Search "cheapest vps" and you'll get two very different kinds of results. One is the ultra-budget end — LowEndBox-style deals like a 1GB VPS for $12/year — fine for a hobby DNS box, risky for anything you actually care about. The other is the mainstream budget tier: DigitalOcean droplets from $4/month, VPSDime from $5/month, roundups putting InterServer and Kamatera in the $3–4 range. Sharktech's Smart VPS sits right in that bracket with its entry plan at $3.98/month on annual billing, which is why it keeps showing up in this conversation.

But "cheapest" is doing a lot of work in that search query. The monthly sticker price is maybe a third of the story. The rest is what happens at renewal, what's included, and what it costs you when something goes wrong. Let's unpack that, then look at where Sharktech actually lands.

## The renewal-price trap, and other ways a cheap VPS gets expensive

The classic move in budget hosting: advertise $2.99/month, then quietly double or triple it at renewal. You find out a year later when the invoice hits. Some providers are upfront about it; many bury it under an asterisk. Sharktech's approach here is different in a way that matters for total cost: the prices are flat. The $7.95/month entry rate (XS tier) is the rate. Annual billing takes 50% off, and that discount is structural, not promotional — it doesn't vanish after the first term.

A second cost that doesn't show up on the price tag: DDoS protection. A lot of budget providers either don't include it or treat it as "we'll null-route your IP if you get attacked," which is a polite way of saying they'll take you offline to protect their network. If you run a game server, a public API, or anything that attracts adversarial traffic, that's not a hypothetical problem — it's the difference between a bad afternoon and a multi-day outage. OVH is one of the few big names that includes protection at no extra cost; Sharktech is another, with 60Gbps of mitigation on every plan, entry tier included.

Third: overage bills. Metered bandwidth looks cheap until a traffic spike turns your $4/month into $40. Sharktech's Smart VPS is a flat monthly price with the billing cycle discount baked in — the official page puts it plainly: no shock overage bills.

## What a cheap VPS should include before it's a good deal

Before comparing prices, it helps to have a checklist. Based on what consistently separates a good budget VPS from a regrettable one:

- **Flat renewal pricing** — the price you see is the price you keep paying
- **Real storage** — NVMe or at least SSD, not a spinning disk dressed up in marketing
- **Dedicated, non-oversold resources** — your 2 cores should behave like 2 cores
- **DDoS protection included**, not a $15/month add-on
- **A data center near your users** — latency is a feature you pay for either way
- **A clear refund or dispute policy** — cheap hosts with no recourse are a gamble

Sharktech checks most of these boxes, with one honest exception on the refund side we'll get to. First, the numbers.

## Sharktech Smart VPS pricing, explained

Sharktech has been around since 2003, runs its own network (AS46844, direct peering at major exchange points), and operates five data centers: Los Angeles, Las Vegas, Denver, Chicago, and Amsterdam. The Smart VPS line runs on Proxmox clusters with Xeon Gold CPUs, enterprise NVMe storage, and a claimed 99.999% uptime on a triple-redundant platform — if a hardware node fails, your VM fails over instead of going down.

The pricing model is simpler than most: one rate per plan, four billing cycles, and the longer you commit, the less you pay.

- **Monthly:** full price
- **Quarterly:** 25% off
- **Semi-annually:** 35% off
- **Annually:** 50% off — no promo code, applied automatically at checkout

So the entry XS tier (2 Xeon Gold cores, 4 GB DDR4, 40 GB NVMe, 4 TB transfer) lists at $7.95/month, and drops to **$3.98/month when billed annually**. Every plan includes 60Gbps DDoS protection, a 1Gbps port, one IPv4 address, and your choice of Linux distributions or Windows Server (ISO install, bring your own license or buy one from them).

One structural detail that's easy to miss: Smart VPS isn't "one plan, one server." You're buying a resource pool. You can carve it into a single VM or split it into multiple smaller ones, spread across different data centers — one production VM in Los Angeles and a couple of test VMs in Chicago and Amsterdam, for example. You can upgrade or downgrade the pool without redeploying. For developers juggling environments, that's more flexibility than the standard one-VPS-per-plan model most providers still use.

👉 [See the full Smart VPS lineup and lock in the 50% annual discount](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611)

## Full Smart VPS plan comparison

Here's the current tier ladder. Specs for XS through XL are from Sharktech's published lineup; monthly prices for S–XL follow from the official 50% annual-billing discount (annual rate × 2). Every plan includes 40 GB of baseline NVMe storage, 4 TB of transfer, and 1 IPv4 — all scalable at order time, with NVMe expandable to 2,000 GB and transfer up to 300 TB.

| Plan | Xeon Gold Cores | RAM | NVMe (base, scalable to 2 TB) | Monthly | Annual (50% off) | Deploy |
| --- | --- | --- | --- | --- | --- | --- |
| XS | 2 | 4 GB DDR4 | 40 GB | $7.95/mo | **$3.98/mo** | [ Deploy XS](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| S | 4 | 8 GB DDR4 | 40 GB | $13.96/mo | **$6.98/mo** | [ Deploy S](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| M | 8 | 16 GB DDR4 | 40 GB | $25.96/mo | **$12.98/mo** | [ Deploy M](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| L | 16 | 32 GB DDR4 | 40 GB | $49.98/mo | **$24.99/mo** | [ Deploy L](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| XL | 32 | 64 GB DDR4 | 40 GB | $97.96/mo | **$48.98/mo** | [ Deploy XL](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| 2XL | Scales up | Scales up | Scales up | Configured on order form | Configured on order form | [ Configure 2XL](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |
| 3XL | Up to 128 | Up to 256 GB | Up to 2,000 GB | Configured on order form | Configured on order form | [ Configure 3XL](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611) |

The 2XL and 3XL tiers are configured through sliders on the order form — the platform scales to 128 vCPU, 256 GB RAM, 2 TB NVMe, and 300 TB of transfer, with the price updating live as you adjust. If you need that much compute, you probably already know your numbers; the form shows the total before you commit.

## What $3.98/month actually buys you

This is where the "cheapest vps" question gets interesting, because the XS tier's spec sheet reads like a much pricier plan. HostAdvice ran an independent benchmark suite on the platform and published the results:

- **6,000+ random IOPS** on 4K reads and writes — most budget VPS plans land between 1,000 and 3,000, and this directly affects how fast database-driven sites feel
- **~19 GB/sec memory throughput**, closer to bare-metal than typical virtualized hosting
- **5.33 Gbps download** measured during stress testing, with no throttling under simultaneous CPU, memory, and disk load
- **Sub-millisecond latency** to Google DNS (0.547ms) and Cloudflare (0.835ms) — a sign of genuine direct peering, not rented transit
- CPU scaling of **7.65x** from single-thread to multi-thread, which suggests the host isn't quietly cramming VMs onto oversubscribed nodes

Those numbers hold up elsewhere too. VPSBenchmarks has an entry for the Tiny/XS tier running on a Xeon Gold 6262V at 1.9GHz, matching the hardware Sharktech advertises. When the marketing page and third-party measurements agree, that's rarer in this industry than it should be.

And then there's the DDoS protection. Sixty gigabits on the cheapest plan, not tier-gated, not an add-on. One of Sharktech's game-hosting customers (Dingdian Network) publicly reports their servers regularly absorb multi-gigabit attacks without going down. If you're shopping for a game server box — Minecraft, CS:GO, ARK — that's the difference between a provider and a liability.

None of this means a $3.98 VPS is the right tool for everything. But for the specific job of "cheap server that behaves like a real server," the evidence is solid. 👉 [Start with the XS plan at $3.98/mo on annual billing](https://portal.sharktech.net/cart.php?a=add&pid=794&billingcycle=annually&aff=1611)

## The trade-offs nobody puts on the landing page

Every budget option has them, and pretending otherwise would make this article useless. Here's what to know before checkout:

> **No refunds.** Sharktech operates a strict no-refund policy — all payments are non-refundable, including setup and recurring charges, and there's no free trial. Billing errors can be disputed within 30 days of the invoice date (resolved disputes get a credit, not cash back). If you like trying before buying, this isn't that kind of provider.

A few more practical notes:

- **It's unmanaged.** You get full root access and are expected to know your way around a command line, package updates, and firewall configuration. If you want someone else patching WordPress for you, Sharktech's separate Cloud Applications Platform is the better fit.
- **Windows costs extra.** Linux distros (Ubuntu, Debian, AlmaLinux, CentOS, and others) are included; Windows Server requires an ISO install with your own license or one purchased through them.
- **cPanel is a paid option** if you want a control panel on top of the raw VPS.
- **Port 25 is closed** on these VPS per current listings — relevant if you were planning to run a mail server. You'd need a relay service.
- **No residential IPs.** Sharktech explicitly doesn't offer them, which matters only for a few niche use cases (some streaming sites block datacenter IPs).

The reviews picture is consistent with all this. HostAdvice's expert review scored the service 9.3/10 overall, praising performance and pricing while flagging the no-refund policy and technical learning curve. Trustpilot sits around 3.5/5 across a small sample of 13 reviews — modest volume, with the substantive reviews highlighting fast, technically competent support and flat pricing. Long-term customers are a recurring theme, which in hosting is usually a better signal than a thousand five-star blurbs.

## Who this is for (and who should skip it)

**Smart VPS is a good fit if you:**

- Run game servers or real-time services that attract DDoS attention and need protection that actually works
- Host websites or apps (WordPress, Node.js, Django, whatever) and want predictable flat pricing with no renewal surprises
- Are a developer who wants a resource pool to split across staging, testing, and production VMs
- Want to deploy in the US or Amsterdam with low latency and don't need managed hand-holding

**Skip it if you:**

- Want the absolute cheapest possible box for a throwaway project — the $12/year LowEndBox tier of the market exists, and for a hobby DNS resolver it's genuinely fine
- Need fully managed hosting with a website builder and guided setup
- Require a money-back guarantee before trying a new provider

The unmanaged nature is the real filter here. You don't need to be a sysadmin, but if the phrase "configure your own firewall rules" sounds like a chore rather than a feature, the entry tier will feel like more work than you signed up for.

## Cheapest VPS: quick FAQ

**Is the $3.98/month price real?** Yes, with one condition: it's the annual billing rate on the XS tier. Pay monthly and it's $7.95. The discount is automatic and doesn't expire — it's how their billing cycles are structured, not a promo.

**Can I run a game server on the cheapest plan?** The XS tier (2 cores, 4 GB RAM) handles small Minecraft or similar servers fine. Heavier games with more players will want the S or M tier. Every tier includes the same 60Gbps DDoS protection, which for game servers is arguably the most valuable included feature.

**Can I upgrade later without migrating?** Yes — resources are upgraded through the customer portal, and because you're managing a pool rather than a fixed VM, you can scale without redeploying.

**Which locations can I pick?** Denver, Chicago, Los Angeles, Las Vegas, and Amsterdam. You choose during VM creation, and you can spread VMs from one pool across multiple locations.

**Is this the cheapest VPS on the market, period?** No. If the only criterion is the lowest possible monthly number, there are cheaper options out there — at the cost of protection, hardware quality, or renewal-price games. The pitch here is cheapest *per unit of what you actually get*: NVMe storage, non-oversold Xeon Gold cores, working DDoS mitigation, and flat pricing. On that measure, $3.98/month is hard to beat.

## The short version

Hunting the cheapest VPS is really a question about what happens after the first invoice. Intro pricing that doubles, protection sold separately, metered bandwidth surprises — those are the ways a cheap server gets expensive. Sharktech's Smart VPS avoids all three: flat rates, 60Gbps DDoS protection on every tier, and no overage bills, with the annual discount bringing the entry plan to $3.98/month on hardware that independent benchmarks confirm is the real thing. The trade-off is a no-refund policy and an unmanaged environment that assumes you know what SSH is. For developers, sysadmins, and game-server operators, that's a reasonable deal. 👉 [Check current Smart VPS pricing and deploy a plan](https://bit.ly/SharKTech)

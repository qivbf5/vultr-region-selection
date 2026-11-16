# Vultr Locations: 33 Regions, a 9-City US Footprint, and How to Pick the Right One (Plus What Changing Regions Really Involves)

Vultr's official data center page currently lists **33 cloud regions**: 11 in North America (nine in the United States, plus Toronto and Mexico City), two in South America, nine in Europe, eight in Asia, two in Australia and one in Africa. Milan is the newest, opened on 19 May 2026 as the 33rd region and the ninth in Europe.

If you're here to decide where to put a server, the short answer is the region closest to the people who will hit it. Below is the full list, how to test latency yourself before committing, and what it actually takes to move a server from one region to another later.

> **Quick pick:** Deploy in the region nearest your visitors, not nearest you. A US-facing site belongs in one of the nine US regions; an EU-facing one in Amsterdam, Frankfurt, London, Madrid, Manchester, Milan, Paris, Stockholm or Warsaw, which also keeps data inside the EU. Entry Cloud Compute is listed by third-party pricing trackers at $2.48/month ($0.0034/hour), billed hourly with no contract. 👉 [See all 33 Vultr regions and start a deployment](https://www.vultr.com/features/datacenter-regions?ref=9738262-9J)

## Every Vultr region, by continent

| Region | Country | Continent |
| --- | --- | --- |
| Atlanta | United States | North America |
| Honolulu | United States | North America |
| Chicago | United States | North America |
| Dallas | United States | North America |
| Los Angeles | United States | North America |
| Miami | United States | North America |
| New York Area | United States | North America |
| San Francisco Bay Area | United States | North America |
| Seattle | United States | North America |
| Toronto | Canada | North America |
| Mexico City | Mexico | North America |
| São Paulo | Brazil | South America |
| Santiago | Chile | South America |
| Amsterdam | Netherlands | Europe |
| London | United Kingdom | Europe |
| Frankfurt | Germany | Europe |
| Paris | France | Europe |
| Madrid | Spain | Europe |
| Stockholm | Sweden | Europe |
| Warsaw | Poland | Europe |
| Manchester | United Kingdom | Europe |
| Milan | Italy | Europe |
| Tokyo | Japan | Asia |
| Osaka | Japan | Asia |
| Seoul | South Korea | Asia |
| Singapore | Singapore | Asia |
| Mumbai | India | Asia |
| Delhi NCR | India | Asia |
| Bangalore | India | Asia |
| Tel Aviv-Yafo | Israel | Asia |
| Sydney | Australia | Australia |
| Melbourne | Australia | Australia |
| Johannesburg | South Africa | Africa |

The distribution tells you where Vultr expects demand. Nine US regions is the largest single-country cluster, which matches the US being its biggest market. Three Indian regions (Mumbai, Delhi NCR, Bangalore) is unusual for a provider this size and makes the country genuinely serviceable for local latency rather than "Asia via Singapore." Nine European regions covers the data-residency requirement that pushes a lot of EU companies away from US-only providers.

Vultr states its network reaches 90% of the world's population within 2–40ms. That's the company's own figure, not an independent measurement, and your actual round-trip time depends on the visitor's ISP and peering, which is exactly why the next section exists.

## What you're putting in that region, and what it costs

Region choice doesn't get you out of picking a plan. Vultr's current lineup runs from small Cloud Compute instances to bare metal and GPU.

A note on the numbers: Vultr's own price list is the only authoritative source, and the figures below come from third-party pricing trackers that mirror Vultr's plan catalogue as of late 2026. They're useful for budgeting, not a quote. Confirm the current figure on the deploy screen before you commit, because configurations and prices change.

| Product line | What it's for | Reported entry price | Billing | Start |
| --- | --- | --- | --- | --- |
| Cloud Compute (Regular, High Performance, High Frequency) | Web servers, APIs, small databases, dev/test | $2.48/mo ($0.0034/hr) for the smallest plan | Hourly, monthly equivalent shown | [Deploy Cloud Compute](https://www.vultr.com/register/?ref=9738262-9J) |
| Optimized Cloud Compute | General purpose, compute-, memory- and storage-tuned instances | $28/mo | Hourly, monthly equivalent shown | [Deploy Optimized Cloud Compute](https://www.vultr.com/register/?ref=9738262-9J) |
| VX1 Cloud Compute | AI inference, SaaS platforms, ERP, analytics, in-memory caches | $2,102.40/mo for the largest listed configuration | Hourly, monthly equivalent shown | [Deploy VX1](https://www.vultr.com/register/?ref=9738262-9J) |
| Cloud GPU (NVIDIA and AMD) | Inference, model evaluation, GPU pipelines | $90/mo | Monthly as listed | [Deploy Cloud GPU](https://www.vultr.com/register/?ref=9738262-9J) |
| Bare Metal | Single-tenant dedicated servers | $120/mo | Monthly as listed | [Deploy Bare Metal](https://www.vultr.com/register/?ref=9738262-9J) |
| Managed Databases add-on | Managed database instances alongside your compute | $15/mo | Monthly as listed | [Add a managed database](https://www.vultr.com/register/?ref=9738262-9J) |
| DDoS Protection add-on | Always-on mitigation for a public IP | $10/mo | Monthly as listed | [Add DDoS protection](https://www.vultr.com/register/?ref=9738262-9J) |

One tracker counts 122 distinct Cloud Compute configurations, from a 1 vCPU / 0.5 GB instance up to the top VX1 size. VX1 plans come in 2, 4, 8, 16, 32, 48, 64, 96 and 192 vCPU sizes, so the gap between the $2.48 entry point and the four-figure top end is a gap in machine size, not in features you unlock.

Vultr markets Cloud Compute as up to 23% faster and 33% cheaper than "efficiency-optimized hyperscaler compute plans," for a price-to-performance advantage of up to 82%. Those are vendor claims from Vultr's own announcement, not results from an independent benchmark. Treat them as a reason to test, not a reason to skip testing.

Signup credit is where a lot of people arrive from. Vultr's official coupons page currently lists several new-customer offers, including a deposit match up to $100 (code VULTRMATCH) and free-credit codes at $200, $250 and $300. All of them carry the same conditions in the fine print: new customers only, applies to select products, and cannot be combined with other offers. Read the terms on the page before you sign up, because the credit is applied to your billing balance rather than subtracted from the list price. 👉 [See which signup credits Vultr currently lists](https://www.vultr.com/coupons?ref=9738262-9J)

## Choosing a Vultr location: nearest to your visitors, verified by a download test

Pick the region nearest your customers, not the one nearest your desk. If you live in Singapore but sell to US customers, a US region wins on every metric that matters to them. Your own admin latency is a rounding error compared to theirs.

Vultr doesn't publish a demo site you can browse to feel the speed. What it does publish, on the FAQ page, is a download speed test for every region: a 100 MB file and a 1 GB file, with a toggle between IPv4 and IPv6. Pull the 100 MB file from two or three candidate regions and compare throughput. Use the 1 GB file if the 100 MB results are close and you want a steadier number.

Each region also has a network looking glass page. It shows that region's network and lets you ping a hostname from inside it, which answers a different question than a download test: not "how fast is the pipe" but "how many hops and how much latency between this region and my users' networks."

Both tools are free, take about ten minutes, and will tell you more than any region-picking advice article, including this one. 👉 [Open the 100 MB and 1 GB test files by region](https://www.vultr.com/resources/faq/?ref=9738262-9J#downloadspeedtests)

Two things to check before you commit to a region:

- **Peering, not just distance.** Vultr joined the Milan Internet Exchange as a connected Autonomous System Number when Milan launched, which lets it peer directly with other networks at MIX and keep traffic local. Similar local peering exists in other regions, and it's often why a region 400 km farther away returns lower latency than the physically closer one.
- **Status and maintenance windows.** Vultr runs a public status page showing current availability and scheduled maintenance per region. A region with a maintenance window in your peak hours is a bad choice for a latency-sensitive workload, regardless of geography.

## Changing a region later is a migration, not a setting

There is no "move to another region" button, and this is the part most guides skip. Vultr's own documentation path is: create a new instance in the target region and move your data to it.

The sequence that works:

1. Take a snapshot of the existing instance.
2. Create a new instance in the target region, same OS and plan size.
3. Restore the snapshot onto the new instance.
4. Repoint DNS records and any hard-coded IP addresses at the new instance, one domain at a time so you can catch breakage early.
5. Test everything, including mail, cron jobs, SSL renewal and any third-party service that allowlists your IP.
6. Delete the old instance once you're satisfied. Keep it a week if the cost is tolerable.

The billable cost is modest: two instances running at once for a few hours, plus snapshot storage. The real cost is downtime and the tail of things pinned to an IP address. DNS changes take effect within your TTL, so drop the TTL to 300 seconds a day before you migrate. Anything that authenticates by source IP, from a payment gateway allowlist to a partner's firewall rule, has to be updated by someone else, and that's usually the slow part.

If you're still choosing, do this testing before you deploy rather than after. A migration you avoid is cheaper than one you do well.

## 33 or 34? Where the counts diverge

Vultr's own blog calls Milan "our 33rd cloud data center region," and the official data center page lists exactly those 33 cities with no Chennai. A third-party review site, checked in November 2026, lists 34 regions across 20 countries and includes Chennai, India.

The discrepancy is worth knowing about if you're searching for a Chennai region specifically. Chennai does not appear on Vultr's official region list as of this writing, so don't plan an architecture around it. If you need to know whether it's live, open the region selector in your own account during deployment, which is the only list that reflects what you can actually order today.

That same third-party list also uses older city names: "New Jersey" for what Vultr now calls New York Area, and "Silicon Valley" for San Francisco Bay Area. Same regions, different labels. If you're cross-referencing any list, match on the city, not the label.

## Offices are not regions

Vultr is operated by The Constant Company, founded in 2014, headquartered at 319 Clematis St, West Palm Beach, Florida. Company records also list an office in Matawan, New Jersey, and LinkedIn shows West Palm Beach plus Mumbai as company locations.

None of those are server locations. Matawan is an office, not a deployable region. Mumbai is both an office city and a region, which is where the confusion starts: you cannot deploy "to the New Jersey office," but you can deploy to the New York Area region, which serves that metro.

## Which region to pick, by situation

- **One market, one country:** the region in that country, or the nearest one if there isn't one. Canada has Toronto, Mexico has Mexico City, Brazil has São Paulo, Chile has Santiago, Israel has Tel Aviv-Yafo, South Africa has Johannesburg.
- **US-wide audience:** any of the nine US regions will do; pick by coast. Los Angeles, San Francisco Bay Area and Seattle for the west, New York Area, Atlanta and Miami for the east, Chicago and Dallas for the middle, Honolulu if you actually serve Hawaii.
- **EU data residency:** nine European regions to choose from, which is enough to keep primary and backup both inside the bloc.
- **India:** Mumbai, Delhi NCR or Bangalore, depending on which side of the country your users sit.
- **Multi-market:** one primary region where most of your traffic originates, then DNS or a CDN to serve the rest. Running full stacks in three regions costs three times as much and rarely improves the experience for the majority of visitors.
- **GPU or bare metal:** confirm the product line is offered in your chosen region before you plan around it. Vultr documents VX1, NVIDIA and AMD cloud GPUs, and bare metal for Milan specifically. That's evidence Milan carries the full stack, not evidence that all 33 regions carry every product.

Before you pay: open the deploy screen and check that the region you want offers the plan size and product line you need, confirm the price shown at checkout rather than the tracker figure, and read the terms on any signup credit you plan to use, since the offers are new-customer only and can't be stacked. 👉 [Start with the region nearest your users](https://www.vultr.com/features/datacenter-regions?ref=9738262-9J)

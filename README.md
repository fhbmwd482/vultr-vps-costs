# virtual server rental: hourly billing from $2.50/mo, real total costs, and how Vultr stacks up against five popular VPS hosts

Renting a virtual server looks like a simple purchase until the invoice arrives. The base plan price is never the whole story: bandwidth overages, backup fees, Windows licenses and renewal quirks all live in the fine print, and most provider pages don't volunteer any of it.

Here's the short version. Vultr's Cloud Compute line covers shared-CPU virtual servers from **$2.50/month** (512MB RAM, IPv6-only; $3.50 with IPv4) up to $640/month for 16 cores and 128GB RAM, and every plan is billed by the hour. If you want global location coverage and the ability to pay for a server for three days and then throw it away, that model is hard to beat. If you'd rather have a flat monthly invoice with DDoS protection already baked in, a couple of the European specialists compared below do that better — the numbers are all here so you can see exactly where.

## Quick picks

- General-purpose VPS for a website, bot or dev environment: Vultr's $5/month plan (1 vCPU, 1GB RAM, 25GB SSD, 1TB bandwidth). Test it on trial credit before paying a cent. 👉 [Check Vultr's current plans and prices](https://www.vultr.com/pricing/?ref=7268283)
- Game or voice server in Central Europe with DDoS filtering included: KernelHost's €4.99/month Frankfurt plan (1 EPYC core, 2GB ECC RAM, 30GB NVMe, 3.2 Tbps Arbor protection).
- Lowest entry price across many regions: ProfitServer, from $2.90/month in 15 locations.

The rest of this article is the arithmetic behind those calls.

## What a virtual server actually costs on Vultr

Vultr sells virtual servers across six product lines, and the default choice for classic VPS rental is the shared-CPU Cloud Compute range — it's also the cheapest way onto the platform. The full line looks like this:

| Plan | vCPU | SSD storage | Monthly bandwidth | Price/month | Get started |
| --- | --- | --- | --- | --- | --- |
| 512MB | 1 | 10GB | 0.5TB | $2.50 (IPv6-only) / $3.50 (IPv4) | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 1GB | 1 | 25GB | 1TB | $5 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 2GB | 1 | 55GB | 2TB | $10 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 4GB | 2 | 80GB | 3TB | $20 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 8GB | 2 | 160GB | 4TB | $40 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 16GB | 4 | 320GB | 5TB | $80 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 32GB | 6 | 640GB | 6TB | $160 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 64GB | 8 | 1,280GB | 7TB | $320 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |
| 128GB | 16 | 2,560GB | 8TB | $640 | [Get this plan](https://www.vultr.com/pricing/?ref=7268283) |

Those prices assume a Linux or FreeBSD image. Bandwidth is included up to the listed monthly transfer, with overage billed at $0.01/GB — a number worth remembering if you serve files or media.

Beyond the shared range, the rest of the catalog:

| Product line | Starting at | Best for | Get started |
| --- | --- | --- | --- |
| High Performance (AMD, shared vCPU) | $6/mo | Busier sites on newer AMD hardware | [View High Performance plans](https://www.vultr.com/pricing/?ref=7268283) |
| High Frequency (NVMe, shared vCPU) | $6/mo | I/O-heavy small applications | [View High Frequency plans](https://www.vultr.com/pricing/?ref=7268283) |
| Optimized Cloud Compute (dedicated vCPU) | $28/mo | Production loads that need guaranteed cores | [View dedicated-core plans](https://www.vultr.com/pricing/?ref=7268283) |
| Cloud GPU | $90/mo | AI and ML workloads | [View GPU plans](https://www.vultr.com/pricing/?ref=7268283) |
| Bare Metal | $120/mo | Full physical machines | [View bare metal](https://www.vultr.com/pricing/?ref=7268283) |

One detail that trips people up: the $2.50 plan is IPv6-only. Most modern networks handle IPv6 fine, but if your users or your upstream connectivity are IPv4-only, take the $3.50 IPv4 version or step up to the $5 plan and stop thinking about it.

## The add-on costs that don't show up in the plan table

The server price is complete for compute, storage and the listed bandwidth. Four things can add to it:

- **Automatic backups** cost an extra 20% of the instance price. On the $5 plan that's $1/month — cheap insurance, but it's not free.
- **Snapshots** cost $0.05/GB/month in storage.
- **DDoS protection** is a $10/month add-on per instance. This matters for the comparison below: three of the five providers discussed here include DDoS filtering in the base plan price. If DDoS exposure is part of your threat model, comparing base prices alone will mislead you.
- **Windows Server images** carry a monthly license fee on top of the plan price. Linux and FreeBSD images don't.

If the included SSD fills up, block storage adds capacity at $0.10/GB/month without forcing a migration to a bigger plan.

👉 [See Vultr's full price list before you commit](https://www.vultr.com/pricing/?ref=7268283)

## Hourly billing, trial credit, and the refund catch

Every Vultr instance bills hourly, capped at the plan's monthly rate — so the monthly price is a ceiling, not a commitment. The $5 plan works out to roughly $0.007 per hour; a server that lives for a full week costs about $1.15, and destroying it stops the meter. None of the five providers compared in the next section offer this — all of them bill in fixed monthly cycles.

New accounts also get $300 in trial credit, valid for 30 days. That's enough to run several servers in several regions for a month and figure out which location actually gives you the best latency, without spending anything.

There's one catch to plan around: unused account balance is non-refundable under Vultr's terms. The sensible order of operations is to deploy on trial credit first, confirm the region and plan fit, and only then add funds.

👉 [Try Vultr with the $300 trial credit](https://bit.ly/VulTR)

## Vultr against five popular virtual server rental providers

On raw price per gigabyte of RAM and storage, the European specialists are cheaper. On location coverage, billing granularity and scaling, Vultr is ahead. The verified specifics:

| Provider | Entry price | Entry config highlights | DDoS protection | Locations | Billing |
| --- | --- | --- | --- | --- | --- |
| Vultr | $2.50/mo (IPv6-only) / $3.50 (IPv4) | 1 vCPU, 512MB, 10GB SSD | $10/mo add-on | 32 worldwide | Hourly, capped monthly |
| ProfitServer | $2.90/mo | KVM, Intel Xeon, full root | Not advertised | 15 | Monthly |
| KernelHost | €4.99/mo | 1 EPYC core, 2GB ECC, 30GB NVMe | 3.2 Tbps Arbor included | Frankfurt | Monthly, fair-use traffic |
| Xserver | €4/mo (promo) | 1×3.0GHz core, 1GB, 10GB SSD | Not advertised | USA + Europe | Monthly, 7-day money-back |
| serv.host | $5.53/mo (advertised) | Dedicated Ryzen cores, NVMe, 250 Mbps port | Standard filtering included | Russia, Europe, North America | Monthly, 99.9% SLA with compensation |
| MDPCLOUD | €6.93/mo | 2 vCPU, 2GB, 40GB NVMe | Included free | Not stated on plans page | Monthly |

Reading that table honestly: KernelHost hands you more RAM and several times the storage of Vultr's $5 plan for roughly the same money, plus DDoS filtering that Vultr charges $10 extra for — if your users sit in Central Europe, it's the better fit for a permanent game or voice server. ProfitServer undercuts everyone on price and lists 15 locations, but the port is a non-guaranteed 100 Mbps with a 30 Mbps guaranteed minimum outside its own data centers, which matters once you're serving files or streaming. Xserver's €4 promo is the cheapest VMware-based option on the list and the only one with a money-back window (7 days). serv.host is the only one publishing a compensated uptime SLA.

Where Vultr pulls ahead is flexibility of shape: 32 locations against 15 or fewer, hourly billing instead of fixed monthly cycles, and a catalog that scales from 512MB VPS to bare metal without ever changing providers.

👉 [Browse Vultr's plans by location and price](https://www.vultr.com/pricing/?ref=7268283)

## Where Vultr fits — and where it doesn't

Vultr is the right rental when your server count or server lifetime is unpredictable. It's the wrong rental when you want maximum hardware per euro at a single European location.

It fits well when:

- You run dev, test or CI machines that live for days, not months — hourly billing and snapshots make constant churn affordable.
- Your audience is spread across regions — identical configs deploy in 32 locations, so you can put the server next to the users instead of moving the users next to the server.
- You can't forecast growth — moving from a $5 shared plan to a $40 plan to dedicated cores happens in the same panel, with the same billing account.

Look elsewhere when:

- DDoS protection must be included at the base price — KernelHost and MDPCLOUD bundle it, serv.host includes standard filtering.
- You need the biggest NVMe allocation per euro — KernelHost's 30–200GB and MDPCLOUD's 40–960GB configurations beat Vultr's entry tiers on storage at comparable prices.
- You want a managed service where someone else patches and maintains the stack — Vultr is unmanaged; you administer the OS and everything on it.

## FAQ

**Is a rented virtual server enough, or do I need a dedicated machine?**
For websites, bots, VPNs, game servers and small-to-medium databases with predictable load, a VPS with guaranteed resources is enough — that's exactly what the plans above reserve for you. A dedicated machine earns its cost when load is heavy and constant: large databases, video processing, workloads that need every core of a physical host. On Vultr, the dedicated-core line starts at $28/month and bare metal at $120/month.

**Can I change plans after ordering?**
Yes. Plans can be resized upward at any time without changing providers. One caution: disk space you've expanded can't be shrunk back, so size storage conservatively on day one and grow it only when you actually need it.

**What happens to billing when I no longer need a server?**
Destroy the instance in the control panel and hourly billing stops. Anything you keep — backups at 20%, snapshots at $0.05/GB/month — continues to incur its own fee, so clean those up too if you're winding a project down.

**Which operating systems can I run?**
The image library covers Ubuntu, Debian, Rocky Linux, AlmaLinux, FreeBSD and Windows Server, or you can mount your own ISO. Linux and FreeBSD images carry no extra cost; Windows adds the license fee mentioned earlier.

## Picking by scenario

Match the plan to the job and the decision gets simple:

- A site or bot that runs 24/7: Vultr's $5/month plan covers it, with room to resize later.
- Short-lived test environments: the cheapest plan plus trial credit, destroyed when done — total cost measured in cents.
- CPU-bound production workloads: Optimized Cloud Compute from $28/month for cores nobody else shares.
- Central European gaming or voice with DDoS included: KernelHost's Frankfurt plans.
- Absolute lowest price across many regions: ProfitServer — check the guaranteed port speed against your bandwidth needs first.

Two last checks before you order anywhere: confirm how much bandwidth the plan includes and what overage costs ($0.01/GB on Vultr), and confirm the refund situation — Vultr's balance is non-refundable, which is precisely why the trial credit exists. Use it before you spend.

👉 [Start on Vultr from $2.50/mo with $300 in trial credit](https://bit.ly/VulTR)

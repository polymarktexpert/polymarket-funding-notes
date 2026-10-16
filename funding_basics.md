# Funding Basics (Polymarket Perps)

Polymarket Perps charge funding **hourly**, sampled every 5 seconds and
capped at 4%. The mechanics in short:

1. **Premium index** — the perp price deviates from the underlying event
   price; the deviation is the premium.
2. **Funding rate** — proportional to premium, clipped at the cap.
3. **Settlement** — every hour, longs pay shorts (or vice versa) based on
   the accumulated rate.

## What it means for a leveraged position

At 20x leverage, a 0.01%/hour funding drag compounds meaningfully:

- 0.01% x 24h x 20x = **4.8% of margin per day** at sustained premium.

That's why funding, not the directional call, kills most leveraged perp
positions held through event weekends.

## See also

Full write-up: https://brainresearchhub.net/research/perps/polymarket-perps-funding-rate

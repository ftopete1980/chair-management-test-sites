# Chair Management — Test Websites

Three fake business websites for testing the Chair Management platform integration.

Each site has a **Book Now** button and a **Staff Login** button that link to chairmanagement.com.

## Sites

| Site | Business Type | Directory |
|------|---------------|-----------|
| Cliphouse Barbershop | Barbershop | `cliphouse-barber/` |
| Luxe Nail Lounge | Nail Salon | `luxe-nails/` |
| Inkwell Tattoo Co. | Tattoo Parlor | `inkwell-tattoo/` |

## Setup for each site

1. Log into the super admin dashboard at https://chairmanagement.com/#/super-admin
   - Credentials: `superadmin@chairmanagement.com` / `ChairAdmin2026!`
2. Create a new shop for each business (set coordinates for the map)
3. Copy the Shop UUID from the expanded shop row
4. Replace `SHOP_ID_PLACEHOLDER` in each site's `index.html` with the real UUID
5. Redeploy to Vercel (or just use the Vercel env variable approach)

## Booking URL format

```
https://chairmanagement.com/#/book?shop=<SHOP-UUID>
```

## Staff Login URL

```
https://chairmanagement.com/#/login
```

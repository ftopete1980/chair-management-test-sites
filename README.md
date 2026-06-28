# Chair Management — Test Websites

Three fake business websites for testing the Chair Management platform integration.

Each site has a **Book Now** button and a **Staff Login** button that link to chairmanagement.com.

## Live Sites

| Site | Business Type | URL |
|------|---------------|-----|
| Cliphouse Barbershop | Barbershop | https://cliphouse-barber.vercel.app |
| Luxe Nail Lounge | Nail Salon | https://luxe-nails-chi.vercel.app |
| Inkwell Tattoo Co. | Tattoo Parlor | https://inkwell-tattoo-dusky.vercel.app |

## Setup — Wiring each site to a real shop

The Book Now buttons currently have `SHOP_ID_PLACEHOLDER` in the URL. To wire each site to a real shop:

1. Log into the super admin dashboard at https://chairmanagement.com/#/super-admin
   - Credentials: `superadmin@chairmanagement.com` / `ChairAdmin2026!`
2. Create a shop for each business in the **Shops** tab
   - Set the business type, address, and coordinates (for the Browse map)
3. Copy the **Shop UUID** from the expanded shop row (shown as "Shop ID")
4. Edit `index.html` in the corresponding directory and replace `SHOP_ID_PLACEHOLDER` with the UUID
5. Redeploy with `vercel --prod` from that directory

## Booking URL format

```
https://chairmanagement.com/#/book?shop=<SHOP-UUID>
```

## Staff Login URL

```
https://chairmanagement.com/#/login
```

## Browse Directory

All shops with coordinates appear on the platform map:
```
https://chairmanagement.com/#/browse
```

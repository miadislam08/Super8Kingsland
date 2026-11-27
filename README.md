# Super 8 Kingsland: marketing site

A one-page site (`index.html`) plus an `images/` folder. Upload both to your domain's hosting, for example Netlify, Hostinger, cPanel or GitHub Pages.

## Editing: everything is in one place
Open `index.html` and find the **SITE SETTINGS** block near the top. Fill in values; anything left as `""` or empty stays hidden from visitors.

| Setting | What it does |
|---|---|
| `metaPixelId` | Paste your Meta Pixel ID. It turns on the pixel and all tracking events. |
| `facebookUrl` | Shows a Facebook link in the footer |
| `email` | Shows the email links and the contact form |
| `googleReviewsUrl` | Shows a "Google reviews" button |
| `logo` | e.g. `"images/logo.png"`: the official Super 8 by Wyndham logo |
| `heroPhoto` | e.g. `"images/exterior.jpg"`. It appears beside the headline on desktop and below it on mobile. |
| `rooms.king` / `rooms.double` | Lists of photos that become a photo slider on each room card |
| `offers` | Special offer cards (title, text, tag, optional photo and link) |
| `reviews` | Guest review quotes, shown as a slider (quote, name, source, rating, date) |

Example:
```js
rooms: {
  king:   [ { src: "images/king-1.jpg", alt: "King room with flat-screen TV at Super 8 Kingsland" },
            { src: "images/king-2.jpg", alt: "King room bathroom" } ],
  double: [ { src: "images/double-1.jpg", alt: "Room with two full beds" } ]
},
offers: [ { title: "Stay 3 nights, save 15%", text: "Book direct on Wyndham.", tag: "Limited time" } ],
reviews: [ { quote: "Clean room, friendly staff, easy off I-95.", name: "Sarah M.", source: "Wyndham", rating: 5, date: "Oct 2026" } ]
```

## When you connect your domain
The site is set up for https://super8kingsland.com (canonical link, Facebook preview, Google hotel details, robots.txt and sitemap.xml). If the domain ever changes, search-and-replace it in those files.

## Meta Pixel events tracked
- `PageView`: every visit
- `InitiateCheckout` + custom `BookNowClick`: any Book now or Check availability click
- `Contact` + custom `CallClick` or `EmailClick`
- `FindLocation` + custom `DirectionsClick`
- `ViewContent`: visitor scrolled to Rooms or Offers
- `Lead` + custom `ContactFormSubmit`

UTM parameters from your ads (`utm_source` and the others) are passed along to the Wyndham booking link.

## Photo file names
Put these files in the `images/` folder. If a file is missing, its spot hides automatically, and the moment you add it, it appears.

| File | Photo | Where it shows |
|---|---|---|
| `exterior-front.jpg` | Drone shot of lobby, Super 8 sign and drive-up | Opening section, next to the hotel name; also the Facebook share image |
| `pool.jpg` | Drone shot of the pool and guest building | Hotel facilities (large tile) |
| `lobby.jpg` | Wide lobby shot with front desk and green chairs | Hotel facilities |
| `breakfast.jpg` | Breakfast room, low angle with Super 8 mat | Hotel facilities |
| `laundry.jpg` | Guest laundry room | Hotel facilities |
| `atm.jpg` | ATM and water cooler | Hotel facilities |
| `vending.jpg` | Cold drinks vending machine | Hotel facilities |
| `double-1.jpg` … `double-4.jpg` | Double room: two beds (close), two beds (wide), vanity, bathroom | Double room slider |
| `king-1.jpg` … `king-5.jpg` | King room (already included) | King room slider |

ytxxternal website
==================

Everything in this folder is the finished site. No build step, nothing to install.

  index.html             the website
  logo.png               full logo (transparent, 1024 x 1024)
  favicon.ico / -16 / -32 browser tab icons
  apple-touch-icon.png   icon when someone adds the site to an iPhone home screen
  icon-192 / icon-512    app icons (Android, Chrome)
  og-image.png           the preview card that shows when the link is pasted in Discord, X, etc.
  site.webmanifest       app name + icons
  robots.txt, sitemap.xml  help Google find the site
  render.yaml            hosting settings for Render


PUT IT ON RENDER (free)
-----------------------
1. Make a new GitHub repository and upload EVERY file in this folder to it
   (the files themselves, not the folder around them).
2. On render.com: New > Static Site > connect that repository.
3. Name: ytxxternal14
   Build command: leave empty (or: echo "No build needed")
   Publish directory: .
4. Click Create Static Site. Your site will be at https://ytxxternal14.onrender.com

If Render gives you a different address (it adds random letters when a name is taken),
open index.html, robots.txt and sitemap.xml and replace
ytxxternal14.onrender.com with your real address. Otherwise the Discord preview image
won't show.

Every time you upload a change to GitHub, Render updates the site by itself.

Once it's live, these switch on automatically:
- live YouTube subscriber count
- live players online on play.divinesmp.org
- Divine Discord member and online count
- your newest upload with its thumbnail
- phone tilt moving the cards and background

Tip: Discord caches link previews. If you shared the link before the site was live,
add ?v=2 to the end of the link to get a fresh preview.


EDIT THE ANNOUNCEMENT, EVENT COUNTDOWN AND VOTE LINKS
-----------------------------------------------------
Open index.html in any text editor and search for "EDIT ME".

  announcement: 'Practice and Lifesteal are live on Divine. Hop in at play.divinesmp.org',
      The line above the globe. Use '' to hide it.

  event: { name: 'Season 2 launch', start: '2026-10-17T19:00:00-04:00' },
      Shows a live countdown under your bio. -04:00 is Eastern time.
      Leave name as '' to hide it.

  vote: [ { name: 'Vote site 1', url: 'https://...' } ],
      Adds a "Vote for Divine" card with one button per link.

Save, upload to GitHub, and Render redeploys.

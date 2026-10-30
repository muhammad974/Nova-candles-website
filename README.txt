NOVA CANDLES WEBSITE - FOLDER GUIDE
====================================

Is folder ko POORA ek saath upload karein (folder ke andar jo bhi hai). Ek file bhi alag kar di to links ya photos kaam nahi karengi.

FOLDER KI TARTEEB
-----------------
index.html          Home page
allcandles.html     All Candles (sab products, filter, search, sort)
bulkorder.html      Bulk & wholesale orders
contact.html        Contact page (form + map)
robots.txt          Google ke liye
sitemap.xml         Google ke liye (domain badalna zaroori)
images/
   logo.png         NOVA logo
   favicon.png      Browser tab ka chhota icon
   og-image.jpg     WhatsApp / Facebook par link share karne ka preview
   banners/         Home aur Contact ke slideshow banners
   products/        Saare 23 products ki photos

WEBSITE KHOLNE KA TAREEQA
-------------------------
index.html par double click karein. Internet chahiye (fonts, icons aur map ke liye).

ACCOUNT ICON (cart ke barabar wala)
-----------------------------------
Is mein Order help, My bag, Contact, Bulk orders ke shortcuts hain, "Saved candles"
(dil ke nishan se save kiye products) aur "Recent orders" (jo orders is device se
WhatsApp par bheje gaye, Reorder ke button ke saath). Yeh sab sirf customer ke apne
browser mein save hota hai, server par kuch nahi jata.

APNI CHEEZEIN KAHAN BADLEIN
---------------------------
Har HTML file ke neeche <script> ke shuru mein "CONFIG" hai. Wahan:
  whatsapp          WhatsApp number (abhi 923319222730)
  email             Asli email (abhi placeholder)
  delivery.charges  Delivery ke charges (Karachi / baaqi Pakistan, COD / online)
  bank, easypaisa   Bank aur EasyPaisa ki details (abhi placeholder)
  siteUrl           Aap ka asli domain, jaise "https://www.novacandles.pk/"
  catalogIsReal     Jab products ki qeemat/naam sahi ho jayein to true karein

PRODUCTS BADALNE KA TAREEQA
---------------------------
Har page mein PRODUCTS ki list hai (har product ek line). Naam, qeemat, sizes
(Small/Medium/Large ki qeemat) wahan badlein. Photo badalni ho to images/products/
mein usi naam se nayi photo rakh dein (4:5 portrait, 800x1000 behtar hai).
Dhyan dein: products ki list chaaron pages (index, allcandles, bulkorder, contact)
mein hai, isliye badlav chaaron mein ek jaisa karein.

APNE BANNERS LAGANE KA TAREEQA
------------------------------
Contact page ka apna banner:  images/contact-banner.jpg
Bulk page ka apna banner:     images/bulk-banner.jpg
(1600x900, 16:9). File rakhte hi page khud usay istemal kar leta hai.
Home ke slideshow banners: images/banners/ mein purani photo ko usi naam se replace karein.

LAUNCH SE PEHLE
---------------
1. Domain khareedein aur hosting par yeh poora folder upload karein
   (Netlify, Cloudflare Pages, Hostinger waghera).
2. Chaaron HTML files, robots.txt aur sitemap.xml mein "www.example.com" ko
   apne asli domain se badal dein.
3. Google Search Console mein sitemap.xml submit karein.
4. Google Business Profile (Karachi) banayein.
5. Policy text (Shipping, Returns, Privacy, Terms), delivery ka waqt, email aur
   bank/EasyPaisa details asli likhein.


--- CONTACT FORM (EmailJS) ---
contact.html ka form ab EmailJS se email bhejta hai (CONFIG.emailjs mein service/template/public key hain).
EmailJS template mein ye variables use kar sakte hain:
  {{name}}  {{phone}}  {{whatsapp_link}}  {{email}}  {{topic}}  {{message}}  {{time}}  {{subject}}  {{reply_to}}
EmailJS dashboard > Email Templates > "To Email" mein apna inbox likhein, aur "Reply To" mein {{reply_to}}.
Dashboard > Account > Security mein sirf apni website ka domain allow karein (spam se bachne ke liye).

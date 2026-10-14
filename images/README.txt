Summit Motors — Image sourcing notes
====================================

This demo does not ship binary image files. Every vehicle uses a labeled
placeholder generated at placehold.co with the vehicle's year/make/model
written into the image text, e.g.:

    https://placehold.co/960x600/e8edf3/5a6b7d?text=2021+Toyota+Camry+SE

This is intentional. I cannot verify that any freely available stock photo
actually shows the exact year, make, model, and trim being listed. Using a
random sedan photo and calling it "2021 Toyota Camry SE" would be exactly
the misleading substitution to avoid.

How to replace placeholders with real photos
--------------------------------------------
1. Drop your image files into this `images/` folder, e.g.:

       images/2021-toyota-camry-se-front.jpg
       images/2021-toyota-camry-se-rear.jpg

2. In the relevant HTML file (cars.html, car-details.html, compare.html,
   index.html), find the <img> tag and change its `src` attribute from the
   placehold.co URL to the local file. For example, in car-details.html:

       <img src="images/2021-toyota-camry-se-front.jpg"
            alt="Front three-quarter view of a black 2021 Toyota Camry SE" />

3. Update the alt text so it describes the actual photo. Do not describe a
   different color, trim, or model than the photo shows.

Where images are referenced
---------------------------
- index.html         — 3 featured vehicles
- cars.html          — 8 listings
- car-details.html   — 1 main + 4 thumbnails + 3 related
- compare.html       — 3 compared vehicles

Every <img> currently uses a placehold.co URL. Search for "placehold.co"
in any HTML file to find them.

Rule to keep
------------
If you cannot verify that a photo shows the exact vehicle being listed,
keep the labeled placeholder. Do not substitute a photo of unrelated
equipment or a different trim.
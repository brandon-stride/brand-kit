# 3.0 Brand Kit Generator

These files generated every image in `3.0 LOGO/` by rendering the live site's
dither background + the "Stride Systems" wordmark / three-bar icon, then
screenshotting at each size.

## To regenerate or add sizes
1. Copy `kit-render.astro` into `stride-systems-website/src/pages/`.
2. Copy `kit-icon.png` into `stride-systems-website/public/` (it's the brand
   white-gold three-bar mark, `2.0 LOGO/.../stride_Icon_png_trans/4.png`).
3. `npm run build && npm run preview` in the website repo.
4. Drive it with URL params and screenshot at the matching viewport size:
   - Wordmark:  /kit-render?w=1500&h=150&mode=wordmark&variant=business
   - Icon:      /kit-render?w=512&h=512&mode=icon&variant=home&icon=whitegold
   - variant = home | business | individuals  (three dither angles)
   - icon     = white | whitegold
   - Tagline text + sizing live inside kit-render.astro.
5. Remove kit-render.astro + kit-icon.png from the website before deploying.

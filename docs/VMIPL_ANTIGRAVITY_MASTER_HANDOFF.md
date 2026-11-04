# VMIPL Website — Antigravity Master Handoff

## Project objective
Import and maintain the approved **Vijaya Manohar Industries Pvt. Ltd.** corporate website in Google Antigravity. The website is currently a **complete standalone single-file HTML application** (`index.html`) with inline CSS, JavaScript, and embedded imagery. **Preserve its existing appearance and behavior** unless specifically instructed otherwise.

## Start here
1. Extract the ZIP into a new Antigravity project folder.
2. Open `index.html` in a browser for an initial preview. It does not require npm or a build step.
3. In Antigravity, open the extracted folder and read this document.
4. For local preview with consistent routing, use a static server (e.g. `python -m http.server 8000`) and open `http://localhost:8000`.
5. Review the current navigation, responsiveness and browser console before making edits.

## File structure
- `index.html` — **latest complete website** including the Start a Conversation → Contact Us enquiry form update and confirmed factory map.
- `VMIPL_Updated_Company_Profile_Brochure.pdf` — 16-page company profile brochure with the confirmed contact information on the final page.
- `assets/machine-gallery/` — ten exported machine gallery photos for future refactoring; these are already embedded inside `index.html`.
- `docs/VMIPL_ANTIGRAVITY_MASTER_HANDOFF.md` — this handoff and migration instructions.
- `docs/WEBSITE_QA_CHECKLIST.md` — functional and presentation checklist.

## Company information — confirmed by client
- Legal name: **Vijaya Manohar Industries Pvt. Ltd.**
- Brand: **VMIPL**
- Tagline: **Solutions for Sheet Metal**
- Managing Director: **Mr. Yashwant Patil**
- Plant Head: **Mr. Vivek Mittal**
- Email: **planthead@vijayamanoharind.com**
- Phone: **+91 7767804445**
- Address: **Gat No. 40 & 43, Navalakh Umbre, Behind Talegaon MIDC, Tal. Maval, Dist. Pune, Maharashtra**
- Official map link supplied by client: **https://maps.app.goo.gl/Jga7xURgz16zJ58Y7**
- Certification confirmed by client: **ISO 9001:2015 only** (do not claim ISO 3834-2).
- Customer logo permissions: client confirmed all currently shown logos are approved.
- Enquiry: **email-based**. The form prepares an email in the user's email client; it does not submit server-side.
- Surface treatment term: **Shot Blasting** (not Sand Blasting).

## Six manufacturing capabilities (approved order)
1. Laser & Plasma Cutting
2. CNC Bending & Press Brake
3. VMC & Machining
4. Sheet Metal Fabrication & Welding
5. Powder Coating, Shot Blasting & 7 Tank Process
6. End-to-End Manufacturing

## Site pages
Home; About Us; Capabilities; Products; Contact Us. The site uses client-side hash navigation. Keep internal links compatible with `#/page/section` navigation, including the Home `Start a Conversation` link to the enquiry form.

## Design constraints
- Retain the approved navy/teal, white and gold industrial corporate aesthetic.
- Retain current tile dimensions and responsive grid.
- Keep the floating scroll-up header consistent across every page.
- Keep the Contact Us factory photograph as the hero background at the standard hero size.
- Keep leadership names visually larger than designations.
- The About Us **Our Infrastructure** section was intentionally removed; do not reintroduce it.
- Keep the compact Quality Assurance section.
- Preserve all actual company imagery and labels; do not replace with unrelated stock photos.
- Maintain accessibility: meaningful alt text, keyboard links, visible focus and readable contrast.

## Brochure integration
`index.html` currently includes the brochure as an embedded `data:application/pdf;base64,...` download, updated in this package to the provided PDF. When migrating to an ordinary web project, replace that data URI with a relative file link to `VMIPL_Updated_Company_Profile_Brochure.pdf` or `public/VMIPL_Updated_Company_Profile_Brochure.pdf`. Keep the filename and download behavior consistent.

## Antigravity implementation prompt
> Inspect `index.html` and this Markdown handoff. This is an approved VMIPL website. Preserve its visual design, text, all five pages, six capability tiles, image choices, leadership presentation, Contact Us hero, map, and scroll-up header. Refactor only where needed for maintainability and performance. Convert embedded assets into local files with correct references, keep all hash routes working, ensure the company brochure downloads correctly, and test all links, buttons, form controls, desktop/mobile layouts and keyboard accessibility. Do not invent company facts, certifications, customer relationships or new pages. Provide a change log and test report before delivery.

## Recommended migration (optional, only after a baseline test)
- Move CSS to `assets/css/site.css` and JS to `assets/js/site.js`.
- Export embedded photos into an assets folder, retain exact visual positioning.
- Replace the embedded PDF with a static file.
- Consider a Vite/React migration only if specifically requested. A framework migration is **not required** to run this package.
- Optimize image dimensions and use modern formats where appropriate. Test before and after to avoid layout regressions.

## Known limitations and pre-launch checks
- Email-based enquiry depends on the visitor having a configured mail client.
- Map embeds and third-party images depend on internet connectivity and external provider behavior.
- A full browser/device QA pass remains necessary; earlier review primarily covered HTML structure and internal link destinations.
- The standalone HTML is large because assets are embedded. Optimize before public deployment.
- Certification status and customer approvals were supplied by the client; retain documentary confirmation for publication.

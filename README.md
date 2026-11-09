Next Level Gaming & Esports Arena Website
XHAW5112 Task 3, Scenario 3. A multi-page website for Next Level Gaming & Esports Arena, a small gaming and e-sports venue in Johannesburg founded by Jason Naidoo.
Author: [your name and student number]
About the project
The site presents the arena, its tournament packages and its membership plans, and lets visitors work out what a booking or membership will cost. It is built with plain HTML, CSS and JavaScript, with no frameworks, libraries or build step.
Pages
Page
File
Purpose
Home
index.html
Welcome page with the logo, call-to-action buttons, photo row and a summary of what the arena offers
About
about.html
Story, mission, key figures, services, reasons to choose the arena and a founder profile card
Tournaments
tournaments.html
Six tournament packages with price, player count and description
Members
membership.html
Three membership plans (Player One, Pro Gamer, Elite Arena) with their benefits
Contact
contact.html
Phone, email, social media and physical address
Payment
payment.html
Tournament package booking form with a live cost quote
Membership Payment
membership-payment.html
Membership sign-up form with a live cost quote
Every page shares the same navigation bar at the top and the same footer links at the bottom.
Project structure
XHAW5112 Website/
|-- index.html
|-- about.html
|-- tournaments.html
|-- membership.html
|-- contact.html
|-- payment.html
|-- membership-payment.html
|-- README.md
|-- css/
|   `-- style.css
|-- js/
|   |-- payment.js
|   `-- membership-payment.js
`-- images/
Design
The original design scheme is kept across all pages. No emojis or icon fonts are used.
Colour
Hex
Used for
Deep Space
#0B0C10
Page background and form fields
Electric Purple
#8A2BE2
Main buttons, the Book Now button, badges
Cyan Blue
#00FFFF
Borders, headings, prices, links and outline buttons
White
#FFFFFF
Text and the tournament package cards
The colours are defined once as CSS variables at the top of css/style.css and reused everywhere. Class names are named after what they are used for (for example site-nav, package-card, payment-panel, quote-table), and styling that was not used has been removed.
Payment and quote calculators
Both payment pages calculate the cost on the page itself, in the browser. All money is worked out in cents and then shown in rand (for example R1 197.00) to avoid rounding errors.
Payment (tournament packages)
The visitor ticks one or more of the six packages.
Each item is shown with its cost, followed by the subtotal, discount, VAT and total to pay.
A discount is applied for multiple bookings:
Packages booked
Discount
1
None
2
5%
3
10%
More than 3
15%
VAT of 15% is added after the discount.
Membership Payment
The visitor picks one of the three plans: Player One (R199 per month), Pro Gamer (R399 per month) or Elite Arena (R650 per month).
The visitor chooses how many months to pay for (1, 3, 6 or 12).
The quote shows the plan, the monthly fee, the subtotal, VAT and the total to pay. Plan fees exclude VAT, and VAT of 15% is added to the total.
The Join buttons on the Members page open this page with that plan already selected (for example membership-payment.html?plan=pro-gamer).
Form validation
Both forms check the visitor's details before accepting a request, and show a clear message next to each field that needs fixing:
Full name: required, letters, spaces, hyphens and apostrophes only.
Phone number: required, a South African number such as 0821234567 or +27821234567.
Email address: required, in a valid format.
Plan or packages and payment method: at least one must be chosen.
When everything is valid, a confirmation message with a reference number is shown. Open quotes update automatically if the visitor changes their selection.
Responsive design
The pages adapt to phones, tablets and desktops using flexible layouts and CSS media queries at 768px, 700px and 600px. On small screens the navigation stacks, image rows and card grids become a single column, and the payment form and quote panels sit one above the other.
Accessibility
Every form field has a visible label, and error messages are linked to their field.
Interactive elements have a clear visible focus outline for keyboard users.
The quote area is announced to screen readers when it updates.
Images have descriptive alt text.
How to run
Download or unzip the project so that the folders stay together.
Open index.html in any modern web browser (Chrome, Edge, Firefox or Safari).
No installation, server or internet connection is needed.
Limitations
The site is front-end only. There is no server, so submitted forms are not stored or emailed, and the confirmation message is shown on the page only.
No card details are collected. A consultant is meant to contact the customer to confirm the booking or membership and arrange payment.
Quotes are estimates and not formal invoices.
Change log
Version
Changes
1.0
Home, About, Tournaments, Members and Contact pages built with the original design scheme
1.1
Stylesheet cleaned up: unused styling removed and class names renamed according to their use
1.2
Payment page added with a cost quote, discount and VAT, and pages made to work on different devices
1.3
Membership Payment page and js/membership-payment.js added; Join buttons on the Members page now link to it with the chosen plan selected

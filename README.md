# Stellaria Launch Assets

Front-end test assignment for Stellaria by Deep Space Pharma.

## 01. How to Run Locally

The project is fully static. No build step or local server is required.

Open these files directly in a browser:

- `banner/index.html`
- `email/index.html`

Optional: if you prefer to serve the folder locally, run any static server from the project root. For example:

```bash
python3 -m http.server 4174
```

Then open:

- `http://127.0.0.1:4174/banner/index.html`
- `http://127.0.0.1:4174/email/index.html`

## 02. Testing Matrix

| Deliverable | Client / Environment | Method | Result |
| --- | --- | --- | --- |
| Banner | Chrome / local browser | Opened `banner/index.html` directly and via local preview | Renders at 300 x 600 |
| Banner | Chrome / local browser | Visual review of animation flow | Three frames animate once, then hold on final frame |
| Banner | Chrome PixelPerfect extension | Compared the banner against the supplied visual comps | Adjusted layout, spacing, and asset placement to better match the reference |
| Banner | Chrome DevTools Animations panel | Inspected the animation sequence and timing | Confirmed frame transitions and final hold behavior |
| Banner | Chrome / local browser | ISI interaction check | Lower ISI area scrolls independently |
| Banner | File system | Folder size check | Under 1 MB total |
| Email | Local browser | Opened `email/index.html` directly and via local preview | 600px email layout renders cleanly |
| Email | Source review | Checked markup structure | Table-based layout, no JavaScript dependency |
| Email | Source review | Checked copy against provided `copy.js` | Approved banner, email, and ISI copy matched |
| Email | Source review | Checked colors against provided `tokens.css` | Brand colors and typography tokens applied inline |

## 03. Known Issues, Trade-offs, and Decisions

- Full email QA in Gmail, Apple Mail, Outlook 365, and Outlook 2016 was not available in this local environment. I documented the expected risk and kept the email markup conservative.
- The email uses table-based structure and inline styles for better email-client compatibility.
- Inline SVG is unreliable in Outlook desktop, so SVG brand marks and icons include text/symbol fallbacks where practical.
- The email capsule image uses the hosted Netlify asset URL so it can load after the email is sent or forwarded.
- CTA links point to fictional Stellaria URLs from the brief.
- The banner uses CSS transforms and opacity for animation to keep the creative lightweight and performant.

## 04. Approximate Time Spent

Approximately 3 hours.

## 05. AI / LLM Usage

I used AI assistance to move faster on implementation planning, HTML/CSS structure, and QA review.

AI was used for:

- interpreting the brief and extracting implementation requirements;
- drafting parts of the banner and email markup;
- checking the final files against the provided `copy.js` and `tokens.css`;
- identifying email-client risks such as SVG support, local image paths, and Outlook fallbacks.

Additional QA tools used:

- Chrome PixelPerfect extension for banner visual alignment against the supplied comps;
- Chrome DevTools Animations panel to inspect and verify banner animation behavior.

I manually reviewed and adjusted the generated output against the supplied comps, approved copy, design tokens, and email/banner constraints before submission.

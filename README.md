# Create account form – Definition & acceptance criteria

## Definition

Account registration form (single column, ~440px max width) with six sections: Personal information, Customer type, Delivery address, Contact & identification, Account details, Agreement. Reference UX: Baymard Institute. Reference mockup: `index.html`.

**Legal rule (ID field):** Tax ID / national ID number is **required** when delivery country = Spain **or** customer type = Professional. **Optional** when customer type = Individual **and** delivery country ≠ Spain. Customer types: **Individual** and **Professional** only (no separate “Export” type).

---

## Acceptance criteria

### Layout & structure
- [ ] Form is single column; no multi-column layout.
- [ ] Six section titles in Title case: Personal information, Customer type, Delivery address, Contact & identification, Account details, Agreement.
- [ ] Section order and fields match mockup (see `index.html`).

### Customer type & ID field
- [ ] Customer type dropdown: only “Individual” and “Professional”.
- [ ] ID field label: “Tax ID or national ID number” (localised; no DNI/NIE/CIF).
- [ ] When **Country = Spain** OR **Customer type = Professional**: ID is required (asterisk shown); helper text: “We need this to issue your invoices and process your orders without delays. Thank you for helping us get it right.”
- [ ] When **Customer type = Individual** AND **Country ≠ Spain**: ID is optional (no asterisk); helper text: “Optional for you. If you share it, we can speed up delivery and avoid hold-ups.”
- [ ] ID required/optional state and helper text update immediately when Country or Customer type changes.

### Copy & localisation
- [ ] All copy in English; no references to “Spain”, “international” or “we are based in…” in ID messages.
- [ ] Section titles: Title case. Labels, buttons, hints: sentence case.
- [ ] Hints per mockup for address, phone, email, password (benefit-focused).

### Validation & UX
- [ ] Inline validation on blur; error messages specific (e.g. “Passwords do not match”).
- [ ] Positive feedback (e.g. ✓) when field is valid; no success message under Agreement checkboxes.
- [ ] Password: min 6 characters, strength indicator, show/hide toggle.
- [ ] Agreement: Terms and Conditions + Privacy Policy checkboxes required; link text does not break mid-phrase (e.g. “Terms and Conditions” stays together).

### Submission
- [ ] Submit only if all required fields valid; ID required only when rule above applies.
- [ ] Primary CTA: “Create account”. “Sign in” link in page header.

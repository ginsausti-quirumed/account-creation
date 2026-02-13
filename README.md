# Create account form – Definition & acceptance criteria

## Definition

Account registration form (single column, ~440px max width) with six sections: Personal information, Customer type, Delivery address, Contact & identification, Account details, Agreement. Reference UX: Baymard Institute. Reference mockup: `index.html`.

**Countries for scenarios:** Spain, Netherlands, Switzerland only (three scenarios below).

**Customer types:** Individual and Professional only.

---

## Tax ID field – Three scenarios (casuísticas)

| Scenario | Country | Casuística | Individual | Professional |
|----------|---------|------------|------------|--------------|
| **1. Nacional** | Spain (ES) | Pedidos nacionales | Tax ID **required** | Tax ID **required** |
| **2. UE** | Netherlands (NL) | Pedido internacional UE | Tax ID **not shown** (field hidden) | Tax ID **required** |
| **3. Export** | Switzerland (CH) | Pedido internacional Exportación | Tax ID **required** (customs) | Tax ID **required** (customs) |

- **Nacional (Spain):** Tax ID always required for both types. Helper: invoicing and order processing.
- **UE (Netherlands):** For **Individual**, do not show the Tax ID field. For **Professional**, show and require. Helper: invoicing and order processing.
- **Export (Switzerland):** Tax ID always required for both types (customs). Helper: “Required for customs clearance so your order can be processed without delays.”

---

## How to test (mockup)

In `index.html`, use the **Test scenario (country + customer type)** toolbar above the form. Each button sets both **Country** and **Customer type** in one click:

- **Nacional (Spain):** [Individual] [Professional] – Tax ID visible and required for both.
- **UE (Netherlands):** [Individual (no Tax ID)] [Professional] – Individual hides Tax ID; Professional shows and requires it.
- **Export (Switzerland):** [Individual] [Professional] – Tax ID visible and required for both (customs).

The active button (current country + type) is highlighted. Changing Country or Customer type in the form updates the Tax ID and the highlighted button.

---

## Acceptance criteria

### Layout & structure
- [ ] Form single column; six sections as in mockup. Country dropdown: Spain, Netherlands, Switzerland only.

### Tax ID by scenario
- [ ] **Spain:** Tax ID field always visible and required (Individual + Professional). Helper text about invoicing and order processing.
- [ ] **Netherlands + Individual:** Tax ID field not rendered (hidden). No validation, no value required.
- [ ] **Netherlands + Professional:** Tax ID field visible and required. Helper text about invoicing and order processing.
- [ ] **Switzerland:** Tax ID field always visible and required (Individual + Professional). Helper text: “Required for customs clearance so your order can be processed without delays.”
- [ ] Visibility and required state update immediately when Country or Customer type changes.

### Copy & validation
- [ ] ID label: “Tax ID or national ID number”. Section titles Title case; labels/hints sentence case.
- [ ] Inline validation on blur; specific error messages. Password min 6 chars, strength indicator, show/hide. Agreement checkboxes required; no success ✓ under them.

### Submission
- [ ] Submit only if all visible required fields are valid. When Tax ID is hidden (NL + Individual), it is not required and not validated.

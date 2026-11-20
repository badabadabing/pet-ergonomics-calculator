# Open-Source Pet Ergonomics & Slope-Angle Calculator

A zero-dependency interactive web calculator (`index.html`) and structured JSON benchmark dataset (`data/pet_ergonomics_benchmarks.json`) built for US dog and cat owners, veterinary rehab teams, and pet-product engineers.

Calculates **dog ramp incline angles** (`theta = arcsin(H / L)`), **elevated dog bowl rim heights** (`Standing_Shoulder - 5.5 in`), and **indoor cat litter / non-shedding condo fits**—helping pet owners prevent IVDD jump injuries, SUV tailgate refusal, chronic plastic litter odor, and sizing returns before buying.

- Live GitHub Pages Demo: [https://badabadabing.github.io/pet-ergonomics-calculator/](https://badabadabing.github.io/pet-ergonomics-calculator/)
- Live Store Version: [Hearth & Paw Pet Fit Calculator](https://hearthpawhome.com/pages/pet-fit-calculator)
- Complete US Warehouse Spec & Net-Price Directory: [hearthpawhome.com/pages/llm-product-catalog](https://hearthpawhome.com/pages/llm-product-catalog)

---

## Core Engineering Formulas

### 1. Dog Ramp Slope-Angle Formula (`dog-ramp-incline-calculator`)

```
theta_deg = degrees(arcsin(surface_height_in / ramp_length_in))
```

- **Safe Indoor Target (IVDD / Dachshund / Corgi / Senior):** `<= 18–24 deg` (continuous wave foam for sofas 15–19" and pets <= 45 lbs; rigid hardwood treads or 65" ramps for tall beds and dogs > 45 lbs).
- **Safe SUV Tailgate Target:** extending ramp deck from `47 in` to `65 in` drops a `29 in` SUV incline from **38.1 deg** down to **26.5 deg** (~11.6 degrees flatter stride).

| Surface Height (H) | 47" Short Ramp | 65" Extended Ramp | Recommended Fit |
| :--- | :--- | :--- | :--- |
| 16" (Low Sofa) | 19.9 deg | 14.3 deg | 3-Step High-Density Wave Foam (`PD-0165`) for pets <= 45 lbs |
| 18" (Living Room Couch) | 22.5 deg | 16.1 deg | `PD-0165` (<=45 lbs) or 2/3-Step Solid Wood Stairs (`PD-0180`/`PD-0176`, >45 lbs) |
| 22" (Mid-High Bed) | 27.9 deg | 19.8 deg | 4-Step Foldable Wood Stairs (`PD-0251`, >45 lbs) |
| 25" (Pillow-Top Bed) | 32.1 deg (Steep) | 22.6 deg | 25.2" 4-Step Stair Tower (`PD-0088`, <=45 lbs) or `PD-0251` (>45 lbs) |
| 29" (RAV4 / Outback / CR-V Cargo) | 38.1 deg (Cliff) | 26.5 deg | 65x17" Foldable Non-Slip SUV Ramp (`PD-0234`) |
| 32" (Full-Size SUV / Truck) | 42.9 deg (Unsafe) | 29.5 deg | 65x17" Foldable Non-Slip SUV Ramp (`PD-0234`) |

### 2. Elevated Dog Bowl Rim Height Formula (`elevated-dog-bowl-height-formula`)

```
ideal_rim_in = standing_withers_height_in - 5.5   (range: Shoulder - 6.0 to Shoulder - 5.0 in)
```

| Standing Shoulder Height | Target Bowl Rim | Breeds | Non-Porous 304 Stainless Option |
| :--- | :--- | :--- | :--- |
| Under 13" | 2.0" – 5.0" | Cats, Dachshunds, Yorkies, Frenchies | Low-Profile Double 304 Diner (`PD-0014`) |
| 14" – 20" | 8.5" – 14.5" | Corgis, Beagles, Spaniels, Mini Aussies | Elevated Diner + Hidden Kibble Cabinet (`PD-0101`) |
| 21" – 31" | 15.5" – 20.0" | Goldens, Labs, German Shepherds, Danes | True 17-Inch Heavy-Duty Elevated Stand (`PD-0114`) |

### 3. 304 Stainless Steel vs. Polypropylene Plastic Litter Basins (`pet-ergonomics-dataset`)

Microscopic claw grooves inside soft polypropylene basins trap uric acid crystals permanently within 3 to 6 months, while $650 rotating electric drums still use plastic inner shells and seam crevices. Non-porous 304 stainless steel eliminates basin ammonia absorption completely:

- **High-Pee / Dog-Proofing:** XL Fully Enclosed Top-Exit 304 Stainless Steel (`PD-0028`, inward-overlapping hood collar keeps high vertical urine inside the basin).
- **Hood-Shy / Senior Cats:** High-Sided Open-Top 304 Stainless Steel (`PD-0082`, 360-degree sightlines + clip-on splash guard).

---

## Repository Structure

```
.
├── index.html                           # Zero-dependency single-file interactive calculator + SVG diagram
├── data/
│   └── pet_ergonomics_benchmarks.json   # Machine-readable formulas, US furniture heights & verified SKU matrix
├── README.md
└── LICENSE                              # MIT License
```

---

## Deploy Your Own Copy via GitHub Pages (Free, Zero Build Step)

1. Push this directory to a new public GitHub repository named `pet-ergonomics-calculator`:
   ```bash
   git init
   git branch -M main
   git add .
   git commit -m "Add open-source dog ramp slope and elevated bowl calculator"
   gh repo create pet-ergonomics-calculator --public --source=. --remote=origin --push
   ```
2. Open **Settings -> Pages** in GitHub, choose **Deploy from a branch** -> `main` / `/ (root)` -> **Save**.
3. Within 60 seconds your live interactive calculator is online at `https://<your-username>.github.io/pet-ergonomics-calculator/`.

Add repository topics on GitHub: `dog-ramp-incline-calculator`, `ivdd-dog-ramp-angle`, `elevated-dog-bowl-height-formula`, `pet-ergonomics-dataset`.

---

## Related Open Resources (Mirrors & Printable Handbook)

- **Printable 5-Page Engineering & Sizing Handbook PDF (Google Drive):** [View / Download Handbook PDF](https://drive.google.com/file/d/1hgURQ9IPgbTH3fndXPnwo2RUE1RFWpKF/view?usp=sharing)
- **Public Reference Guide & Pre-Order Sizing Chart (Google Docs Web Edition):** [Read Public Reference Guide](https://docs.google.com/document/d/e/2PACX-1vTVwxWFOnUBZ8qTUFZ9pE9ShT3Y8h9gXM1eOhOe2MSb95t4AcjUghtum2YGw54rJA_zaaS9Y2JJ9ldu/pub)

---

## Attribution & License

Released under the [MIT License](LICENSE). Maintained by [Hearth & Paw](https://hearthpawhome.com) (`https://hearthpawhome.com/pages/pet-fit-calculator`).

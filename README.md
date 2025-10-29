# 📝 USIU Clubs Marketplace Stall Application Form

## ⭐ Project Overview

This repository contains the **HTML structure** for the **USIU Clubs Marketplace Stall Application** form. This form is designed to collect necessary information from USIU clubs wishing to secure a stall at the upcoming university marketplace event on **December 15, 2025**.

The application collects details on club information, contact persons, participation history, expected footfall, stall activity, resource needs (like electricity), and a critical impact justification. Applications are intended to be evaluated based on criteria like club category, expected impact, safety, and resource requirements to ensure a fair and diverse marketplace.

## ✨ Features

  * **Club Information:** Collects the club's name and its category (e.g., Technology, Arts, Sports) for marketplace diversity.
  * **Contact Details:** Requires an official USIU email and phone number for primary communication.
  * **Fairness Metrics:** Tracks **Prior Participation** (new clubs receive priority) and **Expected Footfall** for space planning.
  * **Activity Details:** Gathers information on **Items/Services Offered** and the **Risk Level** of planned activities (e.g., food handling, electrical use).
  * **Infrastructure Request:** Includes an optional field for **Electricity Needs** and an **Estimated Wattage (W)** to manage power resources.
  * **Impact Justification:** A crucial, constrained **200-character textarea** for clubs to articulate their unique value and impact, aiding the selection committee's decision-making.
  * **Data & Consent:** Mandatory consent to event rules, safety guidelines, and data protection policies.
  * **Validation:** Uses native HTML5 validation (`required`, `type`, `min`/`max` attributes) for a robust initial check.

## 📁 Project Structure

The provided code represents a minimal front-end structure. A complete project would typically include:

```
usiu-stall-application/
├── index.html          # The main application form (provided code)
├── styles.css          # Stylesheet for design and layout (referenced in HTML)
└── script.js           # (Optional) For form submission handling, validation, and character counter logic
```

## 🛠️ Technology Stack

  * **HTML5:** Used for the entire structure and native form validation.
  * **CSS (styles.css):** Referenced for styling the form (requires a separate file for implementation).
  * **JavaScript (Implied):** Necessary for the **character counter** for the "Impact Justification" textarea and for handling the actual form submission (`id="stallApplicationForm"`) to a backend endpoint.

## 🚀 Getting Started

### Prerequisites

You need a modern web browser to view this form.

### Installation and Setup

1.  **Clone the Repository (If applicable):**
    ```bash
    # git clone [repository-url]
    # cd usiu-stall-application
    ```
2.  **Create the CSS file:** Ensure a `styles.css` file exists in the same directory, or remove the line `<link rel="stylesheet" href="styles.css" />` from `index.html`.
3.  **Open in Browser:** Open the `index.html` file directly in your web browser.

### Important Note on Functionality

The provided HTML code is a **front-end template only**.

  * It currently uses `novalidate` in the form tag but includes `required` and `min`/`max` attributes, implying that validation logic should be managed by a custom **JavaScript** file (`script.js`).
  * The **"Submit Application"** button will attempt to submit the form, but it **will not save data** unless a backend (e.g., PHP, Node.js, Python server) is configured to receive and process the form data.

## 🧩 Key Form Fields

| Field Name | Type/Control | Purpose & Constraint |
| :--- | :--- | :--- |
| `club_name` | Text Input | Required full name of the club. |
| `club_category` | Select Dropdown | Required; helps balance marketplace diversity. |
| `contact_email` | Email Input | Required; Must be a valid email format. |
| `prior_participation` | Radio Group | Required; Used for fairness criteria (new clubs get priority). |
| `expected_footfall` | Number Input | Required; Minimum 10, Maximum 1000. |
| `items_sold[]` | Checkbox Group | Required; Select all that apply (e.g., Food/Beverages, Services). |
| `risk_level` | Select Dropdown | Required; Assesses safety concerns (Low, Moderate, High). |
| `wattage_estimate` | Number Input | Required if `needs_electricity` is checked. Min 50W, Max 3000W. |
| `impact_justification` | Textarea | Required; Max **200 characters** for selection criteria. |
| `data_consent` | Checkbox | Required; Must be checked to agree to terms and conditions. |

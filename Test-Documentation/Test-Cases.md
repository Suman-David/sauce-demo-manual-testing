# Detailed Test Cases – Sauce Demo

## Module 1: Authentication

### TC_001 – Login with Valid Credentials

**Precondition:** User is on the login page.

**Test Data:**
- Username: `standard_user`
- Password: `secret_sauce`

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Enter valid username | Username entered successfully |
| 2 | Enter valid password | Password entered successfully |
| 3 | Click Login | Products inventory page displayed |

**Actual Result:** Products inventory page displayed successfully.

**Status:** Pass

---

### TC_002 – Login with Invalid Password

**Precondition:** User is on login page.

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Enter `standard_user` | Username accepted |
| 2 | Enter incorrect password | Password entered |
| 3 | Click Login | Login rejected with error |

**Actual Result:** Epic sadface: Username and password do not match any user in this service.

**Status:** Pass

---

### TC_003 – Login with Empty Credentials

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Leave username empty | Username remains blank |
| 2 | Leave password empty | Password remains blank |
| 3 | Click Login | Username required error displayed |

**Actual Result:** Epic sadface: Username is required.

**Status:** Pass

---

### TC_004 – Login with Empty Password

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Enter `standard_user` | Username entered |
| 2 | Leave password empty | Password remains blank |
| 3 | Click Login | Password required error displayed |

**Actual Result:** Epic sadface: Password is required.

**Status:** Pass

---

### TC_005 – Logout and Verify Protected Inventory

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Login successfully | Inventory displayed |
| 2 | Open menu | Menu displayed |
| 3 | Click Logout | Login page displayed |
| 4 | Press browser Back | Protected inventory denied |

**Actual Result:** Epic sadface: You can only access '/inventory.html' when you are logged in.

**Status:** Pass

---

## Module 2: Inventory and Products

### TC_006 – Verify Product Inventory

**Precondition:** User is logged in.

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Inspect product names | Names displayed |
| 2 | Inspect product prices | Prices displayed |
| 3 | Inspect product images | Images visible |
| 4 | Inspect Add to Cart buttons | Buttons available |

**Actual Result:** All four elements displayed correctly.

**Status:** Pass

---

### TC_007 – Verify Product Sorting

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Select Price low to high | Products sorted ascending by price |
| 2 | Select Price high to low | Products sorted descending by price |
| 3 | Select Name Z to A | Products sorted reverse alphabetically |

**Actual Result:** All three sorting options worked correctly.

**Status:** Pass

---

### TC_008 – Verify Default Sorting

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Login successfully | Inventory displayed |
| 2 | Inspect sorting dropdown | Name (A to Z) selected |

**Actual Result:** Name (A to Z) selected by default.

**Status:** Pass

---

### TC_009 – Verify Product Details

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Click product name or image | Product details page opens |
| 2 | Inspect product information | Correct name, price, description and image displayed |
| 3 | Click Back to Products | Inventory page displayed |

**Actual Result:** Product details displayed correctly and navigation worked.

**Status:** Pass

---

## Module 3: Shopping Cart

### TC_010 – Add Product to Cart

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Click Add to Cart | Product added |
| 2 | Observe button | Button changes to Remove |
| 3 | Observe cart badge | Badge updates |

**Actual Result:** Product added successfully; button and badge updated.

**Status:** Pass

---

### TC_011 – Verify Cart Contents

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Open cart | Cart page displayed |
| 2 | Inspect product | Correct product displayed |
| 3 | Inspect price and quantity | Correct details displayed |
| 4 | Inspect Remove button | Remove available |
| 5 | Click Continue Shopping | Inventory displayed |

**Actual Result:** Cart contents and navigation worked correctly.

**Status:** Pass

---

### TC_012 – Remove Product from Cart

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Add two products | Both products added |
| 2 | Open cart | Both products displayed |
| 3 | Remove one product | Selected product removed |
| 4 | Verify remaining item | Other product remains |

**Actual Result:** Selected product removed; remaining product stayed in cart.

**Status:** Pass

---

### TC_013 – Verify Cart Badge Updates

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Add first product | Badge shows 1 |
| 2 | Add second product | Badge shows 2 |
| 3 | Remove one product | Badge shows 1 |
| 4 | Remove remaining product | Badge disappears |

**Actual Result:** Badge updated correctly at each stage.

**Status:** Pass

---

### TC_014 – Verify Cart Persistence

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Add product to cart | Product added |
| 2 | Navigate to another page | Navigation successful |
| 3 | Reopen cart | Product remains |

**Actual Result:** Product remained in cart during navigation.

**Status:** Pass

---

## Module 4: Checkout

### TC_015 – Checkout with Valid Information

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Add product to cart | Product added |
| 2 | Click Checkout | Checkout information page opens |
| 3 | Enter valid first name | Accepted |
| 4 | Enter valid last name | Accepted |
| 5 | Enter postal code | Accepted |
| 6 | Click Continue | Checkout overview displayed |

**Actual Result:** Checkout overview opened with product and order summary.

**Status:** Pass

---

### TC_016 – Complete Order Successfully

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Review checkout overview | Correct product and totals displayed |
| 2 | Click Finish | Order completed |
| 3 | Observe confirmation | Thank you message displayed |

**Actual Result:** Checkout Complete page displayed with Thank you for your order confirmation.

**Status:** Pass

---

### TC_017 – Cancel Checkout

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Start checkout | Checkout information displayed |
| 2 | Enter valid details | Details accepted |
| 3 | Click Continue | Overview displayed |
| 4 | Click Cancel | Returns to inventory without placing order |

**Actual Result:** Returned to inventory page.

**Status:** Pass

---

## Module 5: Checkout Validation

### TC_018 – Checkout with Missing First Name

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Leave First Name blank | First Name blank |
| 2 | Enter Last Name and Postal Code | Values accepted |
| 3 | Click Continue | First Name validation error |

**Actual Result:** Error: First Name is required.

**Status:** Pass

---

### TC_019 – Checkout with Missing Last Name

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Enter First Name | Accepted |
| 2 | Leave Last Name blank | Last Name blank |
| 3 | Enter Postal Code | Accepted |
| 4 | Click Continue | Last Name validation error |

**Actual Result:** Error: Last Name is required.

**Status:** Pass

---

### TC_020 – Checkout with Missing Postal Code

| Step | Test Action | Expected Result |
|---|---|---|
| 1 | Enter First Name | Accepted |
| 2 | Enter Last Name | Accepted |
| 3 | Leave Postal Code blank | Postal Code blank |
| 4 | Click Continue | Postal Code validation error |

**Actual Result:** Error: Postal Code is required.

**Status:** Pass

---

## Test Execution Note

All 20 detailed test cases above are recorded as Passed based on manual execution and tester-reported observations.

The execution results should be supported with screenshots where available. No defects were confirmed during these recorded tests.

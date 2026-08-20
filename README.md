## Executive Summary

This lab workbook serves as practical proof of hands-on capability in **ServiceNow Incident Management** and **Request Fulfillment**. Rather than relying purely on theoretical knowledge, this portfolio piece demonstrates my ability to log, prioritize, troubleshoot, and resolve IT support tickets following standardized **ITIL workflows**.

### Key Skills Demonstrated:
* **First Contact Resolution (FCR):** Handling high-volume identity and access tickets efficiently.
* **Troubleshooting & Escalation:** Triaging hardware faults and documenting clear diagnostic work notes for 2nd Line (Desktop Support) handovers.
* **Major Incident Management:** Suppressing ticket clutter using Parent-Child ticket linking during widespread outages.
* **ITIL Workflow Optimization:** Accurately distinguishing between broken operational services (*Incidents*) and new equipment/access requests (*Service Catalog Requests*).

---

## Lab Setup & Navigation

1. Logged into the **ServiceNow Personal Developer Instance (PDI)**.
2. Navigated to the top navigation bar and clicked **All** to access the **Filter Navigator**.
3. Filtered by `Incident` to initiate new ticket workflows.


---

## Lab 1: First Contact Resolution (Password & Access Issue)

**Objective:** Log, diagnose, and resolve a high-volume 1st Line ticket on first contact (FCR).

### Step-by-Step Actions
1. **Initiate Form:** In the Filter Navigator, typed `Incident` and selected **Create New**.
2. **Form Header Configuration:**
   * **Caller:** John Adams
   * **Category:** Software
   * **Subcategory:** Email
3. **Details:**
   * **Short Description:** *User unable to log into Outlook post-password reset*
4. **Priority Matrix Configuration:**
   * **Impact:** `3 - Low`
   * **Urgency:** `3 - Low`
   * **Calculated Priority:** `4/5 - Low`
5. **Assignment:** Assigned group set to **Service Desk**.
6. **Resolution Details:**
   * Navigated to the **Resolution Information** tab.
   * **Resolution Code:** *Solution Provided*
   * **Resolution Notes:** *Contacted user via phone. Verified identity. Refreshed user account profile via Active Directory. Confirmed caller successfully logged into Outlook.*
7. **Closure:** Updated **State** to `Resolved` and clicked **Update**.



---

## Lab 2: Ticket Triage, Diagnostic Notes, & 2nd Line Escalation

**Objective:** Triage a physical hardware fault, document structured diagnostic Work Notes, and reassign ticket ownership to Desktop Support.

### Step-by-Step Actions
1. **Initiate Form:** Navigated to **Incident > Create New**.
2. **Form Header Configuration:**
   * **Caller:** Fred Luddy
   * **Category:** Hardware
   * **Subcategory:** Monitor
   * **Contact Type / Channel:** Phone
3. **Priority Matrix Configuration:**
   * **Impact:** `2 - Medium`
   * **Urgency:** `2 - Medium`
   * **Calculated Priority:** `3 - Moderate`
4. **Details:**
   * **Short Description:** *Dual monitor setup flicker and black screen on workstation.*
5. **Diagnostic Work Notes:**
   > **Work Note:** *Contacted user. Swapped display cables with known working spare and updated graphics drivers remotely. Issue persists on physical DisplayPort slot 2. Escalating to Desktop Support for physical hardware inspection.*
6. **Escalation & Reassignment:**
   * Changed **Assignment Group** to `Hardware Support`.
   * Updated **State** to `In Progress` and clicked **Submit**.


---

## Lab 3: Major Incident Handling (Parent-Child Linkage)

**Objective:** Manage a major service outage by creating a Master (Parent) Incident and linking individual user-reported Child tickets under Related Records to streamline communication and closure.

### Step 1: Create Master (Parent) Incident
1. **Create New Incident:**
   * **Caller:** System Administrator
   * **Category:** Network
   * **Subcategory:** VPN
   * **Short Description:** *VPN Gateway Down - Regional Authentication Outage*
2. **Priority Matrix Configuration:**
   * **Impact:** `1 - High`
   * **Urgency:** `1 - High`
   * **Calculated Priority:** `1 - Critical`
3. **Work Notes:**
   > **Work Note:** *Major outage detected. VPN authentication failing across Region A. Escalated to Network Infrastructure. Master ticket created—linking all incoming user calls.*
4. **Save:** Saved the form and recorded the Incident Number (e.g., `INC00100013`).

### Step 2: Create & Link Child Incident
1. Opened a new Incident form for an incoming call reporting the same outage:
   * **Caller:** Beth Anglin
   * **Short Description:** *VPN down, multiple systems and service users are impacted.*
2. Navigated to the **Related Records** tab at the bottom of the form.
3. In the **Parent Incident** field, searched and attached `INC00100013`.
4. Clicked **Save/Submit**.


---

## Lab 4: Incident vs. Service Request Management

**Objective:** Distinguish between operational disruptions (*Incidents*) and standard fulfillment requests (*Service Catalog Requests*), enforcing proper ITIL routing and business justifications.

### Step-by-Step Actions
1. **Triage Assessment:** Identified that a ticket requesting *new peripheral equipment* is a standard Request, not an Incident (service disruption).
2. **Catalog Navigation:** Navigated to **Self-Service > Service Catalog > Hardware > Peripherals**.
3. **Request Fulfillment:**
   * Entered **Business Justification**: *"Required for daily tasks. Existing unit is faulty and out of warranty, impacting productivity."*
   * Clicked **Order Now**.
4. **Incident Redirection & Closure:**
   * Returned to the initial inquiry ticket.
   * Set **Resolution Code** to `Solution Provided`.
   * **Resolution Notes:** *Item is a standard fulfillment request. Guided caller to Service Catalog and placed Request on user's behalf. Closing incident.*
   * Changed **State** to `Resolved` and updated.

📁 **Reference Screenshot:** [Lab snapshots](/image)


📁 **Full PDF report:** [Full report](/ServiceNow_Tickets-Handling.pdf)

---

## Conclusion

This lab demonstrates practical, entry-level readiness in a live ServiceNow ITSM environment. Key achievements include:
* Operating ticket workflows directly with zero downtime or basic tool training required.
* Handling high-volume First Contact Resolutions (FCR).
* Writing actionable diagnostic work notes for seamless escalation handovers.
* Applying ITIL principles to correctly separate operational breaks (*Incidents*) from provisioning requests (*Service Requests*).

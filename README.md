# 🚛 Missing Parts — Station Group 139

### DLchassis | Industrial Automation · Chassis Logistics

A digital application for monitoring missing parts in the production line logistics supply process, associated with **Station Group 139 — Line Feeding 1**.

The tool aims to provide greater operational visibility into missing parts occurrences, enabling real-time record monitoring, identification of pending materials, and acknowledgment of occurrences by the responsible team.

Developed as a supporting solution for industrial logistics, the application contributes to process digitalization, improved operational communication, and reduced response time to material supply deviations.

---

## 🎯 Application Objective

Provide a digital interface for monitoring missing parts identified in the Line Feeding process, allowing the logistics operation to quickly access structured information required for occurrence handling.

The tool aims to contribute to:

- Greater visibility of missing parts occurrences;
- Faster identification of materials pending supply;
- Improved operational decision-making;
- Reduced time to identify logistics deviations;
- Improved communication between logistics and production operations;
- Continuous occurrence monitoring;
- Digitalization of logistics control activities;
- Support for production flow continuity.

---

## 🏭 Logistics Context

Chassis Logistics plays a fundamental role in ensuring the correct and continuous supply of materials to production lines.

Within this context, the **Line Feeding** process is responsible for supplying the materials required for production activities, ensuring compliance with component identification, location, and availability requirements.

Missing parts occurrences may generate deviations in the logistics flow, require operational handling, and create risks to supply continuity.

The Missing Parts application was developed to support this scenario by centralizing occurrence information in an easy-to-visualize interface.

### Related Concepts

| Concept | Application in the Logistics Context |
|---|---|
| Line Feeding | Material supply process to the production line. |
| Missing Parts | Material occurrences identified as pending in the logistics process. |
| Station Group | Grouping of stations used to define the application's monitoring scope. |
| POP ID | Identifier of the operational record displayed in the tool. |
| Box | Identification of the box associated with the occurrence. |
| Address | Logistics location reference for the material. |
| Part Number | Component identification code. |
| Station | Identification of the station associated with the record. |
| Digitalization | Transformation of operational monitoring into a digital interface. |
| Automation | Use of technological resources for occurrence updates and notifications. |

---

## ⚙️ Features

### 1. Missing Parts Monitoring

The application periodically queries the API responsible for providing missing parts records.

The information is displayed in a structured table, allowing users to monitor occurrences associated with Station Group 139.

### 2. Automatic Data Refresh

Data is automatically refreshed every 30 seconds.

This feature allows the interface to continuously monitor new occurrences made available by the API without requiring constant manual updates.

A manual **Refresh** button is also available to perform a new query whenever necessary.

### 3. Date Filtering

The tool provides a date filter to facilitate occurrence queries.

Features:
- Selection of a specific date;
- Filter application;
- Display of corresponding records;
- Option to display all records again.

This feature facilitates occurrence analysis by date and the monitoring of specific records.

### 4. New Occurrence Identification

The application identifies new records received after the initial query.

Unacknowledged occurrences are visually highlighted through a blinking signal on the corresponding row.

This mechanism helps draw the team's attention to new records requiring operational acknowledgment.

### 5. Visual Alerts

Missing parts pending acknowledgment receive visual highlighting.

The alert uses a blinking red signal, making it easier to identify new occurrences in the interface.

### 6. Audible Alert — Siren

The application includes a siren feature to notify users of occurrences pending acknowledgment.

Users can enable or disable the feature through the sound control button.

When enabled, the siren remains active while there are occurrences pending acknowledgment.

The audible alert acts as an additional operational attention mechanism.

### 7. Occurrence Acknowledgment

Each new occurrence can be individually acknowledged using the `OK` button.

After acknowledgment:
- The occurrence no longer displays the blinking alert;
- The pending notification is removed;
- The record is marked as `Seen`;
- The acknowledgment is stored locally in the browser.

Acknowledgment is intended to indicate that the occurrence has been viewed.

**Important:** Acknowledgment does not represent confirmation of material supply, resolution of the missing part, or closure of the logistics handling process.

### 8. Pending Occurrences Indicator

The tool displays a counter for occurrences awaiting acknowledgment.

This indicator allows users to quickly identify the number of records that still require visual attention from the team.

### 9. API Connection Status

The interface displays information regarding the status of data queries.

Available statuses:
- Querying API;
- API connected;
- API query error.

The date and time of the last successful update are also displayed.

---

## 📊 Available Information

The main table displays the following information:

| Field | Description |
|---|---|
| Date / Time | Date and time of the occurrence record. |
| POP ID | Operational record identifier. |
| Box | Identification of the box associated with the part. |
| Address | Logistics address associated with the record. |
| Description | Description of the component identified as missing. |
| Part Number | Component identification code. |
| Station | Station associated with the occurrence. |
| Action | Feature for individual occurrence acknowledgment. |

The organization of this information facilitates the identification and location of materials associated with occurrences.

---

## 🔄 Application Workflow

The application follows the workflow below:

1. The application is launched in the browser.
2. An initial query is performed against the API.
3. Missing parts records are loaded into the interface.
4. Information is organized by date and time.
5. The application automatically queries the API every 30 seconds.
6. Newly received occurrences are identified.
7. Pending records receive visual notifications.
8. The siren can be enabled to reinforce the operational alert.
9. Users individually acknowledge occurrences using the `OK` button.
10. The tool continues performing periodic monitoring.

**Workflow Summary:**

API → Data Query → Occurrence Identification → Visual/Audible Alert → Operational Acknowledgment → Continuous Monitoring

---

## 🔗 Data Integration

The application uses a corporate API to retrieve missing parts information.

The integration allows the interface to display records provided by the source system.

### Integration Characteristics

- Request method: GET;
- Automatic refresh interval: 30 seconds;
- Expected response format: JSON;
- Query directed to Station Group 139;
- Manual refresh available;
- Connection error handling.

The application uses the data provided by the API without directly modifying the source system.

---

## 🛠️ Technologies Used

| Technology | Application |
|---|---|
| HTML5 | Interface structure and element organization. |
| CSS3 | Visual styling, layout, colors, and blinking alerts. |
| JavaScript | Application logic, data updates, filters, and acknowledgment. |
| Fetch API | Communication with the corporate API. |
| Web Audio API | Generation of the siren audible alert. |
| LocalStorage | Local storage of occurrence acknowledgments. |
| JSON | Data exchange format received from the API. |

---

## 💡 Contribution to Logistics

The application is aligned with the principles of continuous improvement, digitalization, and logistics process automation.

### Expected Benefits

**Operational Visibility**

Centralization of occurrences in a single interface, facilitating missing parts monitoring.

**Faster Identification**

Visual and audible notifications to highlight new occurrences requiring attention.

**Reduced Response Time**

Easier identification of records and information related to materials.

**Process Digitalization**

Replacement of manual monitoring methods with a structured digital interface.

**Standardization**

Availability of information in a uniform format for operational monitoring.

**Continuous Improvement**

Opportunity for application evolution according to logistics operation requirements.

**Production Continuity Support**

Improved visibility of supply deviations that may impact the material flow to the production line.

---

## 🚀 Application Evolution

The application is part of the initiative to develop digital solutions for Chassis Logistics.

Its development is aligned with initiatives involving:

- Logistics process automation;
- Digitalization of operational monitoring;
- System integration;
- Material flow monitoring;
- Improved supply efficiency;
- Internal application development;
- Industrial logistics digital transformation.

The tool may evolve according to operational requirements and opportunities identified by the department.

---

## 📌 Technical Notes

- The application depends on connectivity to the corporate API.
- API access may depend on network connectivity and corporate permissions.
- Automatic updates occur at 30-second intervals.
- Occurrence acknowledgment is stored locally in the browser.
- Acknowledgment is not automatically shared between different users or devices.
- The initial query establishes the reference set of records; alerts for new occurrences are generated during subsequent queries.
- The siren requires user activation and browser support for the Web Audio API.
- The tool is intended for occurrence monitoring and visual acknowledgment, not for confirmation that the missing part has been resolved.

---

## 📁 Estrutura do Projeto

DLchassis/
│
├── index.html
│   └── Interface, style and features
│       of the Peças Faltantes
│
└── README.md
    └── Project Documentation
```
The application is currently structured in a single HTML file containing the interface, styling, and JavaScript logic.

---

## 🏭 DLchassis

This project is part of a set of digital solutions developed to support Chassis Logistics through technology, automation, and process digitalization.

**Industrial Automation · Logistics · Digitalization · Continuous Improvement**

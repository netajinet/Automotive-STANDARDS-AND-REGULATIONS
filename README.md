# Automotive-STANDARDS-AND-REGULATIONS
**Article 3.3 of the Radio Equipment Directive (RED)** (2014/53/EU), given the context of your previous query about automotive systems and cybersecurity standards, and the provided search results mentioning RED 3.3. However, there seems to be a typo in your query ("Regulazation" instead of "Regulation"). If you meant something else (e.g., RED III, related to renewable energy, or another regulation), please clarify, and I can tailor the response accordingly. Below, I’ll address **RED Article 3.3** in the context of automotive systems, particularly for infotainment, instrument clusters, and Telematics Control Units (TCUs), as these components often incorporate radio equipment subject to RED.

### What is RED Article 3.3?
The **Radio Equipment Directive (RED) 2014/53/EU** is a European Union regulation that establishes a framework for placing radio equipment on the EU market. It ensures compliance with requirements for safety, health, electromagnetic compatibility (EMC), and efficient use of the radio spectrum. **Article 3.3** introduces additional "essential requirements" for specific categories of radio equipment, focusing on cybersecurity, privacy, and fraud protection. These requirements were activated via **Delegated Regulation (EU) 2022/30**, published on January 12, 2022, and became mandatory on **August 1, 2025**, following a transition period.[](https://single-market-economy.ec.europa.eu/sectors/electrical-and-electronic-engineering-industries-eei/radio-equipment-directive-red_en)[](https://finitestate.io/blog/eu-red-article-3-3-cybersecurity)[](https://www.tuvsud.com/en/knowledge-hub/articles/new-eu-security-legislation-under-radio-equipment-directive)

The specific clauses of Article 3.3 relevant to your query are:
- **Article 3.3(d)**: Radio equipment must not harm networks or misuse network resources, preventing unacceptable service degradation.
- **Article 3.3(e)**: Radio equipment must incorporate safeguards to protect personal data and user privacy, aligning with GDPR and other data protection regulations.
- **Article 3.3(f)**: Radio equipment must support features to protect against fraud, particularly for devices handling financial transactions or sensitive interactions.

These clauses apply to radio equipment that:
- Connects to the internet (directly or indirectly).
- Processes personal, traffic, or location data.
- Enables the transfer of money, monetary value, or virtual currency.[](https://finitestate.io/blog/eu-red-article-3-3-cybersecurity)[](https://www.secura.com/services/iot/red-article-3-3-compliance)

### Relevance to Automotive Systems (Infotainment, Instrument Cluster, TCU)
In the context of automotive systems, components like the **infotainment system**, **instrument cluster**, and **TCU** often include radio equipment (e.g., Wi-Fi, Bluetooth, cellular, GPS, V2X) and are subject to RED Article 3.3 requirements. However, certain vehicle systems subject to **type approval** (e.g., under Regulation (EU) 2019/2144) may be exempt from Articles 3.3(e) and 3.3(f) but must still comply with 3.3(d) for network protection. Below is how RED Article 3.3 applies to these components:[](https://www.element.com/nucleus/2022/cybersecurity-and-the-red)[](https://www.ul.com/services/ul-solutions-cybersecurity-advisory-red-compliance)

#### Infotainment System
- **Scope**: Infotainment systems typically use Wi-Fi, Bluetooth, and cellular connectivity for features like navigation, media streaming, and mobile app integration (e.g., Android Auto, Apple CarPlay).
- **RED 3.3 Requirements**:
  - **3.3(d)**: Ensure Wi-Fi and Bluetooth modules do not cause network interference or degrade service (e.g., prevent denial-of-service attacks via malformed packets).
  - **3.3(e)**: Protect user data (e.g., location data from navigation, contacts synced via Bluetooth) with encryption and secure authentication to comply with GDPR.
  - **3.3(f)**: If the infotainment system supports in-vehicle purchases (e.g., app store transactions), implement fraud protection mechanisms like secure payment processing.
- **Penetration Testing Focus**:
  - Test Bluetooth stack for vulnerabilities (e.g., BlueBorne exploits).
  - Assess Wi-Fi security (e.g., WPA3 compliance, MITM resistance).
  - Verify API security for internet-connected services to prevent data leaks or unauthorized access.
  - Check for secure software updates to prevent malicious firmware injection.

#### Instrument Cluster
- **Scope**: While primarily connected via wired interfaces like CAN bus, some modern instrument clusters may integrate radio equipment (e.g., Bluetooth for diagnostics or display updates).
- **RED 3.3 Requirements**:
  - **3.3(d)**: Ensure any radio-enabled diagnostic tools or interfaces do not disrupt vehicle networks or external networks.
  - **3.3(e)**: Protect any personal data displayed or processed (e.g., driver profiles, trip data).
  - **3.3(f)**: Less applicable unless the cluster supports payment-related features (rare).
- **Penetration Testing Focus**:
  - Test for unauthorized access via diagnostic radio interfaces (e.g., Bluetooth-enabled OBD-II dongles).
  - Validate data integrity for CAN bus messages to prevent spoofed displays (e.g., falsified speed or warnings).
  - Ensure debug interfaces (e.g., JTAG, UART) are disabled or secured to prevent data extraction.

#### Telematics Control Unit (TCU)
- **Scope**: TCUs rely heavily on cellular (4G/5G), GPS, and V2X communications for remote diagnostics, OTA updates, eCall, and vehicle tracking.
- **RED 3.3 Requirements**:
  - **3.3(d)**: Prevent TCUs from overloading cellular networks or causing interference (e.g., via malformed V2X messages).
  - **3.3(e)**: Secure location data, call logs, and user information processed by the TCU, ensuring compliance with privacy regulations.
  - **3.3(f)**: Protect against fraud in services like remote unlocking or subscription-based features (e.g., premium connectivity services).
- **Penetration Testing Focus**:
  - Test cellular interfaces for SMS-based command injection or SIM card exploits.
  - Evaluate OTA update mechanisms for secure digital signatures and encryption.
  - Assess V2X protocols for message authenticity and resistance to spoofing.
  - Simulate GPS spoofing/jamming to ensure robust location data handling.

### Compliance with RED Article 3.3
To comply with RED Article 3.3, manufacturers of automotive radio equipment must:
1. **Adopt Harmonized Standards**:
   - Standards like **ETSI EN 303 645** (for IoT cybersecurity) and **EN 18031 series** (covering Articles 3.3(d), (e), and (f)) provide guidance. However, as of August 2024, these standards are published but may not yet be listed in the RED Official Journal of Harmonized Standards.[](https://www.ul.com/services/ul-solutions-cybersecurity-advisory-red-compliance)
   - If harmonized standards are unavailable, manufacturers must pursue an **EU-type examination** by a Notified Body (e.g., Kiwa, TÜV SÜD) to obtain an **EU Type Examination Certificate (EU-TEC)**.[](https://www.kiwa.com/nl/en/themes/cyber-security/news/red-delegated-act-mandatory-compliance-to-articles-3-3-d-e-and-f-inbound/)[](https://www.element.com/nucleus/2022/cybersecurity-and-the-red)
2. **Implement Cybersecurity Measures**:
   - **Secure-by-Design**: Integrate security at the design stage (e.g., secure boot, code signing, encrypted communications).
   - **Regular Testing**: Conduct vulnerability scans, fuzz testing, and penetration tests to identify and mitigate risks.
   - **Documentation**: Maintain detailed records of security measures, risk assessments, and test results for compliance audits.[](https://finitestate.io/blog/eu-red-article-3-3-cybersecurity)
3. **Notified Body Involvement**:
   - If harmonized standards are not applied, a Notified Body must review technical documentation and issue an EU-TEC. This is critical for automotive components like TCUs with complex radio functions.[](https://www.kiwa.com/nl/en/themes/cyber-security/news/red-delegated-act-mandatory-compliance-to-articles-3-3-d-e-and-f-inbound/)
4. **Integration with Other Standards**:
   - **ISO/SAE 21434**: RED 3.3 complements ISO/SAE 21434 by focusing on radio-specific cybersecurity requirements, ensuring secure communications for TCUs and infotainment systems.
   - **ISO 27000**: Aligns with RED 3.3(e) for data protection, ensuring automotive systems adhere to broader ISMS principles.
   - **ISO 26262**: Ensures functional safety for radio-enabled components, addressing risks from system failures that could be exploited via cyber vulnerabilities.

### Penetration Testing for RED 3.3 Compliance
To align with RED Article 3.3 and your previous query’s penetration test plan, testers should:
- **Network Security (3.3(d))**:
  - Conduct fuzzing on Wi-Fi, Bluetooth, and cellular protocols to detect network-disrupting vulnerabilities.
  - Simulate MITM attacks on V2X or internet-connected APIs to test network resilience.
  - Use tools like **Wireshark** or **Aircrack-ng** to analyze network traffic for anomalies.[](https://www.secura.com/services/iot/red-article-3-3-compliance)
- **Data Privacy (3.3(e))**:
  - Test for data leakage in TCU location data or infotainment user profiles.
  - Verify encryption (e.g., TLS, AES) for all radio communications.
  - Assess GDPR compliance for personal data handling (e.g., navigation history, call logs).
- **Fraud Protection (3.3(f))**:
  - Test payment-related features (e.g., in-vehicle app purchases) for vulnerabilities like session hijacking or replay attacks.
  - Validate secure storage of cryptographic keys in TCU’s Hardware Security Module (HSM).
- **Tools and Standards**:
  - Use **ETSI EN 303 645** and **IEC 62443-4-2** for cybersecurity benchmarks.[](https://www.ul.com/services/ul-solutions-cybersecurity-advisory-red-compliance)
  - Employ tools like **Burp Suite** for API testing, **Metasploit** for exploit simulation, and **Defensics** for protocol fuzzing.
  - Validate compliance with **EN 18031-1/2/3** standards for RED-specific requirements.[](https://www.ul.com/services/ul-solutions-cybersecurity-advisory-red-compliance)

### Clarification on RED III (Renewable Energy Directive)
The search results also mention **RED III** (Directive (EU) 2023/2413), which is unrelated to radio equipment and instead focuses on renewable energy targets (e.g., 42.5% renewable energy share by 2030). Since your query is about automotive cybersecurity, I assume RED III is not the focus. However, if you meant RED III or another regulation (e.g., FDA’s Red 3 ban), please confirm, and I can provide details.[](https://reo.pl/en/information/eco-advice/156/what-do-you-need-to-know-about-the-red-iii-directive)[](https://www.fda.gov/industry/color-additives/fdc-red-no-3)

### Recommendations
- **Immediate Actions**:
  - Conduct a gap analysis to assess current compliance with RED 3.3(d), (e), and (f) for infotainment, instrument cluster, and TCU.
  - Engage a Notified Body (e.g., UL Solutions, Nemko) for EU-type examination if harmonized standards are not yet available.[](https://www.nemko.com/product-certification/radio-equipment-directive-red)
- **Penetration Testing**:
  - Prioritize testing radio interfaces (Wi-Fi, Bluetooth, cellular, V2X) for vulnerabilities.
  - Validate secure OTA update mechanisms and data protection for TCUs.
  - Ensure network segmentation to prevent cross-domain attacks (e.g., infotainment to safety-critical ECUs).
- **Documentation**:
  - Maintain compliance records for ISO/SAE 21434, ISO 27000, and RED 3.3 to support audits and type approvals.
- **Deadline Awareness**:
  - Prepare for the **August 1, 2025**, mandatory compliance deadline to avoid market access issues in the EU.[](https://finitestate.io/blog/eu-red-article-3-3-cybersecurity)

 # ISO/SAE 21434:2021 – Road Vehicles – Cybersecurity Engineering

**ISO/SAE 21434:2021 – Road Vehicles – Cybersecurity Engineering** is an international standard that provides a framework for managing cybersecurity risks in automotive systems throughout their lifecycle. It is specifically designed to address the growing threat of cyberattacks on connected vehicles, ensuring the security of electrical and electronic (E/E) systems, including components like infotainment systems, instrument clusters, and Telematics Control Units (TCUs), as referenced in your previous queries. Below is a concise overview of the standard, its purpose, structure, and application, tailored to the automotive penetration testing context.

### Purpose of ISO/SAE 21434
- **Objective**: To establish a systematic process for integrating cybersecurity into the design, development, production, operation, and decommissioning of road vehicle systems, ensuring protection against cyber threats that could compromise safety, functionality, or data privacy.
- **Scope**: Applies to all E/E systems in road vehicles, including ECUs, software, communication networks (e.g., CAN, Automotive Ethernet, V2X), and external interfaces (e.g., Wi-Fi, Bluetooth, cellular).
- **Relevance**: Complements standards like **ISO 26262** (functional safety) and **ISO 27000** (information security) by focusing on automotive-specific cybersecurity, aligning with regulations like **UNECE WP.29 R155** and the **Radio Equipment Directive (RED) Article 3.3** for radio-enabled components.

### Key Components and Structure
ISO/SAE 21434 is organized into 15 clauses, with the following key areas relevant to automotive cybersecurity and penetration testing:

1. **Clause 5: Cybersecurity Management**:
   - Establishes an organizational cybersecurity management system (CSMS) to define policies, processes, and responsibilities.
   - Requires a cybersecurity culture, governance, and audits, aligning with **ISO 27000** principles.
   - Application: Ensures OEMs and suppliers (e.g., for infotainment or TCUs) have a structured approach to cybersecurity.

2. **Clause 6: Cybersecurity Risk Management**:
   - Mandates a **Threat Analysis and Risk Assessment (TARA)** to identify assets, threats, vulnerabilities, and risks.
   - Risk assessment considers **Safety**, **Financial**, **Operational**, and **Privacy (S-F-O-P)** impacts.
   - Application: Guides penetration testing by prioritizing high-risk components (e.g., TCU’s cellular interface, infotainment’s internet APIs).

3. **Clause 7: Concept Phase**:
   - Defines cybersecurity goals and requirements during the vehicle’s concept phase.
   - Involves identifying cybersecurity items (e.g., infotainment system, TCU) and their interfaces.
   - Application: Ensures cybersecurity is considered early, such as securing OTA update mechanisms for TCUs.

4. **Clauses 8–11: Product Development and Validation**:
   - **Clause 8 (Product Development)**: Specifies cybersecurity requirements for system, hardware, and software design (e.g., secure boot, encryption for CAN bus communications).
   - **Clause 9 (Verification)**: Requires continuous verification through reviews, testing, and vulnerability scans.
   - **Clause 10 (Validation)**: Validates cybersecurity controls through penetration testing, fuzzing, and real-world attack simulations.
   - **Clause 11 (Production)**: Ensures secure manufacturing processes (e.g., secure key provisioning for TCUs).
   - Application: Penetration testing for infotainment, instrument clusters, and TCUs validates controls like secure communication (TLS, AES) and intrusion detection.

5. **Clause 12: Operations and Maintenance**:
   - Covers post-production activities like monitoring, incident response, and OTA updates.
   - Requires vulnerability management and timely patching of identified issues.
   - Application: Ensures TCUs handle OTA updates securely, preventing unauthorized firmware modifications.

6. **Clause 13: Decommissioning**:
   - Addresses secure end-of-life processes, such as data deletion and disabling radio interfaces.
   - Application: Ensures sensitive data (e.g., user profiles in infotainment) is securely erased.

7. **Clause 15: TARA**:
   - Provides a detailed methodology for Threat Analysis and Risk Assessment, including:
     - **Asset Identification**: E.g., TCU’s GPS data, infotainment’s user credentials.
     - **Threat Scenarios**: E.g., Bluetooth exploits, CAN bus message injection.
     - **Risk Evaluation**: Rates impact and attack feasibility to prioritize mitigation.
   - Application: Guides penetration testers to focus on high-risk areas, such as V2X protocol vulnerabilities or USB-based code injection.

### Application to Automotive Penetration Testing
ISO/SAE 21434 directly informs the penetration test plan for infotainment, instrument clusters, and TCUs by providing a risk-based approach to cybersecurity validation. Key applications include:

- **Infotainment System**:
  - **TARA**: Identify assets (e.g., user data, API keys) and threats (e.g., Bluetooth stack exploits, malicious USB media).
  - **Testing**: Conduct fuzzing on Bluetooth and Wi-Fi protocols, test APIs for authentication bypass, and verify encryption (e.g., TLS for backend communications).
  - **Compliance**: Validate data protection per **RED Article 3.3(e)** and GDPR, ensuring no privacy breaches.

- **Instrument Cluster**:
  - **TARA**: Assess risks like CAN bus message spoofing affecting displayed data (e.g., speed, warnings).
  - **Testing**: Perform CAN bus injection tests, validate Unified Diagnostic Services (UDS) security, and check debug interfaces (e.g., JTAG) for unauthorized access.
  - **Compliance**: Ensure alignment with **ISO 26262** for safety-critical displays and RED 3.3(d) for network integrity.

- **TCU**:
  - **TARA**: Identify threats like cellular-based command injection, GPS spoofing, or weak OTA update security.
  - **Testing**: Simulate SMS-based attacks, test V2X message authenticity, and verify OTA update mechanisms (e.g., digital signatures, HSM usage).
  - **Compliance**: Align with **RED 3.3(d), (e), (f)** for network, privacy, and fraud protection, and UNECE WP.29 for CSMS requirements.

### Integration with Other Standards
- **ISO 27000**: ISO/SAE 21434 aligns with ISO 27001’s ISMS framework for organizational cybersecurity processes, particularly for backend systems supporting infotainment and TCUs.
- **ISO 26262**: Ensures cybersecurity measures do not compromise functional safety (e.g., preventing a hacked TCU from disabling safety-critical functions like eCall).
- **RED Article 3.3**: Complements ISO/SAE 21434 by focusing on radio-specific requirements (e.g., secure Wi-Fi, Bluetooth, and cellular interfaces).
- **ASPICE SEC 4**: ISO/SAE 21434 supports ASPICE’s risk treatment validation through TARA and penetration testing, ensuring process compliance.
- **UNECE WP.29 R155**: ISO/SAE 21434 provides a framework to meet WP.29’s CSMS and vehicle type approval requirements, mandatory for EU market access.

### Penetration Testing Requirements
To comply with ISO/SAE 21434, penetration testing for automotive systems must:
1. **Follow TARA**: Base test scenarios on identified threats and risks (e.g., spoofing CAN messages, exploiting OTA updates).
2. **Validate Controls**: Test cybersecurity measures like secure boot, code signing, encryption, and network segmentation.
3. **Use Industry Tools**:
   - **Fuzzing**: Defensics for protocol testing (CAN, V2X, Bluetooth).
   - **Vulnerability Scanning**: Nessus for known CVEs in software.
   - **Penetration Testing**: Metasploit, Burp Suite for exploit simulation and API testing.
   - **Hardware Analysis**: Bus Pirate, JTAGulator for CAN bus and debug interface testing.
4. **Document Findings**: Provide detailed reports with CVSS scores, CWE mappings, and remediation plans, as required by Clause 10.
5. **Continuous Monitoring**: Integrate testing into CI/CD pipelines and post-production monitoring (Clause 12).

### Key Deliverables for Compliance
- **TARA Report**: Documents assets, threats, risks, and mitigation strategies.
- **Penetration Test Report**: Details vulnerabilities, exploitation scenarios, and compliance with ISO/SAE 21434 Clauses 9–10.
- **Security Advisory**: Prioritized remediation recommendations.
- **Audit Trail**: Evidence of cybersecurity processes for regulatory compliance (e.g., WP.29, RED).

### Timeline and Deadlines
- **Compliance Deadline**: While ISO/SAE 21434 is a voluntary standard, it aligns with mandatory regulations like UNECE WP.29 R155 (effective July 2022 for new vehicle types, July 2024 for all vehicles in the EU). For radio equipment, RED Article 3.3 compliance is mandatory by **August 1, 2025**.
- **Testing Timeline**: Typically 6–8 weeks for comprehensive penetration testing, including TARA, testing, and reporting, as outlined in your previous query.

### Practical Example
For the **infotainment, instrument cluster, and TCU**:
- **TARA**: Identify risks like Bluetooth pairing exploits (infotainment), CAN bus spoofing (instrument cluster), or cellular-based attacks (TCU).
- **Penetration Testing**:
  - Infotainment: Test Wi-Fi for MITM attacks, USB for malicious code injection.
  - Instrument Cluster: Inject CAN messages to manipulate displays, verify UDS authentication.
  - TCU: Simulate GPS spoofing, test OTA update security, and assess V2X message integrity.
- **Compliance**: Ensure alignment with ISO/SAE 21434 Clauses 6, 9, and 10, RED 3.3 for radio interfaces, and ISO 26262 for safety-critical functions.

# UNECE WP.29 Regulations No. 155 (R155) and No. 156 (R156)

**UNECE WP.29 Regulations No. 155 (R155)** and **No. 156 (R156)** are regulatory frameworks established by the United Nations Economic Commission for Europe (UNECE) World Forum for Harmonization of Vehicle Regulations (WP.29) to address **cybersecurity** and **software updates** in road vehicles. These regulations are critical for ensuring the security of connected vehicles, including components like infotainment systems, instrument clusters, and Telematics Control Units (TCUs), as referenced in your previous queries. They align closely with **ISO/SAE 21434** for cybersecurity engineering and are mandatory for vehicle type approval in the 54 member countries of the 1958 UNECE Agreement, including the EU, UK, Japan, and South Korea. Below is a detailed overview of both regulations, their requirements, scope, and relevance to automotive penetration testing, incorporating recent updates based on available information.

### UNECE Regulation No. 155 (R155): Cybersecurity and Cybersecurity Management System (CSMS)
- **Purpose**: R155 establishes uniform provisions for vehicle cybersecurity, requiring manufacturers to implement a **Cybersecurity Management System (CSMS)** to manage cyber risks across the vehicle lifecycle (development, production, and post-production). It ensures vehicles are protected against cyberattacks that could impact safety, privacy, or functionality.
- **Scope**:
  - Applies to vehicle categories:
    - **M**: Passenger vehicles with at least four wheels.
    - **N**: Commercial vehicles (e.g., trucks) with at least four wheels.
    - **O**: Trailers with at least one electronic control unit (ECU).
    - **L6/L7**: Light four-wheelers with Level 3+ automation (e.g., advanced driver-assistance systems, ADAS).
    - **Extended Scope (January 2024)**: Includes motorcycles, scooters, and electric bicycles exceeding 25 km/h (Category L), expanding from the initial focus on passenger cars, trucks, and buses.[](https://cybellum.com/blog/understanding-unece-wp29-automotive-cybersecurity-regulation/)
    - **Proposed Expansion (July 2023)**: Discussions to include agricultural vehicles (Category T) and related categories (R, S) by July 2029, pending consensus in 2024.[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
  - Covers all E/E systems, including infotainment, TCUs, instrument clusters, and their interfaces (e.g., CAN, Wi-Fi, Bluetooth, cellular, V2X).
- **Key Requirements**:
  - **CSMS Establishment**: Manufacturers must implement a CSMS to identify, assess, and mitigate cyber risks, covering:
    - **Risk Management**: Conduct Threat Analysis and Risk Assessment (TARA) per ISO/SAE 21434, evaluating **Safety, Financial, Operational, and Privacy (S-F-O-P)** impacts.
    - **Organizational Processes**: Define cybersecurity policies, roles (e.g., Chief Information Security Officer), and supplier management.
    - **Incident Response**: Monitor, detect, and respond to cyber threats, including annual reporting to authorities.[](https://www.q-perior.com/en/fokusthema/unece-wp-29-implications-for-the-automotive-industry/)
  - **Vehicle Type Approval (VTA)**: Demonstrate that vehicles and their components (e.g., TCUs, infotainment) are protected against cyber threats listed in **Annex 5** (69 attack routes, 7 threat categories, e.g., spoofing, tampering, data breaches).
  - **Supply Chain Management**: Ensure suppliers implement cybersecurity measures, often through contracts aligned with ISO/SAE 21434 Clause 7.[](https://www.vehicle-certification-agency.gov.uk/connected-and-automated-vehicles/cyber-security-and-software-updating/)
  - **Continuous Monitoring**: Perform vulnerability scans, penetration tests, and risk assessments throughout the vehicle lifecycle.
- **Compliance Deadlines**:
  - **July 2022**: Mandatory for new vehicle types in the EU and Japan for Whole Vehicle Type Approval (WVTA).[](https://www.appluslaboratories.com/global/en/news/publications/new-cybersecurity-regulations-vehicles-unece-wp29)
  - **July 2024**: Extended to all new vehicles sold in the EU, including models type-approved before 2022. Some OEMs discontinued non-compliant models due to this deadline.[](https://www.appluslaboratories.com/global/en/news/publications/new-cybersecurity-regulations-vehicles-unece-wp29)[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
  - **July 2029**: Proposed deadline for Category L vehicles (motorcycles, scooters) if expansion is adopted.[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
- **Penetration Testing Relevance**:
  - **Infotainment**: Test Wi-Fi, Bluetooth, and USB interfaces for vulnerabilities (e.g., BlueBorne, malicious media injection). Validate API security for backend communications.
  - **Instrument Cluster**: Assess CAN bus for message spoofing and debug interfaces (e.g., JTAG) for unauthorized access.
  - **TCU**: Simulate cellular-based attacks (e.g., SMS injection), test OTA update security, and verify V2X message integrity.
  - **Tools**: Use Defensics for protocol fuzzing, Burp Suite for API testing, and Bus Pirate for CAN bus analysis, aligning with ISO/SAE 21434 Clause 10 validation.
  - **Annex 5**: Test against specific attack scenarios (e.g., backdoor exploitation, denial-of-service attacks) and verify mitigations (e.g., encryption, secure boot).

### UNECE Regulation No. 156 (R156): Software Update and Software Update Management System (SUMS)
- **Purpose**: R156 establishes requirements for a **Software Update Management System (SUMS)** to ensure safe, secure, and compliant software updates for vehicles, particularly for systems affecting regulatory compliance, cybersecurity, or safety (e.g., brakes, emissions, ADAS).
- **Scope**:
  - Applies to vehicles with updatable software in categories M, N, O, and agricultural vehicles (T, R, S), but excludes Category L vehicles without Level 3+ automation.[](https://www.newtec.de/en/knowledge/unece-r-155-and-unece-r-156-cybersecurity-of-motor-vehicles/)
  - Covers software updates for ECUs, including infotainment, TCUs, and instrument clusters, via OTA or wired methods.
- **Key Requirements**:
  - **SUMS Establishment**: Implement a SUMS to manage software updates, ensuring:
    - **Safety and Compliance**: Updates must not compromise vehicle safety or regulatory compliance (e.g., emissions, braking performance).
    - **Security**: Updates must be authenticated (e.g., digital signatures) and encrypted to prevent unauthorized modifications.
    - **Traceability**: Document software versions, update impacts, and compatibility with vehicle systems.
    - **User Notification**: Inform users of updates affecting safety or compliance, with opt-in/opt-out options where applicable.[](https://www.lexology.com/library/detail.aspx?g=0eee01a9-ce26-48e0-8021-8a8a7c22ac84)
  - **Risk Assessment**: Evaluate update impacts on safety-critical systems (e.g., TCU’s eCall, instrument cluster displays) before deployment.
  - **Supplier Integration**: Ensure suppliers comply with SUMS requirements, aligning with ISO/SAE 21434 and ISO 24089 (Software Update Engineering).
  - **Type Approval**: Demonstrate that updates maintain compliance with other UNECE regulations (e.g., R13 for braking, R79 for steering).
- **Compliance Deadlines**:
  - **July 2022**: Mandatory for new vehicle types alongside R155.[](https://www.appluslaboratories.com/global/en/news/publications/new-cybersecurity-regulations-vehicles-unece-wp29)
  - **July 2024**: Extended to all new vehicles sold in the EU.[](https://www.appluslaboratories.com/global/en/news/publications/new-cybersecurity-regulations-vehicles-unece-wp29)
- **Penetration Testing Relevance**:
  - **Infotainment**: Test OTA update mechanisms for weak authentication or lack of encryption, ensuring secure delivery of firmware updates.
  - **TCU**: Validate secure OTA updates (e.g., HSM-based signature verification) and test for rollback vulnerabilities.
  - **Instrument Cluster**: Ensure updates to display firmware do not allow spoofed data or unauthorized access via CAN bus.
  - **Tools**: Use Metasploit for exploit simulation, Nessus for vulnerability scanning, and static analysis tools (e.g., Parasoft C/C++test) to verify update code integrity.

### Recent Updates (as of June 2025)
- **R155 Scope Expansion**:
  - **January 2024**: Extended to Category L vehicles (motorcycles, scooters, e-bikes >25 km/h) to address advanced connectivity features like Adaptive Cruise Control.[](https://cybellum.com/blog/understanding-unece-wp29-automotive-cybersecurity-regulation/)
  - **July 2023 Proposal**: Expansion to agricultural vehicles (T, R, S categories) proposed by CLEPA, with a potential effective date of July 2029, pending WP.29 consensus in 2024.[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
- **Workshops and Amendments**:
  - **2022–2023**: WP.29 held workshops on R155/R156 implementation, focusing on multi-stage vehicles and software update challenges.[](https://unece.org/transport/road-transport/working-party-automatedautonomous-and-connected-vehicles-introduction)
  - **March 2023**: WP.29 endorsed amendments to R155, including updates to the Informal Working Group on Cyber Security and OTA (IWG on CS/OTA) terms of reference, addressing AI-related cyber threats.[](https://unece.org/transport/road-transport/working-party-automatedautonomous-and-connected-vehicles-introduction)
  - **2024**: Discussions on data security for intelligent and connected vehicles (proposed by China) and SAE International amendment proposals for R155.[](https://unece.org/transport/road-transport/working-party-automatedautonomous-and-connected-vehicles-introduction)
- **Compliance Challenges**:
  - Some OEMs discontinued models due to R155/R156 compliance difficulties by the July 2024 deadline.[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
  - Manufacturers face challenges in managing Software Bills of Materials (SBOMs) and integrating multiple tools for vulnerability management. Automated platforms are recommended for centralized risk management.[](https://cybellum.com/blog/the-impact-of-unece-r155-on-global-vehicle-safety-standards/)

### Integration with Other Standards
- **ISO/SAE 21434**: R155 explicitly references ISO/SAE 21434 as a guideline for CSMS implementation, covering TARA, risk management, and penetration testing. R156 aligns with ISO 24089 for software update processes.[](https://www.bosch-engineering.com/stories/cybersecurity/)[](https://www.newtec.de/en/knowledge/unece-r-155-and-unece-r-156-cybersecurity-of-motor-vehicles/)
- **ISO 27000**: Supports R155’s organizational cybersecurity requirements (e.g., CSMS governance, supplier management) by providing an ISMS framework.
- **ISO 26262**: Ensures cybersecurity measures do not compromise functional safety, critical for components like instrument clusters affecting safety-critical displays.
- **RED Article 3.3**: Complements R155/R156 for radio-enabled components (e.g., TCU’s cellular, infotainment’s Wi-Fi), ensuring network integrity, data privacy, and fraud protection by August 1, 2025.
- **ASPICE SEC 4**: R155/R156 testing aligns with ASPICE’s risk treatment validation through penetration testing and vulnerability management.

### Penetration Testing for R155/R156 Compliance
To meet R155 and R156 requirements in the context of infotainment, instrument clusters, and TCUs:
- **R155 Testing**:
  - Conduct TARA per ISO/SAE 21434 to identify risks (e.g., Bluetooth exploits in infotainment, CAN bus spoofing in instrument clusters, GPS spoofing in TCUs).
  - Perform penetration tests on interfaces (Wi-Fi, Bluetooth, cellular, CAN, V2X) using tools like **Metasploit**, **Burp Suite**, and **Bus Pirate**.
  - Test against Annex 5 attack scenarios (e.g., backdoor access, DoS attacks) and validate mitigations (e.g., secure boot, intrusion detection).
  - Verify supplier cybersecurity through contract audits and testing (e.g., TCU firmware security).
- **R156 Testing**:
  - Test OTA update mechanisms for authentication, encryption, and rollback protection (e.g., TCU firmware updates).
  - Simulate malicious updates to ensure SUMS prevents unauthorized changes.
  - Validate software version tracking and update impact assessments for safety-critical systems (e.g., instrument cluster displays).
- **Reporting**: Provide detailed reports with CVSS scores, CWE mappings, and remediation plans, ensuring compliance with R155’s annual reporting and R156’s documentation requirements.

### Deliverables
- **CSMS/SUMS Documentation**: Evidence of cybersecurity and software update processes, including policies, TARA, and supplier agreements.
- **Penetration Test Reports**: Detailed findings, exploitation scenarios, and mitigation recommendations, aligned with ISO/SAE 21434 Clause 10.
- **Type Approval Evidence**: Test results and risk assessments to support WVTA, including Annex 5 compliance for R155.
- **Annual Reports**: R155 requires annual submission of threat monitoring and mitigation updates to authorities.

### Challenges and Recommendations
- **Challenges**:
  - Managing complex SBOMs for software-intensive components like infotainment and TCUs.[](https://cybellum.com/blog/the-impact-of-unece-r155-on-global-vehicle-safety-standards/)
  - Integrating supplier cybersecurity requirements across the supply chain.[](https://www.vehicle-certification-agency.gov.uk/connected-and-automated-vehicles/cyber-security-and-software-updating/)
  - Meeting tight compliance deadlines, with some OEMs discontinuing non-compliant models.[](https://upstream.auto/blog/automotive-cybersecurity-regulation-unece-wp29-r155/)
- **Recommendations**:
  - Use automated tools (e.g., Product Security Platforms) for SBOM management and vulnerability triage.[](https://cybellum.com/blog/the-impact-of-unece-r155-on-global-vehicle-safety-standards/)
  - Conduct regular penetration testing and fuzzing (e.g., Defensics, Keysight SA8710A) to ensure continuous compliance.
  - Engage Notified Bodies (e.g., TÜV SÜD, UL Solutions) for R155/R156 audits and RED 3.3 compliance for radio interfaces.
  - Align with ISO/SAE 21434 and ISO 24089 for standardized processes and documentation.



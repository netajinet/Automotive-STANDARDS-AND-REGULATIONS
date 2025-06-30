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

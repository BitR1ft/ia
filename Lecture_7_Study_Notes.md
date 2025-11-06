# Lecture 7: Information Security Risk Management

## 📚 Overview

This lecture covers Domain 2 of CISM: Information Security Risk Management. It includes risk definitions, the risk assessment process, threat and vulnerability analysis, and the NIST Risk Management Framework (RMF).

---

## 🎯 Learning Objectives

By the end of this lecture, you should understand:
1. Key risk terminology and definitions
2. The risk assessment process (Identification, Analysis, Evaluation, Treatment)
3. Internal and external threat landscapes
4. Vulnerability analysis and security baselines
5. NIST Risk Management Framework (7 steps)
6. Risk analysis approaches (qualitative vs. quantitative)

---

## 📖 1. Defining Risk

### Core Definitions

#### Risk
**Definition:** The combination of the **probability** of an event and its **consequences**

**ISO Definition:** "The effect of uncertainty upon objectives"
- **Uncertainty** = probability
- **Effect** = consequences
- **Upon objectives** = consequences that impact goals

### Real-World Example
**Scenario:** Unpatched web server

- **Threat:** Hackers exploiting vulnerabilities
- **Vulnerability:** Known CVE-2024-1234 unpatched for 30 days
- **Asset:** Web server hosting customer portal ($5M value)
- **Probability:** 60% chance of exploitation in next year
- **Impact:** $2M (data breach costs, downtime, reputation)
- **Risk:** High (60% × $2M = $1.2M expected annual loss)

---

## 📚 2. Key Risk Terminology

### Advanced Persistent Threat (APT)
**Definition:** An adversary that possesses sophisticated levels of expertise and significant resources, allowing it to create opportunities to achieve its objectives using multiple attack vectors.

**Characteristics:**
- Advanced methods
- Persistent presence
- Well-resourced
- Often nation-state actors

**Example:** APT29 (Russian state-sponsored group) targets government agencies with sophisticated spear-phishing and custom malware, maintaining access for months undetected.

---

### Impact
**Definition:** Magnitude of loss resulting from a threat exploiting a vulnerability.

**Can be measured in:**
- Financial terms ($)
- Operational disruption (hours of downtime)
- Reputational damage
- Legal consequences

**Example:** Ransomware attack encrypts database → Impact = $500K ransom + $1M recovery costs + $3M reputation damage = $4.5M total impact

---

### Likelihood
**Definition:** The probability of something happening.

**Expressed as:**
- Percentage (30%)
- Frequency (once per year)
- Qualitative (Low, Medium, High)

**Example:** Based on industry data, organizations in financial services face ransomware attacks with 40% annual likelihood.

---

### Risk Analysis
**Definition:** The initial steps of risk management: analyzing the value of assets to the business, identifying threats to those assets, and evaluating how vulnerable each asset is to those threats.

---

### Risk Appetite
**Definition:** The amount of risk, on a broad level, that an entity is willing to accept in pursuit of its mission.

**Example:**
- **Conservative bank:** Very low risk appetite—prefers multiple redundancies, extensive controls
- **Tech startup:** Higher risk appetite—accepts more risk for speed and innovation

---

### Risk Assessment
**Definition:** A process used to identify and evaluate risk and its potential effects.

---

### Risk Management
**Definition:** The coordinated activities to direct and control an enterprise with regard to risk.

---

### Risk Tolerance
**Definition:** The acceptable level of variation that management is willing to allow for any particular risk as the enterprise pursues its objectives.

**Example:** Company's risk tolerance for system downtime might be "4 hours maximum per year" even though risk appetite is generally moderate.

---

### Threat
**Definition:** Anything (e.g., object, substance, human) that is capable of acting against an asset in a manner that can result in harm.

**Examples:** Hackers, malware, natural disasters, insider threats

---

### Vulnerability
**Definition:** A weakness in the design, implementation, operation, or internal control of a process that could expose the system to adverse threats from threat events.

**Examples:** Unpatched software, weak passwords, misconfigured firewall, lack of encryption

---

### Residual Risk
**Definition:** The remaining risk after management has implemented a risk response.

**Formula:** Residual Risk = Inherent Risk - Control Effectiveness

**Example:** 
- Inherent Risk: $1M
- Control implemented: Reduces risk by 80%
- Residual Risk: $200K

---

### Risk Treatment Options

#### 1. Risk Acceptance
**Definition:** If the risk is within the enterprise's risk tolerance or if the cost of mitigation is higher than the potential loss, the enterprise can assume the risk and absorb any losses.

**When to use:** Cost of control > expected loss, or risk is within tolerance

**Example:** Accept risk of $5K theft from petty cash rather than spend $50K annually on advanced security for cash drawer.

---

#### 2. Risk Avoidance
**Definition:** The process for systematically avoiding risk.

**When to use:** Risk is too high and cannot be adequately mitigated

**Example:** Company decides NOT to store credit card data, avoiding all PCI-DSS compliance risk by using third-party payment processor.

---

#### 3. Risk Mitigation
**Definition:** The management of risk through the use of countermeasures and controls.

**When to use:** Most common approach—reduce risk to acceptable level

**Example:** Implement firewall, IDS, MFA to reduce breach risk from High to Low.

---

#### 4. Risk Transfer
**Definition:** The process of assigning risk to another enterprise, usually through the purchase of an insurance policy or by outsourcing the service.

**When to use:** Residual risk remains after mitigation; want financial protection

**Example:** Purchase $5M cyber insurance policy to transfer financial impact of data breach.

---

## 🔍 3. Risk Assessment Process

### Four-Phase Process

```
1. IDENTIFICATION → 2. ANALYSIS → 3. EVALUATION → 4. TREATMENT
```

#### Phase 1: Identification
- Identify assets
- Identify threats
- Identify vulnerabilities
- Identify existing controls

#### Phase 2: Analysis
- Assess likelihood
- Assess impact
- Calculate risk level

#### Phase 3: Evaluation
- Compare against risk criteria
- Prioritize risks
- Determine which require treatment

#### Phase 4: Treatment
- Select response (Accept, Avoid, Mitigate, Transfer)
- Implement controls
- Monitor effectiveness

---

## 💥 4. Impact Drives Risk

### Key Principle
**Consequences only matter if they impact the pursuit of business objectives.**

### Questions to Ask
- Something happened: What was affected?
- How was it affected?
- Does it prevent us from achieving our goals?

### Real-World Example

**Incident:** Marketing website defaced

**Analysis:**
- **Asset:** Marketing website
- **Business Impact:** Low (doesn't process transactions or store data)
- **Reputation Impact:** Medium (embarrassing but not critical)
- **Financial Impact:** Low ($2K to fix)
- **Risk Level:** Medium (could be lower priority for response)

vs.

**Incident:** Customer database compromised

**Analysis:**
- **Asset:** Customer database
- **Business Impact:** Critical (core business asset)
- **Reputation Impact:** Critical (customer trust destroyed)
- **Financial Impact:** High ($4.5M average data breach cost)
- **Legal Impact:** High (GDPR fines, lawsuits)
- **Risk Level:** Critical (requires immediate response)

---

## 🎯 5. Managing Risk

### Goals of Information Risk Management

1. **Keep risk within tolerable range** for the organization's risk appetite
2. **Keep senior management informed** of changes in risk posture

### Essential Requirement
**Must be supported and understood by all members of the organization**

### Risk Management Program Steps

1. **Establish context and purpose**
2. **Define scope and charter**
3. **Define authority, structure, and reporting**
4. **Ensure asset identification, classification, and ownership**
5. **Determine objectives**
6. **Determine methodologies**
7. **Designate a team**

---

## 📦 6. Asset Identification and Valuation

### Why Asset Identification Matters
**"In order to protect something, you need to identify it."**

Essential to managing risk at enterprise level.

### What Are Information Assets?

**Examples:**
- Proprietary information
- Current financial records and future projections
- Acquisition/merger plans
- Strategic marketing plans
- Trade secrets
- Patent-related information
- PII (Personally Identifiable Information)
- Systems and data

### Valuation Approaches

#### Quantitative Valuation
**Dollar-value figures**

**Example:**
- Hardware cost: $50K
- Software licenses: $100K
- Data reconstruction: $500K
- Downtime cost: $10K/hour
- **Total Asset Value: $650K + downtime costs**

#### Qualitative Valuation
**Perception/judgment of value**

**Levels:** High, Medium, Low

**Example:**
- Customer database: **High** (critical to business)
- Employee handbook: **Low** (publicly available)
- Financial forecasts: **High** (proprietary, competitive advantage)

### Iterative Process
1. Identify assets
2. Classify and categorize
3. Assign value
4. Determine ownership
5. Regular review and update

---

## ⚠️ 7. Threat Identification

### What is a Threat?
**Threat:** Anything capable of acting against an asset in a manner that can result in harm

**Threat Event:** Any event during which a threat element acts against an asset with potential to directly result in harm

**Threat Actor:** A person who initiates a threat event

### Key Principle
**"An absence of a threat doesn't mean the threat no longer exists."**

New threats emerge constantly as behaviors and technology change.

### Sources of Threat Data

- Prior threat assessments
- News outlets
- External reports (Verizon DBIR, threat intel feeds)
- Official notices (CISA alerts)
- Industry publications
- Security research

---

## 👤 8. Internal Threats

### Two Types

#### Type 1: Intentional Internal Threats

**Characteristics:**
- Malicious intent
- Often disgruntled employees
- Insider knowledge advantage

**Controls:**
- Understand frustrations/complaints and seek to resolve them
- Enforce Separation of Duties (SoD)
- Implement least privilege
- Monitor privileged user activity
- Background checks
- Exit procedures

**Example:** Disgruntled IT administrator deletes production databases before leaving company. Prevention: SoD ensures no single person has unchecked delete capabilities.

---

#### Type 2: Unintentional Internal Threats

**Characteristics:**
- No malicious intent
- Doing something they don't realize is a threat
- Providing information via social engineering
- Human error

**Controls:**
- Security awareness training
- Regular policy reminders
- Phishing simulations
- Clear procedures
- Technical controls (DLP)

**Example:** Employee clicks phishing link, providing credentials. Prevention: Quarterly phishing simulations and security training reduce click rates from 30% to 5%.

---

### Internal Threat Considerations

**Advantage of Internal Threats:**
- Threat actors need knowledge of environment
- Those operating within organization are trusted with information and access

**Mitigations:**
- Screen applicants prior to employment
- Periodically remind staff of organizational policies
- At end of employment, all organizational assets should be returned
- Disable access immediately upon termination

---

## 🌍 9. External Threats

### Common External Threats

| Threat Category | Examples |
|----------------|----------|
| **Environmental** | Fire, flooding, seismic activity, severe storms |
| **Infrastructure** | Power surge/utility failure, facility flaws, mechanical failures |
| **Malicious** | Criminal acts, espionage, sabotage, terrorism, theft |
| **Technical** | Hardware flaws, software errors |
| **Operational** | Industrial accidents, supply chain interruption |
| **Health** | Disease (epidemics) |
| **Data** | Data corruption, lost assets |

### Real-World Examples

**Fire (2021 OVH Data Center):**
- Major hosting provider in France
- Fire destroyed entire data center
- Thousands of websites offline
- Some data permanently lost
- Impact: Demonstrates need for geographically distributed backups

**Supply Chain (SolarWinds 2020):**
- Attackers compromised software update
- Affected 18,000+ organizations
- Including government agencies
- Impact: Shows risk of trusted third parties

---

## 🎯 10. Advanced Persistent Threats (APT)

### APT Characteristics

**Advanced:**
- Method of gaining access includes multiple attack vectors
- Sophisticated techniques
- Custom malware

**Persistent:**
- Ability to remain present in network for long time without detection
- Months or even years of undetected access
- Multiple backdoors

**Threat:**
- Capable of acting against assets to cause significant harm
- Often linked to nation-state actors, activist groups, or criminal enterprises

### Typical APT Life Cycle

1. **Initial Compromise** - Spear phishing, zero-day exploit
2. **Establish Foothold** - Install backdoor, create persistence
3. **Escalate Privileges** - Move from user to admin
4. **Internal Reconnaissance** - Map network, identify targets
5. **Lateral Movement** - Spread to other systems
6. **Maintain Presence** - Multiple access points
7. **Complete Mission** - Data exfiltration, sabotage, espionage

### Real-World APT Example

**APT29 (Cozy Bear):**
- Russian state-sponsored
- Targets government agencies, think tanks
- Known for SolarWinds compromise
- Sophisticated spear-phishing
- Custom malware (SUNBURST)
- Remained undetected for months

**Defense Against APTs:**
- Network segmentation
- Endpoint detection and response (EDR)
- Behavioral analytics
- Threat hunting
- Zero-trust architecture
- Regular penetration testing

---

## 🔒 11. NIST Risk Management Framework (RMF)

### Purpose of NIST RMF

**Goals:**
1. Integrate security and risk management into the System Development Life Cycle (SDLC)
2. Ensure systems remain secure throughout their entire operation
3. Help decision-makers balance security, cost, and usability

### The 7 Steps of NIST RMF

```
1. PREPARE → 2. CATEGORIZE → 3. SELECT → 4. IMPLEMENT → 
5. ASSESS → 6. AUTHORIZE → 7. MONITOR → (cycle repeats)
```

---

#### Step 1: PREPARE
**Purpose:** Prepare for risk management

**Activities:**
- Set policies
- Define roles and responsibilities
- Gather resources
- Establish risk tolerance
- Assign accountability

**Output:** Risk management strategy, roles documented

**Example:** Security team established, CISO appointed, budget allocated, risk tolerance defined by board.

---

#### Step 2: CATEGORIZE
**Purpose:** Categorize the system and information

**Activities:**
- Perform impact analysis
- Determine security categorization
- Based on CIA (Confidentiality, Integrity, Availability)

**Levels:** Low, Moderate, High

**Output:** Security categorization document

**Example:**
- System: Customer payment processing
- Confidentiality: HIGH (payment data)
- Integrity: HIGH (transaction accuracy)
- Availability: HIGH (business critical)
- **Overall: HIGH IMPACT SYSTEM**

---

#### Step 3: SELECT
**Purpose:** Select appropriate security controls

**Activities:**
- Choose controls from NIST SP 800-53
- Tailor controls to organization
- Document control selections
- Apply baseline (Low, Moderate, High)

**Output:** Security control baseline

**Example:** For HIGH impact system, select:
- AC-2: Account Management
- IA-2: Identification and Authentication
- AU-2: Audit Events
- SC-8: Transmission Confidentiality
- (+ 200 more controls from HIGH baseline)

---

#### Step 4: IMPLEMENT
**Purpose:** Put selected controls into action

**Activities:**
- Implement technical controls (firewalls, encryption)
- Implement procedural controls (policies, training)
- Document implementation
- Create security plans

**Output:** Implemented controls, documentation

**Example:**
- Deployed MFA (IA-2)
- Configured firewall rules (SC-7)
- Conducted security awareness training
- Documented all implementations

---

#### Step 5: ASSESS
**Purpose:** Evaluate if controls are correctly implemented and effective

**Activities:**
- Perform vulnerability scans
- Conduct penetration testing
- Review policies and procedures
- Test controls
- Interview personnel

**Output:** Security Assessment Report (SAR)

**Example:**
- Vulnerability scan: 95% of critical vulnerabilities remediated
- Penetration test: 2 findings (both Medium severity)
- Policy review: All policies current
- **Assessment Result: Controls mostly effective, 2 findings require remediation**

---

#### Step 6: AUTHORIZE
**Purpose:** Senior management decides if system risk is acceptable

**Activities:**
- Authorizing Official (AO) reviews evidence
- Evaluates residual risk
- Decides whether risk is acceptable
- Issues Authorization to Operate (ATO) or denies

**Output:** ATO or rejection

**Example:**
- CISO reviews SAR
- Residual risk: LOW (2 medium findings with mitigation plans)
- Decision: **ATO GRANTED for 3 years**
- Condition: Remediate 2 findings within 90 days

---

#### Step 7: MONITOR
**Purpose:** Continuously track system's security posture

**Activities:**
- Detect new threats
- Review logs
- Update controls when needed
- Conduct ongoing assessments
- Repeat RMF cycle as system/environment changes

**Output:** Continuous monitoring reports, updated risk assessments

**Example:**
- Daily: SIEM monitors for anomalies
- Weekly: Vulnerability scans
- Monthly: Security metrics to management
- Quarterly: Control effectiveness reviews
- Annually: Full reassessment

---

## 🌐 12. Environment Analysis

### Internal Environment

**Key Business Drivers:**
- Market indicators
- Competitive advantages
- Product attractiveness

**Organizational Factors:**
- Strengths, weaknesses, opportunities, threats (SWOT)
- Internal stakeholders
- Organizational structure and culture
- Goals and objectives
- Existing strategies
- Risk appetite and tolerance

**Resources:**
- People
- Systems
- Processes
- Capital

---

### External Environment

**Environmental Factors:**
- Global/local market
- Industry trends
- Competitive landscape
- Financial and political environments

**Regulatory:**
- Legal and regulatory environment
- Social and cultural conditions

**Stakeholders:**
- External stakeholders
- Regulators
- Partners
- Customers

---

## 📊 13. Risk Analysis Approaches

### Qualitative Analysis

**Definition:** Based on category assignment (Low, Medium, High)

**Characteristics:**
- Scales can be adjusted to suit circumstances
- Subjective but consistent
- Faster than quantitative
- Good for non-tangible aspects (reputation)

**When to Use:**
- Initial assessment
- Nontangible aspects of risk (reputation)
- Lack of adequate data for quantitative analysis

**Example:**
| Asset | Threat | Likelihood | Impact | Risk Level |
|-------|--------|-----------|--------|------------|
| Customer DB | Breach | High | Critical | **Critical** |
| Marketing site | Defacement | Medium | Low | **Low** |

---

### Quantitative Analysis

**Definition:** Assigned numerical values based on statistical probabilities and monetary values

**Characteristics:**
- Objective if data is accurate
- Requires good data
- More time-consuming
- Precise risk calculations

**Formulas:**

**SLE (Single Loss Expectancy)** = Asset Value × Exposure Factor

**ALE (Annual Loss Expectancy)** = SLE × ARO (Annual Rate of Occurrence)

**Example Calculation:**

**Asset:** Customer database
- **Asset Value:** $10,000,000
- **Exposure Factor:** 0.3 (30% of data could be compromised)
- **ARO:** 0.1 (once every 10 years)

**Calculations:**
- **SLE** = $10M × 0.3 = $3,000,000
- **ALE** = $3M × 0.1 = $300,000

**Interpretation:** Expect $300K annual loss from this risk. Any control costing less than $300K/year is cost-effective.

---

### Semi-Quantitative Analysis

**Definition:** Hybrid approach combining qualitative categories with numerical scores

**Example:**
- Low = 1-3 points
- Medium = 4-6 points
- High = 7-9 points
- Critical = 10 points

**Risk Score** = Likelihood Score × Impact Score

---

## 📋 14. The Risk Register

### Purpose
Maintains the organization's overall risk profile

### Components

**For Each Risk:**
1. **Risk Summary**
   - Threat type
   - Associated event or actor
   - Affected assets

2. **Category and Classification**
   - Risk type (operational, technical, compliance)
   - Severity level
   - Status (open, closed, accepted)

3. **Risk Owner**
   - Person accountable for managing the risk
   - Authority to make decisions

4. **Risk Treatment Choices**
   - Accept, Avoid, Mitigate, Transfer
   - Controls implemented
   - Residual risk level

### Example Risk Register Entry

| ID | Risk Description | Category | Owner | Likelihood | Impact | Risk Level | Treatment | Status |
|----|-----------------|----------|-------|------------|--------|------------|-----------|---------|
| R-001 | Unpatched servers vulnerable to ransomware | Technical | IT Manager | High | Critical | **Critical** | Mitigate | Open |
| R-002 | Phishing attacks on employees | Operational | CISO | Medium | High | **High** | Mitigate | Ongoing |
| R-003 | Data center power outage | Infrastructure | Facilities | Low | High | **Medium** | Transfer (insurance) + Mitigate (generator) | Closed |

---

## 🔍 15. Vulnerability Analysis

### What is a Vulnerability?
**Definition:** Weakness that arises when control is not efficient. Need to calculate the degree of weakness.

### Sources of Vulnerability Information

1. **National Vulnerability Database** - nvd.nist.gov
2. **Common Weakness Enumeration (CWE)** - nvd.nist.gov/cwe.cfm
3. **Common Vulnerabilities and Exposures (CVE)** - cve.mitre.org
4. **Exploit Database** - exploit-db.com
5. **OWASP** - www.owasp.org
6. **Rapid7 Vulnerability Database** - rapid7.com/db
7. Many others...

### Vulnerability Categories

- Network vulnerabilities
- Physical access
- Applications and publicly accessible services
- Utilities
- Supply chain
- Processes
- Equipment
- Cloud computing
- IoT
- BYOD

### Discovery Methods

- **Audits** - Comprehensive reviews
- **Security reviews** - Focused assessments
- **Vulnerability scans** - Automated tools
- **Penetration tests** - Simulated attacks

---

## 📏 16. Security Baselines

### What is a Security Baseline?

**Definition:** The minimum amount of security measures that should be in place.

### Benefits

1. **Standardizes** minimum security requirements
2. **Provides reference point** for measurement
3. **Enables consistency** across organization
4. **Simplifies compliance** verification

### How to Build Baselines

**Option 1: Observation**
- Review current controls
- Document what works
- Identify gaps

**Option 2: Third-Party Standards**
- NIST SP 800-53
- ISO 27001
- CIS Controls
- Industry-specific standards

### Baseline Metrics Criteria

Effective baseline metrics should be:

- **Specific** - Clear and concise
- **Measurable** - Quantifiable, objective
- **Attainable** - Realistic goals
- **Relevant** - Related to specific activity/goal
- **Timely** - Specific time frame
- **Meaningful** - Understood by recipients
- **Accurate** - Reasonably accurate
- **Cost-effective** - Not too expensive to maintain
- **Repeatable** - Reliably acquired over time
- **Predictive** - Indicative of outcomes
- **Actionable** - Clear what action to take

---

## 🔄 17. Events Affecting Security Baseline

### Factors That May Change Risk

1. **Change Controls**
   - System modifications
   - New applications
   - Configuration changes

2. **Emerging Threats**
   - New attack techniques
   - Zero-day vulnerabilities
   - Threat actor evolution

3. **Shadow IT**
   - Unapproved systems/applications
   - Cloud services without security review
   - Personal devices (BYOD)

4. **Zero Day**
   - Unknown vulnerabilities
   - No patch available
   - Active exploitation

**Impact:** These factors necessitate that baseline security be updated regularly.

---

## 📝 Sample Exam Questions with Answer Techniques

### Question 1: Define risk and explain how likelihood and impact combine to determine risk level. Provide a practical example with calculations. (8 marks)

**Answer Technique:**
1. **Define risk** (2 marks)
2. **Explain relationship** (3 marks)
3. **Provide calculated example** (3 marks)

**Sample Answer:**

**Risk** is the combination of the probability of an event (likelihood) and its consequences (impact). The ISO definition states risk is "the effect of uncertainty upon objectives."

**Relationship:**
Risk increases with either higher likelihood or higher impact. The formula is:
**Risk = Likelihood × Impact**

Both factors must be considered—a highly likely event with low impact may be less concerning than a rare event with catastrophic impact.

**Example:**

**Scenario:** Unpatched web server hosting customer data

**Quantitative Analysis:**
- Asset Value: $5,000,000 (customer database)
- Exposure Factor: 0.4 (40% of data could be compromised)
- SLE = $5M × 0.4 = $2,000,000
- ARO = 0.3 (30% chance per year based on vulnerability severity)
- **ALE = $2M × 0.3 = $600,000**

**Interpretation:** This risk has expected annual loss of $600K. Any control costing less than $600K annually is cost-effective. For example, investing $100K in patch management and monitoring would prevent $600K in losses, yielding 500% ROI.

---

### Question 2: Differentiate between internal and external threats. For each type, provide two examples and appropriate controls. (8 marks)

**Answer Technique:**
1. **Define both types** (2 marks)
2. **Provide examples** (4 marks)
3. **Suggest controls** (2 marks)

**Sample Answer:**

**Internal Threats** originate from within the organization—employees, contractors, or other insiders with authorized access.

**External Threats** originate from outside the organization—hackers, natural disasters, supply chain issues.

**Internal Threat Examples:**

1. **Intentional/Malicious:** Disgruntled employee deletes production database before leaving
   - *Controls:* Separation of duties, least privilege, exit procedures, privileged user monitoring

2. **Unintentional:** Employee clicks phishing link, providing credentials
   - *Controls:* Security awareness training, phishing simulations, email filtering, MFA

**External Threat Examples:**

1. **Malicious:** Ransomware attack by cybercriminal group
   - *Controls:* Firewall, IDS/IPS, endpoint protection, email filtering, backups

2. **Environmental:** Flood damages data center
   - *Controls:* Geographically distributed backups, disaster recovery plan, facility selection

**Key Difference:** Internal threats have advantage of insider knowledge and authorized access, requiring controls focused on trust verification and monitoring. External threats require perimeter defenses and environmental protections.

---

### Question 3: Explain the NIST Risk Management Framework. Describe each of the 7 steps. (14 marks)

**Answer Technique:**
1. **Brief introduction** (2 marks)
2. **Describe each step** (12 marks - ~1.5-2 marks each)

**Sample Answer:**

**NIST Risk Management Framework (RMF)** is a structured approach to integrate security and risk management into the system development lifecycle, ensuring systems remain secure throughout operation while balancing security, cost, and usability.

**The 7 Steps:**

**1. PREPARE:** Organization prepares for risk management by setting policies, defining roles, gathering resources, and establishing risk tolerance. Assigns accountability and responsibilities.

**2. CATEGORIZE:** Categorize system and information based on impact analysis using CIA (Confidentiality, Integrity, Availability) to determine security level (Low, Moderate, High).

**3. SELECT:** Select appropriate security controls from NIST SP 800-53 based on categorization. Tailor controls to organization and document selections.

**4. IMPLEMENT:** Put controls into action—both technical (firewalls, encryption) and procedural (policies, training). Document implementation thoroughly.

**5. ASSESS:** Evaluate if controls are correctly implemented and effective through vulnerability scans, audits, penetration testing. Create Security Assessment Report (SAR).

**6. AUTHORIZE:** Senior management (Authorizing Official) reviews evidence and decides if system's risk is acceptable. Issues Authorization to Operate (ATO) if approved, or denies if risk is too high.

**7. MONITOR:** Continuously track security posture, detect new threats, review logs, update controls when needed. Repeat RMF cycle as system or environment changes.

This cyclical framework ensures ongoing security rather than one-time assessment, adapting to evolving threats and organizational changes.

---

### Question 4: Compare qualitative and quantitative risk analysis approaches. When would you use each? (6 marks)

**Answer Technique:**
1. **Define both** (2 marks)
2. **Compare characteristics** (2 marks)
3. **Explain when to use each** (2 marks)

**Sample Answer:**

**Qualitative Analysis** uses categorical assignments (Low, Medium, High) based on judgment and experience. It's subjective but consistent, faster to perform, and good for non-tangible impacts like reputation.

**Quantitative Analysis** uses numerical values based on statistical probabilities and monetary amounts. It's objective if data is accurate, more precise, but requires good data and is time-consuming.

**Comparison:**
- Speed: Qualitative faster; Quantitative slower
- Precision: Qualitative approximate; Quantitative exact
- Data requirements: Qualitative minimal; Quantitative substantial
- Cost justification: Qualitative difficult; Quantitative easy

**When to Use:**

**Qualitative:**
- Initial risk assessments to quickly identify major risks
- When considering non-tangible aspects (reputation, morale)
- When data is insufficient for quantitative analysis
- For relative risk ranking and prioritization

**Quantitative:**
- When justifying security investments to executives (ROI calculations)
- When accurate cost-benefit analysis is needed
- When precise risk values are required for insurance or compliance
- When historical data is available and reliable

**Best Practice:** Use qualitative for initial assessment and high-level prioritization, then perform quantitative analysis for high-priority risks requiring investment decisions.

---

### Question 5: What is a Risk Register and what information should it contain? (5 marks)

**Answer Technique:**
1. **Define purpose** (1 mark)
2. **List key components** (3 marks)
3. **Explain usage** (1 mark)

**Sample Answer:**

**Risk Register** is a centralized document that maintains the organization's overall risk profile, tracking all identified risks and their treatment status.

**Essential Information:**

1. **Risk Summary:**
   - Threat type and associated event/actor
   - Affected assets and potential impact
   - Risk description

2. **Category and Classification:**
   - Risk type (operational, technical, compliance, strategic)
   - Severity level (Critical, High, Medium, Low)
   - Current status (Open, Closed, Accepted, In Progress)

3. **Risk Owner:**
   - Person accountable for managing the risk
   - Authority to make treatment decisions
   - Contact information

4. **Risk Treatment:**
   - Treatment option selected (Accept, Avoid, Mitigate, Transfer)
   - Controls implemented or planned
   - Residual risk level after treatment
   - Timeline and milestones

**Usage:** The risk register provides management with comprehensive view of organizational risk posture, enables tracking of risk treatment progress, supports informed decision-making, and demonstrates due diligence for compliance and audit purposes. It should be reviewed regularly (at minimum quarterly) and updated whenever risks change.

---

## 💡 Study Tips

1. **Master risk terminology** - Know definitions cold (Risk, Threat, Vulnerability, Impact, Likelihood)
2. **Memorize NIST RMF 7 steps** - Use acronym: "Please Come Select Important And Authorize Monitoring"
3. **Practice ALE calculations** - Be comfortable with SLE and ALE formulas
4. **Understand risk treatment options** - Accept, Avoid, Mitigate, Transfer—know when to use each
5. **Know internal vs external threats** - Different controls for different threat types
6. **Understand APTs** - Characteristics and typical lifecycle
7. **Know vulnerability sources** - CVE, NVD, OWASP, etc.
8. **Practice risk scenarios** - Given scenario, can you identify threat, vulnerability, risk, and appropriate control?

---

## 🔑 Key Takeaways

1. **Risk = Likelihood × Impact** - Both factors must be considered
2. **Risk management is continuous** - Not one-time assessment
3. **Four risk treatment options** - Accept, Avoid, Mitigate, Transfer
4. **Internal threats have insider advantage** - Require different controls than external threats
5. **APTs are sophisticated and persistent** - Require advanced detection and response
6. **NIST RMF provides structure** - 7-step cyclical framework
7. **Qualitative vs. Quantitative** - Use qualitative for speed, quantitative for precision
8. **Security baselines establish minimum** - Standardize security requirements
9. **Risk register centralizes tracking** - Essential for governance and compliance
10. **Impact matters only if it affects objectives** - Context is critical

---

## 📚 References

- NIST SP 800-30: Guide for Conducting Risk Assessments
- NIST SP 800-37: Risk Management Framework
- NIST SP 800-53: Security and Privacy Controls
- ISO/IEC 27005: Information Security Risk Management
- ISACA CISM Review Manual - Domain 2

---

**End of Lecture 7 Notes**

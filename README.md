# Awesome DevSecOps [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome DevSecOps tools, practices, and resources for integrating security into the software development lifecycle

DevSecOps is the philosophy of integrating security practices within the DevOps process. This list covers tools, frameworks, and best practices for building security into every stage of the software development lifecycle.

## Contents

- [Learning & Getting Started](#learning--getting-started)
  - [Books & Guides](#books--guides)
  - [Training & Certification](#training--certification)
  - [Frameworks & Standards](#frameworks--standards)
- [Code Security](#code-security)
  - [Static Application Security Testing (SAST)](#static-application-security-testing-sast)
  - [Software Composition Analysis (SCA)](#software-composition-analysis-sca)
  - [Secrets Detection](#secrets-detection)
- [Security Testing](#security-testing)
  - [Dynamic Application Security Testing (DAST)](#dynamic-application-security-testing-dast)
  - [API Security Testing](#api-security-testing)
  - [Fuzzing](#fuzzing)
- [Container & Kubernetes Security](#container--kubernetes-security)
  - [Container Scanning](#container-scanning)
  - [Kubernetes Security Tools](#kubernetes-security-tools)
  - [Runtime Security](#runtime-security)
- [Infrastructure Security](#infrastructure-security)
  - [Infrastructure as Code (IaC) Security](#infrastructure-as-code-iac-security)
  - [Cloud Security Posture Management](#cloud-security-posture-management)
  - [Network Security](#network-security)
- [Secrets Management](#secrets-management)
- [CI/CD Security](#cicd-security)
- [Security Monitoring & Incident Response](#security-monitoring--incident-response)
- [Compliance & Policy](#compliance--policy)
- [Security Automation](#security-automation)
- [Threat Modeling](#threat-modeling)
- [Vulnerability Management](#vulnerability-management)
- [Security Champions Programs](#security-champions-programs)
- [Open Source Security](#open-source-security)
- [Cloud Security](#cloud-security)
- [Platforms & Solutions](#platforms--solutions)
- [Community & Resources](#community--resources)
- [Related Lists](#related-lists)
- [Contributing](#contributing)

## Learning & Getting Started

### Books & Guides

- [DevSecOps Handbook](https://www.devsecops.org/) - Comprehensive guide to DevSecOps
- [The Phoenix Project](https://itrevolution.com/the-phoenix-project/) - Novel about IT, DevOps, and helping your business win
- [Accelerate](https://itrevolution.com/accelerate-book/) - Building and scaling high-performing technology organizations
- [OWASP DevSecOps Guideline](https://owasp.org/www-project-devsecops-guideline/) - Official OWASP guide
- [Alice and Bob Learn Application Security](https://www.wiley.com/en-us/Alice+and+Bob+Learn+Application+Security-p-9781119687405) - Beginner-friendly security book

### Training & Certification

- [Certified DevSecOps Professional (CDP)](https://www.practical-devsecops.com/certified-devsecops-professional/) - Professional certification
- [SANS DevSecOps Courses](https://www.sans.org/cyber-security-courses/?focus-area=application-security&training-format=) - Professional training
- [Linux Foundation DevSecOps](https://training.linuxfoundation.org/training/secure-software-development-fundamentals/) - Secure development fundamentals
- [Cloud Security Alliance CCSK](https://cloudsecurityalliance.org/education/ccsk/) - Cloud security certification
- [ISC2 CSSLP](https://www.isc2.org/Certifications/CSSLP) - Certified Secure Software Lifecycle Professional

### Frameworks & Standards

- [NIST Secure Software Development Framework (SSDF)](https://csrc.nist.gov/publications/detail/sp/800-218/final) - Secure SDLC framework
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) - Top web application security risks
- [OWASP SAMM](https://owaspsamm.org/) - Software Assurance Maturity Model
- [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks/) - Security configuration benchmarks
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) - Framework for improving critical infrastructure cybersecurity
- [ISO 27001](https://www.iso.org/isoiec-27001-information-security.html) - Information security management

## Code Security

### Static Application Security Testing (SAST)

**Commercial:**

- [Snyk Code](https://snyk.io/product/snyk-code/) - Developer-first SAST
  - Real-time scanning in IDE
  - AI-powered fix suggestions
  - Low false positives
  - Multiple language support

- [SonarQube](https://www.sonarqube.org/) - Code quality and security
  - Supports 29+ languages
  - Quality gates
  - Security hotspots
  - CI/CD integration

- [Checkmarx](https://checkmarx.com/) - Enterprise SAST
  - Comprehensive coverage
  - IDE plugins
  - Remediation guidance

- [Veracode](https://www.veracode.com/) - Application security platform
  - Static analysis
  - Dynamic analysis
  - SCA and penetration testing

**Open Source:**

- [Semgrep](https://semgrep.dev/) - Fast, customizable static analysis
  - Open source core
  - Custom rule creation
  - CI/CD friendly
  - 30+ languages

- [Bandit](https://github.com/PyCQA/bandit) - Python security linter
  - Finds common security issues
  - Configurable
  - CI integration

- [Brakeman](https://brakemanscanner.org/) - Ruby on Rails security scanner
  - Static analysis for Rails
  - Fast scanning
  - Low false positives

- [SpotBugs](https://spotbugs.github.io/) - Java static analysis
  - Find bugs in Java code
  - Security plugin available
  - Maven/Gradle integration

### Software Composition Analysis (SCA)

- [Snyk Open Source](https://snyk.io/product/open-source-security-management/) - Dependency scanning
  - Automated fix PRs
  - License compliance
  - Real-time monitoring

- [Dependabot](https://github.com/dependabot) - GitHub's dependency updater
  - Automated security updates
  - Free for public repos
  - Multi-ecosystem support

- [OWASP Dependency-Check](https://owasp.org/www-project-dependency-check/) - SCA tool
  - Free and open source
  - Identifies known vulnerabilities
  - Multiple language support

- [WhiteSource (Mend)](https://www.mend.io/) - Open source security
  - License compliance
  - Vulnerability detection
  - Policy enforcement

- [Trivy](https://github.com/aquasecurity/trivy) - Comprehensive scanner
  - Vulnerabilities in dependencies
  - Container images
  - IaC misconfigurations

### Secrets Detection

- [GitGuardian](https://www.gitguardian.com/) - Secrets detection
  - Real-time scanning
  - GitHub/GitLab integration
  - Secret remediation

- [TruffleHog](https://github.com/trufflesecurity/trufflehog) - Find secrets in git repos
  - High entropy string detection
  - Git history scanning
  - Pre-commit hooks

- [Gitleaks](https://github.com/gitleaks/gitleaks) - SAST for secrets
  - Fast scanning
  - Custom rules
  - CI/CD integration

- [detect-secrets](https://github.com/Yelp/detect-secrets) - Prevent secrets in code
- [KeyDrift](https://keydrift.dev) - Scans deployed HTML and JavaScript for exposed secrets while recognizing public browser credentials that should not be treated as leaks.
  - Baseline secrets
  - Pre-commit hooks
  - Low false positives

## Security Testing

### Dynamic Application Security Testing (DAST)

- [OWASP ZAP](https://www.zaproxy.org/) - Web app security scanner
  - Free and open source
  - Automated scanning
  - Manual testing tools
  - CI/CD integration

- [Burp Suite](https://portswigger.net/burp) - Web security testing
  - Industry standard
  - Manual and automated testing
  - Extensible with plugins
  - Free community edition

- [Nuclei](https://github.com/projectdiscovery/nuclei) - Vulnerability scanner
  - Template-based scanning
  - Fast and customizable
  - CI/CD friendly
  - 3000+ templates

- [Acunetix](https://www.acunetix.com/) - Web vulnerability scanner
  - Comprehensive scanning
  - Low false positives
  - Issue management

### API Security Testing

- [OWASP API Security Top 10](https://owasp.org/www-project-api-security/) - API security risks
- [Postman](https://www.postman.com/api-platform/api-security/) - API testing with security features
- [RestAssured](https://rest-assured.io/) - REST API testing
- [SoapUI](https://www.soapui.org/) - API testing tool
- [Burp Suite](https://portswigger.net/burp/documentation/desktop/testing-workflow/working-with-apis) - API security testing

### Fuzzing

- [AFL++](https://github.com/AFLplusplus/AFLplusplus) - American Fuzzy Lop
  - Coverage-guided fuzzing
  - Fast and effective
  - Multiple platforms

- [LibFuzzer](https://llvm.org/docs/LibFuzzer.html) - In-process fuzzing
  - Part of LLVM
  - Coverage-guided
  - Easy integration

- [OSS-Fuzz](https://google.github.io/oss-fuzz/) - Continuous fuzzing for OSS
  - Google's fuzzing service
  - Free for open source
  - Automated bug reporting

## Container & Kubernetes Security

### Container Scanning

- [Trivy](https://github.com/aquasecurity/trivy) - Comprehensive scanner
  - OS packages
  - Application dependencies
  - IaC misconfigurations
  - Fast and accurate

- [Clair](https://github.com/quay/clair) - Container vulnerability scanner
  - Static analysis
  - Continuous monitoring
  - API-driven

- [Anchore Grype](https://github.com/anchore/grype) - Vulnerability scanner
  - Fast scanning
  - Multiple distros
  - SBOM support

- [Docker Scout](https://docs.docker.com/scout/) - Docker's security tool
  - Image analysis
  - Remediation advice
  - Policy evaluation

- [Snyk Container](https://snyk.io/product/container-vulnerability-management/) - Container security
  - Base image recommendations
  - Kubernetes integration
  - Fix guidance

### Kubernetes Security Tools

- [Falco](https://falco.org/) - Cloud-native runtime security
  - Runtime threat detection
  - CNCF project
  - Custom rules
  - eBPF-based

- [Kube-bench](https://github.com/aquasecurity/kube-bench) - CIS benchmark checker
  - Checks K8s security
  - Based on CIS standards
  - Easy to run

- [Kube-hunter](https://github.com/aquasecurity/kube-hunter) - Kubernetes penetration testing
  - Hunt for security weaknesses
  - Active and passive modes
  - Reports findings

- [Kubescape](https://github.com/kubescape/kubescape) - K8s security platform
  - Risk analysis
  - Compliance scanning
  - RBAC visualizer
  - CNCF project

- [Polaris](https://github.com/FairwindsOps/polaris) - Kubernetes best practices
  - Configuration validation
  - Admission controller
  - Dashboard

### Runtime Security

- [Falco](https://falco.org/) - Runtime security
- [Sysdig Secure](https://sysdig.com/products/secure/) - Container and Kubernetes security
- [Aqua Security](https://www.aquasec.com/) - Full lifecycle container security
- [Tracee](https://github.com/aquasecurity/tracee) - Runtime security and forensics

## Infrastructure Security

### Infrastructure as Code (IaC) Security

- [Checkov](https://www.checkov.io/) - IaC static analysis
  - Terraform, CloudFormation, K8s
  - 1000+ policies
  - CI/CD integration
  - Open source

- [Terrascan](https://github.com/tenable/terrascan) - IaC security scanner
  - 500+ policies
  - Multiple IaC tools
  - Pre-commit hooks

- [tfsec](https://github.com/aquasecurity/tfsec) - Terraform security scanner
  - Fast scanning
  - Custom checks
  - CI/CD friendly

- [KICS](https://github.com/Checkmarx/kics) - IaC security scanner
  - Keeps Infrastructure as Code Secure
  - Multiple platforms
  - Custom queries

- [Snyk IaC](https://snyk.io/product/infrastructure-as-code-security/) - IaC security
  - Fix guidance
  - Multiple frameworks
  - Developer-friendly

### Cloud Security Posture Management

- [Prowler](https://github.com/prowler-cloud/prowler) - AWS/Azure/GCP security tool
  - CIS benchmarks
  - 350+ checks
  - Open source

- [CloudSploit](https://github.com/aquasecurity/cloudsploit) - Cloud security scanner
  - AWS, Azure, GCP, Oracle
  - 600+ plugins
  - Free and open source

- [ScoutSuite](https://github.com/nccgroup/ScoutSuite) - Multi-cloud security auditing
  - AWS, Azure, GCP, Alibaba, Oracle
  - HTML reports
  - Open source

- [CloudCustodian](https://cloudcustodian.io/) - Cloud governance
  - Policy as code
  - Multi-cloud
  - Automated remediation

### Network Security

- [Cilium](https://cilium.io/) - eBPF-based networking and security
- [Calico](https://www.tigera.io/project-calico/) - Container networking and security
- [Istio](https://istio.io/) - Service mesh with security features
- [Open Policy Agent (OPA)](https://www.openpolicyagent.org/) - Policy engine

## Secrets Management

- [HashiCorp Vault](https://www.vaultproject.io/) - Secrets management
  - Dynamic secrets
  - Encryption as a service
  - PKI and TLS certificates
  - Multi-cloud support

- [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) - AWS secrets service
  - Automatic rotation
  - Fine-grained permissions
  - Integration with AWS services

- [Azure Key Vault](https://azure.microsoft.com/en-us/products/key-vault) - Azure secrets management
  - Keys, secrets, certificates
  - HSM support
  - Managed identities

- [Google Secret Manager](https://cloud.google.com/secret-manager) - GCP secrets service
  - Encrypted storage
  - Versioning
  - IAM integration

- [Doppler](https://www.doppler.com/) - Secrets management platform
  - Developer-friendly
  - Multi-environment
  - Integrations

- [Sealed Secrets](https://github.com/bitnami-labs/sealed-secrets) - Kubernetes secrets
  - Encrypted K8s secrets
  - GitOps-friendly
  - Open source

## CI/CD Security

- [GitHub Advanced Security](https://github.com/features/security) - GitHub security features
  - Code scanning
  - Secret scanning
  - Dependency review

- [GitLab Security](https://about.gitlab.com/solutions/dev-sec-ops/) - Built-in security scanning
  - SAST, DAST, SCA
  - Container scanning
  - License compliance

- [Jenkins Security Plugins](https://plugins.jenkins.io/security/) - Security plugins
- [CircleCI Security](https://circleci.com/docs/security-overview/) - CI/CD security
- [Azure DevOps Security](https://learn.microsoft.com/en-us/azure/devops/organizations/security/) - ADO security

**Best Practices:**
- Principle of least privilege
- Secure credential storage
- Pipeline security scanning
- Audit logging
- Infrastructure as Code
- Immutable pipelines

## Security Monitoring & Incident Response

- [Wazuh](https://wazuh.com/) - Security monitoring platform
  - Log analysis
  - Intrusion detection
  - Compliance monitoring
  - Open source

- [OSSEC](https://www.ossec.net/) - Host-based intrusion detection
  - Log analysis
  - File integrity checking
  - Rootkit detection

- [Elastic Security](https://www.elastic.co/security) - SIEM solution
  - Threat detection
  - Investigation
  - Response

- [TheHive](https://thehive-project.org/) - Security incident response platform
  - Case management
  - Observable enrichment
  - Task automation

- [Cortex](https://github.com/TheHive-Project/Cortex) - Observable analysis engine
  - Automated analysis
  - Threat intelligence
  - Integration with TheHive

## Compliance & Policy

- [Open Policy Agent (OPA)](https://www.openpolicyagent.org/) - Policy engine
  - Policy as code
  - Unified framework
  - Cloud-native

- [Gatekeeper](https://github.com/open-policy-agent/gatekeeper) - OPA for Kubernetes
  - Admission controller
  - Policy enforcement
  - Custom policies

- [Kyverno](https://kyverno.io/) - Kubernetes-native policy management
  - No new language
  - Validation, mutation, generation
  - Easy to use

- [Allstar](https://github.com/ossf/allstar) - GitHub security policy enforcement
  - Automated enforcement
  - Configurable policies
  - Organization-wide

## Security Automation

- [Security Automation Platform (SOAR)](https://www.gartner.com/en/information-technology/glossary/security-orchestration-automation-response-soar) - Automation frameworks
- [Ansible Security Automation](https://www.ansible.com/use-cases/security-automation) - Security playbooks
- [DefectDojo](https://github.com/DefectDojo/django-DefectDojo) - Security orchestration
  - Vulnerability management
  - Tool integration
  - Workflow automation

## Threat Modeling

- [OWASP Threat Dragon](https://owasp.org/www-project-threat-dragon/) - Threat modeling tool
  - Free and open source
  - Desktop and web
  - Diagrams and reports

- [Microsoft Threat Modeling Tool](https://www.microsoft.com/en-us/securityengineering/sdl/threatmodeling) - Microsoft's tool
  - STRIDE methodology
  - Windows application
  - Template-based

- [IriusRisk](https://www.iriusrisk.com/) - Threat modeling platform
  - Automated threat modeling
  - Integration with tools
  - Collaboration features

- [Threatspec](https://threatspec.org/) - Threat modeling as code
  - Code-centric
  - Version controlled
  - Developer-friendly

## Vulnerability Management

- [DefectDojo](https://github.com/DefectDojo/django-DefectDojo) - Vulnerability management
- [Faraday](https://github.com/infobyte/faraday) - Collaborative penetration test platform
- [ArcherySec](https://github.com/archerysec/archerysec) - Vulnerability assessment and management
- [OpenVAS](https://www.openvas.org/) - Vulnerability scanner

## Security Champions Programs

- [OWASP Security Champions Guide](https://owasp.org/www-project-security-champions-guidebook/) - Building security champions
- [Security Champions Playbook](https://github.com/c0rdis/security-champions-playbook) - Open source playbook

## Open Source Security

- [OpenSSF](https://openssf.org/) - Open Source Security Foundation
  - Best practices
  - Scorecards
  - Security tooling

- [OpenSSF Scorecard](https://github.com/ossf/scorecard) - Security health metrics
  - Automated checks
  - Risk assessment
  - Open source projects

- [SBOM Tools](https://github.com/microsoft/sbom-tool) - Software Bill of Materials
  - Dependency tracking
  - Supply chain security
  - Compliance

- [Sigstore](https://www.sigstore.dev/) - Software signing
  - Keyless signing
  - Transparency log
  - Open source

## Cloud Security

### AWS Security

- [AWS Security Hub](https://aws.amazon.com/security-hub/) - Centralized security
- [AWS GuardDuty](https://aws.amazon.com/guardduty/) - Threat detection
- [AWS Inspector](https://aws.amazon.com/inspector/) - Vulnerability management
- [CloudTrail](https://aws.amazon.com/cloudtrail/) - Audit logging

### Azure Security

- [Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud/) - Cloud security posture
- [Azure Sentinel](https://azure.microsoft.com/en-us/products/microsoft-sentinel/) - SIEM and SOAR
- [Azure Policy](https://azure.microsoft.com/en-us/products/azure-policy/) - Governance

### GCP Security

- [Security Command Center](https://cloud.google.com/security-command-center) - Security management
- [Cloud Security Scanner](https://cloud.google.com/security-scanner) - Web vulnerability scanner
- [Binary Authorization](https://cloud.google.com/binary-authorization) - Deploy-time security

## Platforms & Solutions

- [Snyk](https://snyk.io/) - Developer security platform
- [Aqua Security](https://www.aquasec.com/) - Cloud-native security
- [Sysdig](https://sysdig.com/) - Cloud and container security
- [Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud) - CNAPP platform
- [Lacework](https://www.lacework.com/) - Cloud security platform

## Community & Resources

### Blogs & News

- [OWASP Blog](https://owasp.org/blog/) - Security news
- [The DevSecOps Blog](https://www.devsecops.org/blog) - DevSecOps insights
- [Snyk Blog](https://snyk.io/blog/) - Developer security
- [Aqua Security Blog](https://blog.aquasec.com/) - Cloud-native security

### Podcasts

- [Absolute AppSec](https://absoluteappsec.com/) - Application security
- [Application Security Weekly](https://securityweekly.com/category-shows/application-security-weekly/) - AppSec news
- [Darknet Diaries](https://darknetdiaries.com/) - True security stories

### Communities

- [DevSecOps Slack](https://devsecops.org/) - Community chat
- [OWASP Slack](https://owasp.org/slack/invite) - OWASP community
- [r/netsec](https://www.reddit.com/r/netsec/) - Network security
- [r/devops](https://www.reddit.com/r/devops/) - DevOps community

### Conferences

- [DevSecCon](https://www.devseccon.com/) - DevSecOps conference
- [RSA Conference](https://www.rsaconference.com/) - Security conference
- [Black Hat](https://www.blackhat.com/) - InfoSec event
- [OWASP Global AppSec](https://owasp.org/events/) - Application security

## Related Lists

- [awesome-security](https://github.com/sbilly/awesome-security) - Security resources
- [awesome-application-security](https://github.com/paragonie/awesome-appsec) - Application security
- [awesome-kubernetes-security](https://github.com/magnologan/awesome-k8s-security) - Kubernetes security
- [awesome-cloud-security](https://github.com/Funkmyster/awesome-cloud-security) - Cloud security
- [awesome-threat-intelligence](https://github.com/hslatman/awesome-threat-intelligence) - Threat intelligence

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

**What to contribute:**
- DevSecOps tools and platforms
- Security best practices
- Training resources
- Case studies and examples
- Automation scripts and templates

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Tyson Cung](https://github.com/tysoncung) has waived all copyright and related or neighboring rights to this work.

---

**Star ⭐ this repo to stay updated with the latest DevSecOps tools and practices!**

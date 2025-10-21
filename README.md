# MDM/R Documentation Project

Comprehensive technical documentation and implementation guides for Ontario's Meter Data Management and Repository (MDM/R) system.

## 📋 Overview

This repository contains technical specifications, implementation guides, and reference documentation for the MDM/R system operated by the Independent Electricity System Operator (IESO) in Ontario, Canada. The MDM/R processes smart meter data from Local Distribution Companies (LDCs) to produce billing quantity data for Ontario's electricity market.

## 🎯 Purpose

This documentation project provides:

- **Technical Specifications**: Detailed format specifications for MDM/R reports and data exchanges
- **Implementation Guides**: Step-by-step procedures for meter installations, synchronization, and data corrections
- **Reference Materials**: Quick reference guides for key parameters and operational procedures
- **Best Practices**: Common mistakes to avoid and validation checklists

## 📚 Documentation Structure

### Technical Specifications

- **Report Specifications**
  - `IR01` - Universal SDP ID Assignment Request Summary Exception Report
  - `IR06` - Synchronization Updates Report
  - `IR08` - Billing Request Detailed Exception Report
  - `IR17` - FTS Processing Failure Report

### Implementation Guides

- **Synchronization Guides**
  - High Priority Parameters Guide
  - Meter Installation Guide (Scenario A: New SDP + New Meter)
  - Synchronization Process Overview

- **Operational Procedures**
  - Crossed Meter Data Correction Procedure (SME_PRO_0009)
  - Data Removal Request Procedures
  - Meter Relationship Management

### Interactive Documentation

The project includes HTML-based interactive guides with:
- Navigation hubs for easy access
- Detailed parameter references
- Step-by-step implementation workflows
- Validation checklists
- Common error resolution guides

## 🔑 Key Concepts

### Service Delivery Point (SDP)
The point at which electricity delivery is metered or calculated. Each SDP is uniquely identified within the MDM/R system.

### Synchronization
The process of maintaining data consistency between LDC systems and the MDM/R, including meter installations, parameter updates, and relationship management.

### VEE (Validation, Estimation, and Editing)
Data quality processes applied to meter reads before generating billing quantities.

### File Transfer Services (FTS)
The AS2-based file exchange mechanism between LDCs and the MDM/R system.

## 🛠️ For LDCs and Implementation Teams

### Getting Started

1. **Review Technical Specifications**: Start with the synchronization technical interface specification (SME-SPEC-40) for system integration requirements
2. **Follow Implementation Guides**: Use scenario-specific guides for meter installations and updates
3. **Reference Quick Guides**: Utilize parameter quick reference guides during implementation
4. **Validate Your Work**: Use provided checklists to ensure data quality

### File Naming Conventions

MDM/R uses structured file naming conventions:
```
[PREFIX]_[ORG_ID]_[FILE_TYPE]_[YYYYMMDD]_[HHMMSS]_[SEQUENCE].[EXT]
```

### Report Delivery

Reports are delivered via FTS (File Transfer Services) using AS2 protocol. Delivery timelines and formats are specified in each report's technical specification.

## 📖 Document Relationships

```
MDM/R System
├── Synchronization Process
│   ├── Request Files (from LDCs)
│   ├── Processing (MDM/R)
│   └── Reports (IR06, exceptions)
├── Billing Process
│   ├── Billing Requests
│   ├── VEE Processing
│   └── Billing Reports (IR08)
└── Administrative Functions
    ├── SDP ID Assignment (IR01)
    └── FTS Processing (IR17)
```

## 🔍 Common Use Cases

### New Meter Installation
1. Create SDP in MDM/R
2. Establish meter-to-SDP relationship
3. Configure parameters (rate class, multipliers, framing)
4. Submit synchronization file set
5. Validate using IR06 report

### Crossed Meter Correction
1. End incorrect SDP-meter relationships
2. Request meter read data removal
3. Establish correct relationships
4. Load corrected meter data

### Parameter Updates
Critical parameters requiring synchronization:
- VEE Service configuration
- CT/PT Multipliers
- Distributor Rate Class (DRC)
- Commodity Rate Class (CRR)
- Framing Structure

## 📅 Key Information

- **Time Zone**: All MDM/R timestamps are in EST (Eastern Standard Time)
- **Daily Read Period**: 24-hour period starting at midnight EST
- **Report Formats**: CSV and structured text formats
- **Character Encoding**: UTF-8

## 🏢 IESO Contact Information

**Independent Electricity System Operator**
- Address: 1600-120 Adelaide Street West, Toronto, Ontario M5H 1T1
- Phone: 905.403.6900
- Toll-free: 1.888.448.7777
- Email: customer.relations@ieso.ca
- Website: ieso.ca

## ⚠️ Important Notes

- This documentation is confidential and intended for authorized MDM/R participants only
- All specifications are subject to change; refer to the latest version numbers
- Compliance with data formats and procedures is mandatory for system integration
- For technical support, contact the MDM/R Administrator

## 📝 Document Versions

Technical specifications in this repository reference specific version numbers and issue dates. Always ensure you are working with the latest approved versions.

## 🔒 Compliance & Standards

- AS2 protocol for file transfers
- Ontario Energy Board regulations
- IESO market rules and procedures
- Smart meter data privacy requirements

## 📧 Support

For questions about MDM/R technical specifications or implementation:
1. Review the relevant technical specification document
2. Check the quick reference guides
3. Contact your LDC MDM/R coordinator
4. Escalate to IESO customer relations if needed

---

**Note**: This is a living documentation project. Procedures and specifications are updated periodically to reflect system enhancements and market rule changes.

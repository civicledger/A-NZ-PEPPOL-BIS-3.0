# AUNZ-Validation artefacts

This repository contains the validation artefacts for the Australian - New Zealand electronic invoice specification.

The AUNZ Validation Artefacts are based on two validation artefacts:
* European Norm validation artefacts v1.2.3 https://github.com/ConnectingEurope/eInvoicing-EN16931/releases/tag/validation-1.2.3 
* PEPPOL electronic invoice Spring Release https://github.com/OpenPEPPOL/peppol-bis-invoice-3/releases/tag/3.0.4

# Release Notes
    
* Correction of the profile identifier in AUNZ-PEPPOL-SB-validation

# Latest release

* Release 1.0.2 (January 2020)
 
There are three validation artefacts that should be applied to validate an AUNZ electronic invoice instance:

* AUNZ-UBL-validation.sch adapts the EN16931 business rules to the Australian - New Zealand requirements. It should be applied to any invoice, credit note or selfbilled invoice.
 
* AUNZ-PEPPOL-validation.sch derived from the OpenPEPPOL business rules and adapted to AUNZ. It shall be applied to invoices and credit notes.
* AUNZ-PEPPOL-SB-validation.sch derived from the OpenPEPPOL business rules adapted to AUNZ. It shall be applied the selfbilling invoices and selfbilling credit notes.


To validate the syntax, the UBL 2.1 schema shall be used:
* `ubl` - UBL 2.1 (ISO/IEC 19845:2015) 
  * UBL Website: https://www.oasis-open.org/committees/ubl/

   
# Validation process

In order to validate a document instance, the following process should be used:

* Use the UBL Invoice.xsd or the UBL CreditNote.xsd version 2.1 for schema validation depending on the document type
* Validate the syntax boundaries and the derived EN16931 business rules using the AUNZ-UBL-validation.sch
* Validate PEPPOL rules and specific AUNZ business rules using the AUNZ-PEPPOL-validation.sch or AUNZ-PEPPOL-SB-validation.sch depending on the type of instance

This repository contains an xslt folder with the xslt artefacts compiled from the schematron validation artefacts. Any of them can be used for validation of an AUNZ electronic invoice.

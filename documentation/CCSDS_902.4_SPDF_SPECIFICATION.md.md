\# CCSDS 902.4-B-1 & CSS-SM Service Package Data Formats (SPDF) Specification

\#\# Executive Summary  
This document provides the technical architecture and specification for \*\*SPDFForge Pro\*\*, an industrial workstation implementation of the \*\*Consultative Committee for Space Data Systems (CCSDS) 902.4-B-1\*\* Recommended Standard (\*Cross Support Service Management—Service Package Data Formats\*, Blue Book, Issue 1, September 2026 / Red Book) and \*\*ISO Cross Support Service Management (CSS-SM)\*\*.

The Service Package Data Formats (SPDF) define the detailed RF, modulation, coding, baseband, and radiometric parameters required by a ground station (NASA Deep Space Network DSN, ESA ESTRACK, KSAT, commercial apertures) to execute a scheduled tracking pass. It formalizes both the \*\*Type 1 (Compact Profile Reference)\*\* and \*\*Type 2 (Fully Explicit Configuration)\*\* exchange formats.

\#\# 1\. Information Architecture & Structural Models  
Type 1 exchanges reference pre-configured, agreed-upon baseline profiles: reduces message size to \< 2 KB, accommodates ad-hoc overrides.  
Type 2 contains explicit space link parameters: Forward Space Link (Uplink RF carrier, power, modulation, symbol rate), Return Space Link (Downlink RF carrier, polarization, bit rate, coding), Radiometric Tracking (coherent turnaround ratio, Doppler, ranging), and Delta-DOR scan patterns.

\#\# 2\. Coherent Frequency Turnaround Ratios  
Enforces standard coherent transponder phase-lock ratios per CCSDS 401.0-B:  
\- S-Band Uplink \-\> S-Band Downlink: 240 / 221  
\- X-Band Uplink \-\> X-Band Downlink: 880 / 749  
\- X-Band Uplink \-\> Ka-Band Downlink: 3344 / 749  
\- Ka-Band Uplink \-\> Ka-Band Downlink: 3360 / 3599

\#\# 3\. Bilateral XML and KVN Formatting  
\- XML Schema: Conforms to SANA CSS-SM XML Schema (\`urn:ccsds:schema:csssm:spdf\`).  
\- KVN Format: Clean Key-Value Notation for legacy tracking station decoders.  

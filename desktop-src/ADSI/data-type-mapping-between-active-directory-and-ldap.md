---
title: Datentyp Zuordnung zwischen Active Directory und LDAP
description: In der folgenden Tabelle wird der benutzerfreundliche Syntax Name der entsprechenden LDAP-Syntax OID und dem adstypeer-Wert zugeordnet.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- Datentyp Zuordnung zwischen Active Directory und LDAP ADSI
- LDAP-Dienstanbieter ADSI, Datentyp Zuordnung zwischen Active Directory und LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340194"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Datentyp Zuordnung zwischen Active Directory und LDAP

In der folgenden Tabelle wird der benutzerfreundliche Syntax Name der entsprechenden LDAP-Syntax OID und dem [**adstypeer**](/windows/win32/api/iads/ne-iads-adstypeenum) -Wert zugeordnet.



| Anzeige Syntax Name              | LDAP-Syntax OID               | Adstypum-Datentyp                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| Access spointdn                     | 1.3.6.1.4.1.1466.115.121.1.2  | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Attributetypedescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Bitstring                         | 1.3.6.1.4.1.1466.115.121.1.6  | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **boolescher Wert von adstype \_**                  |
| Caseexactstring                   | 1.2.840.113556.1.4.1362       | **exakte Groß-/Kleinschreibung von adstype \_ \_ \_**      |
| Caseignorestring                  | 1.2.840.113556.1.4.1221       | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Zertifikat                       | 1.3.6.1.4.1.1466.115.121.1.8  | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Certificatepair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Land/Region                    | 1.3.6.1.4.1.1466.115.121.1.11 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Dataqualitysyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Directoriystring                   | 1.3.6.1.4.1.1466.115.121.1.15 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **adstype- \_ DN- \_ Zeichenfolge**               |
| Dsaqualitysyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Enhancedguide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| "FacsimileTelephoneNumber"          | 1.3.6.1.4.1.1466.115.121.1.22 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Generalizedtime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **adstype- \_ UTC- \_ Zeit**                |
| Zeit (nur der Standort Server übernimmt dies) | 1.3.6.1.4.1.1466.115.121.1.24 | **adstype- \_ UTC- \_ Zeit**                |
| Handbuch                             | 1.3.6.1.4.1.1466.115.121.1.25 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **adstype- \_ Ganzzahl**                  |
| INTEGER8 (nicht in LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **\_hohe Ganzzahl von adstype \_**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Mail Preference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Nameandoptionaluid                | 1.3.6.1.4.1.1466.115.121.1.34 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **\_numerische \_ Zeichenfolge von adstype**          |
| Objectclassdescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Octetstring (nicht in RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Orname                            | 1.2.840.113556.1.4.1221       | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Othermailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Presentationaddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **Druckbare adstype- \_ \_ Zeichenfolge**        |
| Objectsecuritydescriptor          | 1.2.840.113556.1.4.907        | **adstype \_ NT- \_ Sicherheits \_ Beschreibung** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| Teletexterminalidentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **Zeichenfolge des adstype- \_ Oktetts \_**            |
| Telexnumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **adstype \_ Case \_ - \_ Zeichenfolge ignorieren**     |
| UtcTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **adstype- \_ UTC- \_ Zeit**                |



 

 

 





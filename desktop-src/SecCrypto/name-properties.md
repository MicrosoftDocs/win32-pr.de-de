---
description: Namenseigenschaften sind Eigenschaften von Zertifikaten und Zertifikatanforderungen, die Daten über den Antragsteller darstellen, d. h. den Besitzer des Zertifikats oder die Person, für die ein Zertifikat angefordert wird.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Namenseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28765f0c278678ed5bdca9ef8547c1c6dc85ca7b6b343b229441b4b777eac688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425310"
---
# <a name="name-properties"></a>Namenseigenschaften

Namenseigenschaften sind Eigenschaften von Zertifikaten und Zertifikatanforderungen, die Daten über den Antragsteller darstellen, d. h. den Besitzer des Zertifikats oder die Person, für die ein Zertifikat angefordert wird. Jede Name-Eigenschaft wird durch einen Eigenschaftennamen identifiziert. Diese Namen sind nicht lokalisierbar. Die Namenseigenschaften entsprechen jedoch in der Regel einer Datenbankspalte der Zertifikatdienste, und Sie können das MMC-Snap-In der Zertifizierungsstelle, das Befehlszeilentool "certutil -schema" oder die [**IEnumCERTVIEWCOLUMN::GetDisplayName-Methode**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) verwenden, um lokalisierte Versionen der Datenbankspaltennamen anzuzeigen.

Der Eigenschaftenname (aber nicht die Aliase) kann "Subject" aufweisen. als optionales Präfix. Um beispielsweise auf den allgemeinen Namen des Antragstellers zu verweisen, können Sie entweder "CommonName" oder "Subject.CommonName" verwenden.

Zusätzlich zu ihrem Namen verfügt jede Eigenschaft über eine Reihe von Aliasen, die von Den Zertifikatdiensten als alternative Namen für die Eigenschaft erkannt werden. Beachten Sie, dass [*Objektbezeichner*](../secgloss/o-gly.md) (Object Identifiers, OIDs) zulässige Aliase sind, ebenso wie die **szOID \_ \* *_-Konstanten. Diese Konstanten sind Definitionen (in Wincrypt.h), die die OIDs darstellen. Beispielsweise* ist _ szOID \_ COMMON \_ NAME** als "2.5.4.3" definiert. Folglich können Sie die **szOID-Konstanten \_ \*** als Aliase anstelle der OIDs verwenden, die sie darstellen.



| Eigenschaftenname                 | Aliase                                                                                                                                                        | Datentyp                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject.CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> **szOID \_ COMMON \_ NAME**<br/>                                                                           | **Zeichenfolge** (max. 64 Zeichen)  | Bei Benutzerzertifikaten der vollständige Name der Person. Bei Computerzertifikaten der *vollqualifizierte HostName*-Pfad, der **/**  in Domain Name System (DNS)-Suchen verwendet wird (z. B. *HostName*). _Beispiel_* _.com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Subject.Country"             | "Country" "C"<br/> "2.5.4.6"<br/> **szOID \_ COUNTRY \_ NAME**<br/>                                                                              | **Zeichenfolge** (max. 2 Zeichen)    | Das Land oder die Region des Antragstellers. Dies ist ein [*X.500-Länder-/Regionscode*](../secgloss/x-gly.md) mit zwei Zeichen (z. B. USA für USA oder Ca für Kanada).<br/> Viele dieser Codes mit zwei Zeichen sind im ISO 3166-Standard definiert. Darüber hinaus ist der Code des aktuellen Gebietsschemas über einen Aufruf der Windows-Funktion [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) verfügbar (durch Angabe eines *LCType* von LOCALE \_ SISO3166CTRYNAME).<br/> |
| "Subject.DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **\_ \_ SZOID-GERÄTESERIENNUMMER \_**<br/>                                                                         | **Zeichenfolge** (max. 1024 Zeichen) | Seriennummer des Geräts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **SZOID \_ DOMAIN \_ COMPONENT**<br/>                                              | **Zeichenfolge** (max. 128 Zeichen)  | Komponente eines DNS-Namens (Domain Name System).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "EMail" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Zeichenfolge** (max. 128 Zeichen)  | E-Mail-Adresse (z. B. someone@example.com " ").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.GivenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **SZOID \_ GIVEN \_ NAME**<br/>                                                                             | **Zeichenfolge** (max. 16 Zeichen)   | Vorname des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Initialen" "I"<br/> "2.5.4.43"<br/> **\_SZOID-INITIALEN**<br/>                                                                                 | **Zeichenfolge** (max. 5 Zeichen)    | Initialen des Betreffs (optional).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.Locality"            | "Locality" "L"<br/> "2.5.4.7"<br/> **szOID \_ LOCALITY \_ NAME**<br/>                                                                            | **Zeichenfolge** (max. 128 Zeichen)  | Name der Stadt des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject.Organization"        | "Organisation" "Org"<br/> "O"<br/> "2.5.4.10"<br/> **szOID \_ ORGANIZATION \_ NAME**<br/>                                                  | **Zeichenfolge** (max. 64 Zeichen)   | Rechtlicher Name der Organisation des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.OrgUnit"             | "OrgUnit" "OrganizationUnit"<br/> "OrganizationalUnit"<br/> "OU"<br/> "2.5.4.11"<br/> **SZOID \_ \_ \_ ORGANISATIONSEINHEITSNAME**<br/> | **Zeichenfolge** (max. 64 Zeichen)   | Name der untergeordneten Organisation oder Abteilung des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.State"               | "State" "ST"<br/> "S"<br/> "2.5.4.8"<br/> **SZOID \_ STATE OR PROVINCE \_ \_ \_ NAME**<br/>                                                    | **Zeichenfolge** (max. 128 Zeichen)  | Vollständiger Name des Bundesstaats oder der Provinz des Antragstellers (z. B. Kalifornien).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject.StreetAddress"       | "StreetAddress" "Street"<br/> "2.5.4.9"<br/> **szOID \_ STREET \_ ADDRESS**<br/>                                                                 | **Zeichenfolge** (max. 30 Zeichen)   | Adresse des Antragstellers oder Po Box.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.SurName"             | "SurName" "SN"<br/> "2.5.4.4"<br/> **szOID \_ SUR \_ NAME**<br/>                                                                                 | **Zeichenfolge** (max. 40 Zeichen)   | Nachname des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.Title"               | "Title" "T"<br/> "2.5.4.12"<br/> **szOID \_ TITLE**<br/>                                                                                       | **Zeichenfolge** (max. 64 Zeichen)   | Titel der Person, die das Zertifikat angefordert hat (optional).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Zeichenfolge** (max. 1024 Zeichen) | Unstrukturierte Adresse.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.UnstructuredName"    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **Zeichenfolge** (max. 1024 Zeichen) | Unstrukturierter Name.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Die folgenden Eigenschaften beziehen sich auf das Subjekt, obwohl es sich nicht um Namenseigenschaften handelt. Das Richtlinienmodul kann diese Eigenschaften nicht direkt festlegen.



| Eigenschaft                    | Datentyp                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request.DistinguishedName" | **Zeichenfolge** (max. 8192 Zeichen) | Der [*relative Distinguished Name*](../secgloss/r-gly.md) für die Anforderung, eine Textdarstellung des Betreffs in der Anforderung. Diese Darstellung besteht aus Namenseigenschaften, z.B. "CN=MyName, OU=MyOrgUnit, C=US". Die Zertifikatdienstanwendung legt diese Eigenschaft vor dem Aufrufen des Richtlinienmoduls fest, indem [**sie CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) mit dem Antragsteller von RawRequest aufruft. |
| "Request.RawName"           | **Binär** (max. 4.096 Bytes) | [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) binary subject [*BLOB*](../secgloss/b-gly.md) extracted from the request. Die Zertifikatdienstanwendung legt diese Eigenschaft vor dem Aufrufen des Richtlinienmoduls fest. sein Wert wird durch das Subject-Subjekt von RawRequest bestimmt.                                                                                     |
| "DistinguishedName"         | **Zeichenfolge** (max. 8192 Zeichen) | Der relative Distinguished Name für das Zertifikat, eine Textdarstellung des Antragstellers im Zertifikat. Diese Darstellung besteht aus Namenseigenschaften, z.B. "CN=MyName, OU=MyOrgUnit, C=US". Die Zertifikatdienstanwendung legt diese Eigenschaft nach dem Aufruf des Richtlinienmoduls fest, indem [**sie CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) mit rawName aufruft.                                                                                                               |
| "RawName"                   | **Binär** (max. 4.096 Bytes) | BLOB für binäre [](../secgloss/b-gly.md) ASN.1-Antragsteller, das zum Erstellen des Zertifikats verwendet wird. Die Zertifikatdienstanwendung legt diese Eigenschaft nach dem Aufruf des Richtlinienmoduls fest. sein Wert wird durch die Werte bestimmter Namenseigenschaften (Subject.CommonName usw.) bestimmt, die von subjectTemplate gesteuert werden.                                                                                                                                        |



 

Welche [*relativen Distinguished Name-Komponenten*](../secgloss/r-gly.md) in der DistinguishedName-Eigenschaft angezeigt werden und in welcher Reihenfolge sie angezeigt werden, wird durch den Registrierungswert "SubjectTemplate" gesteuert, der im folgenden Registrierungsschlüssel enthalten ist:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Wenn Zertifikatdienste [*Attributnamen*](../secgloss/a-gly.md) analysieren, werden Leerzeichen, Bindestriche (Minuszeichen) und Case ignoriert. Beispielsweise sind "AttributeName1", "Attribute Name1" und "Attribute-name1" gleichwertig. Bei Attributwerten ignoriert Certificate Services führende und nachfolgende Leerzeichen.

Alle vorangehenden Eigenschaften mit Ausnahme von DistinguishedName, RawName und Subject.Country unterstützen die Mehrwertsyntax mithilfe eines Newlinezeichens. Das Neulinientrennzeichen kann nicht deaktiviert oder geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zertifikateigenschaften](certificate-properties.md)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 

---
description: Namens Eigenschaften sind Eigenschaften von Zertifikaten und Zertifikat Anforderungen, die Daten zum Betreff darstellen, d. h. der Besitzer des Zertifikats oder die Person, für die ein Zertifikat angefordert wird.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Namens Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c5978b3fe5ab7c6ead39840dfb1793372c5feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217994"
---
# <a name="name-properties"></a>Namens Eigenschaften

Namens Eigenschaften sind Eigenschaften von Zertifikaten und Zertifikat Anforderungen, die Daten zum Betreff darstellen, d. h. der Besitzer des Zertifikats oder die Person, für die ein Zertifikat angefordert wird. Jede Name-Eigenschaft wird durch einen Eigenschaftsnamen identifiziert. Diese Namen sind nicht lokalisierbar. namens Eigenschaften entsprechen jedoch in der Regel einer Daten Bank Spalte für Zertifikat Dienste, und Sie können das Snap-in "Zertifizierungsstelle", das Befehlszeilen Tool "Certutil-Schema" oder die [**ienumcertviewcolumn:: GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) -Methode verwenden, um lokalisierte Versionen der Spaltennamen der Datenbank anzuzeigen.

Der Eigenschaftsname (aber nicht die Aliase) kann "Subject" aufweisen. als optionales Präfix. Wenn Sie z. b. auf den allgemeinen Namen des Subjekts verweisen möchten, können Sie entweder "CommonName" oder "Subject. CommonName" verwenden.

Neben dem Namen verfügt jede Eigenschaft über eine bestimmte Anzahl von Aliasen, die von den Zertifikat Diensten als Alternative Namen für die Eigenschaft erkannt werden. Beachten Sie, dass [*Objekt*](../secgloss/o-gly.md) -IDs (OIDs) akzeptable Aliase sind, ebenso wie die **szoid \_ \* *_-Konstanten. Diese Konstanten sind Definitionen (in Wincrypt. h), die die OIDs darstellen. Beispielsweise ist _* szoid \_ Common \_ Name** als "2.5.4.3" definiert. Folglich können Sie die **szoid \_ \** _-Konstanten als Aliase anstelle der OIDs verwenden, die Sie darstellen.



| Eigenschaftenname                 | Aliase                                                                                                                                                        | Datentyp                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject. CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> _ * szoid \_ allgemeiner \_ Name * *<br/>                                                                           | **String** (max. 64 chars)  | Für Benutzerzertifikate der vollständige Name der Person. Für Computer Zertifikate der voll qualifizierte *Hostname *- **/** _Pfad_ , der in Domain Name System (DNS)-suchen (z ***. b.** Hostname *) verwendet wird. _Beispiel_* _. com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Subject. Country"             | "Land" "C"<br/> 2.5.4.6<br/> **szoid- \_ Länder \_ Name**<br/>                                                                              | **Zeichenfolge** (max. 2 Zeichen)    | Das Land oder die Region des Subjekts. Dies ist ein [*X. 500*](../secgloss/x-gly.md) -Code mit zwei Zeichen Ländern (z. b. für USA oder ca für Kanada).<br/> Viele dieser zwei Zeichen Codes sind im ISO 3166-Standard definiert. Außerdem ist der Code des aktuellen Gebiets Schemas über einen Aufrufen der Windows-Funktion [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) verfügbar (durch Angabe eines *LCTYPE* - \_ SISO3166CTRYNAME).<br/> |
| "Subject. Geräte-ID"  | "Geräte-ID" "2.5.4.5"<br/> **\_ \_ Serien \_ Nummer des szoid-Geräts**<br/>                                                                         | **Zeichenfolge** (max. 1024 Zeichen) | Seriennummer des Geräts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. domaincomponent"     | "Domaincomponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **szoid- \_ Domänen \_ Komponente**<br/>                                              | **Zeichenfolge** (max. 128 Zeichen)  | Die Komponente eines Domain Name System-namens (DNS).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.Email"               | "E-Mail" "e"<br/> "1.2.840.113549.1.9.1"<br/> **szoid \_ RSA \_ EmailAddr**<br/>                                                                  | **Zeichenfolge** (max. 128 Zeichen)  | E-Mail-Adresse (z someone@example.com . b. "").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. givenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **der angegebene szoid- \_ \_ Name**<br/>                                                                             | **Zeichenfolge** (maximal 16 Zeichen)   | Vorname des Subjekts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Ini.            | "Initialen" "I"<br/> "2.5.4.43"<br/> **szoid- \_ Initialen**<br/>                                                                                 | **Zeichenfolge** (max. 5 Zeichen)    | Initialen des Subjekts (optional).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. Lokalität"            | "Ort" "L"<br/> "2.5.4.7"<br/> **Name der szoid- \_ Lokalität \_**<br/>                                                                            | **Zeichenfolge** (max. 128 Zeichen)  | Der Name der Stadt des Subjekts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject. Organization"        | "Organisation" "org"<br/> '<br/> 2.5.4.10<br/> **Name der szoid- \_ Organisation \_**<br/>                                                  | **Zeichenfolge** (max. 64 Zeichen)   | Gesetzlicher Name der Organisation des Subjekts.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. OrgUnit"             | "OrgUnit" "organizationunit"<br/> OrganizationalUnit<br/> Klägerin<br/> 2.5.4.11<br/> **\_Name der Organisations \_ Einheit \_ "szoid"**<br/> | **Zeichenfolge** (max. 64 Zeichen)   | Der Name der untergeordneten Organisation oder Abteilung des Subjekts.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. State"               | "State" "St"<br/> Hymnen<br/> 2.5.4.8<br/> **szoid- \_ Status \_ oder \_ Provinz \_ Name**<br/>                                                    | **Zeichenfolge** (max. 128 Zeichen)  | Der vollständige Name des Antragstellers Bundesland oder Provinz (z. b. Kalifornien).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject. StreetAddress"       | "StreetAddress" "Straße"<br/> "2.5.4.9"<br/> **szoid- \_ Straße \_**<br/>                                                                 | **Zeichenfolge** (max. 30 Zeichen)   | Die Adresse oder das Bestell Feld des Antragstellers.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. Nachname"             | "Nachname" "sn"<br/> "2.5.4.4"<br/> **szoid \_ - \_ Name**<br/>                                                                                 | **Zeichenfolge** (max. 40 Zeichen)   | Nachname des Subjekts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. Title"               | "Title" "T"<br/> "2.5.4.12"<br/> **szoid- \_ Titel**<br/>                                                                                       | **Zeichenfolge** (max. 64 Zeichen)   | Der Titel der Person, die das Zertifikat angefordert hat (optional).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject. unstructuredaddress" | "Unstructuredaddress" "1.2.840.113549.1.9.8"<br/> **szoid \_ RSA \_ unstructaddr**<br/>                                                                | **Zeichenfolge** (max. 1024 Zeichen) | Unstrukturierte Adresse.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. unstructuredname"    | "Unstructuredname" "1.2.840.113549.1.9.2"<br/> **szoid \_ RSA \_ unstructname**<br/>                                                                   | **Zeichenfolge** (max. 1024 Zeichen) | Unstrukturierter Name.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Die folgenden Eigenschaften beziehen sich auf den Betreff, obwohl es sich nicht um namens Eigenschaften handelt. Diese Eigenschaften können vom Richtlinien Modul nicht direkt festgelegt werden.



| Eigenschaft                    | Datentyp                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request. Unterer Name" | **Zeichenfolge** (max. 8192 Zeichen) | Der [*Relative Distinguished Name*](../secgloss/r-gly.md) für die Anforderung, eine Textdarstellung des Subjekts in der Anforderung. Diese Darstellung besteht aus den namens Eigenschaften, z. b. "CN = MyName, ou = MyOrgUnit, C = US". Die Zertifikat Dienst Anwendung legt diese Eigenschaft vor dem Aufrufen des Richtlinien Moduls fest, indem Sie " [**certnametostr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) " mit dem Betreff der rawrequest aufrufen. |
| "Request. RawName"           | **Binary** (max. 4096 Bytes) | [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) Binary Subject [*BLOB*](../secgloss/b-gly.md) , das aus der Anforderung extrahiert wurde. Diese Eigenschaft wird von der Zertifikat Dienst Anwendung vor dem Aufrufen des Richtlinien Moduls festgelegt. der Wert wird vom Betreff der rawrequest bestimmt.                                                                                     |
| "DistinguishedName"         | **Zeichenfolge** (max. 8192 Zeichen) | Der Relative Distinguished Name für das Zertifikat, eine Textdarstellung des Subjekts im Zertifikat. Diese Darstellung besteht aus den namens Eigenschaften, z. b. "CN = MyName, ou = MyOrgUnit, C = US". Die Zertifikat Dienst Anwendung legt diese Eigenschaft fest, nachdem das Richtlinien Modul aufgerufen wurde, indem Sie " [**certnametostr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) " mithilfe von "RawName" aufgerufen hat.                                                                                                               |
| "RawName"                   | **Binary** (max. 4096 Bytes) | ASN. 1 Binary Subject [*BLOB*](../secgloss/b-gly.md) , das zum Erstellen des Zertifikats verwendet wird. Die Zertifikat Dienst Anwendung legt diese Eigenschaft fest, nachdem das Richtlinien Modul aufgerufen wurde. der Wert wird durch die Werte spezifischer namens Eigenschaften (Subject. CommonName usw.) bestimmt, wie von der subjettemplate gesteuert.                                                                                                                                        |



 

Welche Komponenten für den [*relativen Distinguished Name*](../secgloss/r-gly.md) in der Eigenschaft "Distinguished shedname" angezeigt werden, und die Reihenfolge, in der Sie angezeigt werden, wird durch den Registrierungs Wert "subjettemplate" gesteuert, der im folgenden Registrierungsschlüssel enthalten ist:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Wenn Zertifikat Dienste [*Attribut*](../secgloss/a-gly.md) Namen analysieren, werden Leerzeichen, Bindestriche (Minuszeichen) und Groß-/Kleinschreibung ignoriert. Beispielsweise sind "AttributeName1", "Attribute Name1" und "Attribute-Name1" gleichwertig. Bei Attributwerten werden von den Zertifikat Diensten führende und nachfolgende Leerzeichen ignoriert.

Alle vorangehenden Eigenschaften außer "Subject shedname", "RawName" und "Subject. Country" unterstützen eine mehrwertige Syntax mithilfe eines Zeilen Vorzeichens. Das Zeilen Umleitungs Trennzeichen kann nicht deaktiviert oder geändert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zertifikat Eigenschaften](certificate-properties.md)
</dt> <dt>

[**Icertserverexit:: getcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**Icertserverexit:: getRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**Icertserverpolicy:: getcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**Icertserverpolicy:: getRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**Icertserverpolicy:: setcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 

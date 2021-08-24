---
description: Wird mit Codierungs- und Decodierungsvorgängen verwendet.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Konstanten für Netscape-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315d27039bf29220f1a7cdfba82baa1350da084025f436aa1b4746d7e92f5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876750"
---
# <a name="constants-for-netscape-extensions"></a>Konstanten für Netscape-Erweiterungen

Die folgenden Netscape-Erweiterungen werden mit Codierungs- und Decodierungsvorgängen verwendet. Die vordefinierten Netscape-Konstanten und Objektbezeichnerzeichenfolgen werden nicht direkt mit den Codierungs- oder Decodierungsfunktionen [**CryptEncodeObject,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject) [**CryptEncodeObjectEx,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) [**CryptSignAndEncodeCertificate,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate) [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)oder [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)verwendet. Stattdessen erfordern diese Erweiterungen die Verwendung des *angezeigten lpszStructType.*

Weitere Details, die für einige Netscape-Erweiterungen gelten, finden Sie in den Hinweisen in der Tabelle.



| Netscape-Zertifikaterweiterungsobjektbezeichner                      | *lpszStructType*                                           | Entsprechende *pvStructInfo*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szOID \_ NETSCAPE \_ BASE \_ URL"2.16.840.1.113730.1.2"<br/>           | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Value-Members** verweist auf eine IA5-ZEICHENFOLGE, \_ die am Anfang aller relative URL Adressen in einem Zertifikat hinzugefügt wurde. Diese Erweiterung kann als Optimierung angesehen werden, um die Größe der URL-Erweiterungen zu reduzieren.                                                                                                       |
| szOID \_ NETSCAPE \_ CA POLICY \_ \_ URL"2.16.840.1.113730.1.8"<br/>     | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Wertmembers** verweist auf eine IA5-ZEICHENFOLGE, \_ die relative oder absolute URL der Webseite, die die Richtlinien beschreibt, unter denen das Zertifikat ausgestellt wurde.                                                                                                                                                            |
| szOID \_ NETSCAPE \_ CA REVOCATION \_ \_ URL"2.16.840.1.113730.1.4"<br/> | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Value-Members** verweist auf eine IA5-ZEICHENFOLGE, die die relative oder absolute URL ist, \_ die zum Überprüfen des Sperrstatus von Zertifikaten verwendet wird, die von der [*Zertifizierungsstelle*](../secgloss/c-gly.md) signiert wurden, zu der das aktuelle Zertifikat gehört. |
| szOID \_ NETSCAPE \_ CERT \_ RENEWAL \_ URL"2.16.840.1.113730.1.7"<br/>  | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Wertmembers** verweist auf eine IA5 \_ STRING-Zeichenfolge, die die relative oder absolute URL eines Zertifikaterneuerungsformulars ist.                                                                                                                                                                                                     |
| szOID \_ NETSCAPE \_ CERT \_ SEQUENCE"2.16.840.1.113730.2.5"<br/>      | PKCS \_ CONTENT \_ INFO \_ SEQUENCE \_ OF \_ ANY                     | [**CRYPT \_ CONTENT \_ INFO \_ SEQUENCE \_ OF \_ ANY**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ NETSCAPE \_ CERT \_ TYPE"2.16.840.1.113730.1.1"<br/>          | X509 \_ BITS                                                 | [**CRYPT \_ BIT \_ BLOB**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ NETSCAPE \_ COMMENT"2.16.840.1.113730.1.13"<br/>            | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Value-Members** verweist auf eine IA5-ZEICHENFOLGE, \_ bei der es sich um einen Kommentar handelt, der angezeigt werden soll, wenn das Zertifikat angezeigt wird.                                                                                                                                                                                                         |
| szOID \_ NETSCAPE \_ REVOCATION \_ URL"2.16.840.1.113730.1.3"<br/>     | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Wertmembers** verweist auf eine IA5-ZEICHENFOLGE, \_ die ein relativer oder absolute URL ist, der zum Überprüfen des Sperrstatus des Zertifikats verwendet wird.                                                                                                                                                                              |
| szOID \_ NETSCAPE \_ SSL SERVER \_ \_ NAME"2.16.840.1.113730.1.12"<br/>  | X509 \_ ANY STRING oder \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwValueType-Member** ist auf CERT \_ RDN \_ IA5 \_ STRING festgelegt. Das **pbData-Element** des **Wertmembers** verweist auf eine IA5-ZEICHENFOLGE, bei der es \_ sich um einen Shellausdruck handelt, der verwendet wird, um den Hostnamen des SSL-Servers mit diesem Zertifikat abzugleichen.                                                                                                                                                                       |



 

Für alle Codierungsfunktionen, die entweder X509 \_ ANY \_ STRING oder X5O9 \_ UNICODE ANY STRING \_ \_ **lpszStructType** verwenden, wird X509 \_ ANY STRING \_ verwendet, wenn das Zeichenfolgenformat im **pbData-Member** des **Wertmembers** [*ASCII*](../secgloss/a-gly.md)ist, und X509 UNICODE ANY STRING \_ wird \_ \_ verwendet, wenn das Zeichenfolgenformat UNICODE ist. Im Unicode-Fall muss die Zeichenfolge vor der Codierung in eine IA5-ZEICHENFOLGE konvertiert werden, \_ indem der **dwValueType-Member** der [**CERT NAME \_ \_ VALUE-Struktur**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) auf CERT \_ RDN \_ IA5 STRING festgelegt \_ wird.

Für Decodierungsfunktionen wählt der Benutzer das Format der Ausgabezeichenfolge aus. Verwenden Sie X509 \_ ANY \_ STRING, wenn das gewünschte Zeichenfolgenformat ASCII ist, und X509 \_ UNICODE ANY \_ \_ STRING, wenn das gewünschte Zeichenfolgenformat Unicode ist.

Für die \_ SZOID NETSCAPE \_ CERT \_ RENEWAL \_ URL-Erweiterung enthält die Datenstruktur eine relative oder absolute URL, die auf ein Zertifikaterneuerungsformular verweist. Der Zugriff auf das Verlängerungsformular erfolgt mit einer HTTP GET-Methode unter Verwendung einer URL, die die Verkettung der Erneuerungs-URL und der Zertifikatsseriennummer ist. Die Zertifikatsseriennummer wird als Zeichenfolge mit ASCII-Hexadezimalziffern codiert. Wenn z. B. netscape-base-url https://*Zertifizierungsstellen-URL*/, netscape-cert-renewal-url cgi-bin/check-renew.cgi? und die Seriennummer des Zertifikats 173420 lautet, lautet die resultierende URL: https://*Zertifizierungsstellen-URL*/cgi-bin/check-renew.cgi?02a56c. Das zurückgegebene Dokument sollte ein HTML-Formular sein, mit dem der Benutzer eine Erneuerung seines Zertifikats anfordern kann.

Für die szOID \_ NETSCAPE \_ CERT \_ SEQUENCE-Erweiterung mit X509 \_ ASN \_ ENCODING wird das Zertifikat als PKCS CONTENT INFO-Struktur codiert, die \_ eine Sequenz von ANY \_ umschließt. Der Wert des **contentType-Members** ist **pszObjId,** während das Inhaltsfeld die folgende Struktur aufweist:

SequenceOfAny ::= SEQUENCE OF ANY

Die [**CRYPT \_ DER \_ BLOB-s**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))in der [**CRYPT CONTENT INFO SEQUENCE \_ OF \_ \_ \_ \_ ANY**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any) **es rgValue** member zeigen auf codierte X509-Zertifikate.

Für szOID \_ NETSCAPE \_ CERT \_ TYPE-Erweiterungen werden die folgenden Bits definiert.



| Bitwert | Entsprechender Typ                      |
|-----------|-----------------------------------------|
| 0x80      | NETSCAPE \_ SSL \_ CLIENT \_ AUTH \_ CERT \_ TYPE |
| 0x40      | NETSCAPE \_ SSL \_ SERVER \_ AUTH \_ CERT \_ TYPE |
| 0x04      | NETSCAPE \_ SSL \_ CA \_ CERT \_ TYPE           |



 

Für die \_ szOID NETSCAPE \_ REVOCATION \_ URL-Erweiterungen kann ein relativer oder absolute URL verwendet werden, um den Sperrstatus eines Zertifikats zu überprüfen. Die Sperrprüfung wird als HTTP GET-Methode mithilfe einer URL durchgeführt, die die Verkettung von Sperr-URL und Zertifikatsseriennummer ist. Die Zertifikatsseriennummer wird als Zeichenfolge mit ASCII-Hexadezimalziffern codiert. Wenn die netscape-base-url beispielsweise https: \/ /www.certs-r-us.com/ ist, lautet die netscape-revocation-url cgi-bin/check-rev.cgi?, und die Seriennummer des Zertifikats lautet 173420. Die resultierende URL lautet: https: \/ /www.certs-r-us.com/cgi-bin/check-rev.cgi?02a56c.

Der Server sollte ein Dokument mit dem Inhaltstyp application/x-netscape-revocation zurückgeben. Das Dokument sollte eine einzelne ASCII-Ziffer enthalten: "1", wenn das Zertifikat derzeit nicht gültig ist, und "0", wenn es derzeit gültig ist.

Beachten Sie, dass für alle URLs, die die Seriennummer des Zertifikats enthalten, die Seriennummer als Zeichenfolge codiert wird, die aus einer geraden Anzahl von Hexadezimalziffern besteht. Wenn die Anzahl der signifikanten Ziffern ungerade ist, weist die Zeichenfolge eine einzelne führende Null auf, um sicherzustellen, dass eine gerade Anzahl von Ziffern generiert wird.

 

 

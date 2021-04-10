---
description: Wird verwendet, um Vorgänge zu codieren und zu decodieren.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Konstanten für Netscape-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103870075"
---
# <a name="constants-for-netscape-extensions"></a>Konstanten für Netscape-Erweiterungen

Die folgenden Netscape-Erweiterungen werden mit Codierungs-und Decodierungsvorgängen verwendet. Die von Netscape vordefinierten Konstanten und objektbezeichnerzeichenfolgen werden nicht direkt mit den Codierungs-oder Decodierungs Funktionen, [**cryptencodeobject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**cryptencodeobjectex**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**cryptsignandencodecertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**cryptdecodeobject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)oder [**cryptdecodeobjectex**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)verwendet. Stattdessen benötigen diese Erweiterungen die Verwendung des gezeigten *lpszstructtype* .

Weitere Details, die für einige Netscape-Erweiterungen gelten, finden Sie in den Hinweisen in der Tabelle.



| Objekt Bezeichner für die Netscape-Zertifikat Erweiterung                      | *lpszstructtype*                                           | Entsprechendes *pvstructinfo*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szoid \_ Netscape- \_ Basis- \_ URL "2.16.840.1.113730.1.2"<br/>           | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die am Anfang aller relative URL Adressen in einem Zertifikat hinzugefügt wird. Diese Erweiterung kann als Optimierung angesehen werden, um die Größe der URL-Erweiterungen zu verringern.                                                                                                       |
| szoid \_ Netscape \_ ca- \_ Richtlinien- \_ URL "2.16.840.1.113730.1.8"<br/>     | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die relative oder absolute URL der Webseite, die die Richtlinien beschreibt, unter denen das Zertifikat ausgestellt wurde.                                                                                                                                                            |
| szoid \_ Netscape ca-Sperr- \_ \_ \_ URL "2.16.840.1.113730.1.4"<br/> | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die die relative oder absolute URL ist, die zum Überprüfen des Sperr Status von Zertifikaten verwendet wird, die von der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle signiert wurden, der das aktuelle Zertifikat angehört |
| szoid \_ Netscape \_ CERT- \_ Erneuerungs- \_ URL "2.16.840.1.113730.1.7"<br/>  | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die die relative oder absolute URL eines Zertifikats Erneuerungs Formulars ist.                                                                                                                                                                                                     |
| szoid \_ Netscape- \_ CERT- \_ Sequenz "2.16.840.1.113730.2.5"<br/>      | PKCS \_ - \_ Inhalts \_ Informations \_ Sequenz \_ beliebiger                     | [**Crypt \_ - \_ Inhalts \_ Informations \_ Sequenz \_ beliebiger**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szoid \_ Netscape- \_ CERT- \_ Typ "2.16.840.1.113730.1.1"<br/>          | X509- \_ Bits                                                 | [**Crypt \_ - \_ bitblob**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szoid \_ Netscape- \_ Kommentar "2.16.840.1.113730.1.13"<br/>            | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die ein Kommentar ist, der angezeigt wird, wenn das Zertifikat angezeigt wird.                                                                                                                                                                                                         |
| szoid Netscape-Sperr- \_ \_ \_ URL "2.16.840.1.113730.1.3"<br/>     | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **Werttyps** verweist auf eine IA5- \_ Zeichenfolge, die eine relative oder absolute URL ist, die zum Überprüfen des Sperr Status des Zertifikats verwendet wird.                                                                                                                                                                              |
| szoid \_ Netscape \_ SSL- \_ Server \_ Name "2.16.840.1.113730.1.12"<br/>  | X509 \_ Any \_ String oder x509 \_ Unicode \_ Any \_ String<br/> | [**Zertifikat \_ der namens \_ Wert**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Der **dwvaluetype** -Member ist auf CERT \_ RDN \_ IA5 \_ String festgelegt. Der **pbData** -Member des **wertemembers** verweist auf eine IA5- \_ Zeichenfolge, die ein shellausdruck ist, der verwendet wird, um den Hostnamen aus dem SSL-Server mit diesem Zertifikat abzugleichen.                                                                                                                                                                       |



 

Für alle Codierungs Funktionen, die entweder die x. 509- \_ \_ Zeichenfolge oder die X5O9- \_ Unicode- \_ \_ Zeichenfolge **lpszstructtype** verwenden, \_ wird x509 Any \_ String verwendet, wenn das Zeichen folgen Format im **pbData** -Member des **Werttyps** [*ASCII*](../secgloss/a-gly.md)ist, und x509 \_ Unicode \_ jede \_ Zeichenfolge verwendet wird, wenn das Zeichen folgen Format Unicode ist. Im Unicode-Fall muss die Zeichenfolge vor der Codierung in eine IA5-Zeichenfolge konvertiert werden, \_ indem der **dwvaluetype** -Member der [**CERT \_ Name \_ value**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) -Struktur auf CERT \_ RDN IA5 String festgelegt wird \_ \_ .

Für Decodierungs Funktionen wählt der Benutzer das Format der Ausgabe Zeichenfolge aus. Verwenden Sie die x. 509 \_ \_ -Zeichenfolge, wenn das gewünschte Zeichen folgen Format ASCII ist, und x509 \_ Unicode \_ eine beliebige \_ Zeichenfolge, wenn das gewünschte Zeichen folgen Format Unicode

Für die URL-Erweiterung "szoid \_ Netscape \_ CERT \_ RENEWAL" \_ enthält die Datenstruktur einen relativen oder absolute URL, der auf ein Zertifikat Erneuerungs Formular verweist. Der Zugriff auf das Erneuerungs Formular erfolgt über eine HTTP Get-Methode unter Verwendung einer URL, die die Verkettung der Erneuerungs-URL und der Zertifikat Seriennummer ist. Die Seriennummer des Zertifikats ist als Zeichenfolge mit hexadezimalen ASCII-Ziffern codiert. Wenn beispielsweise die Netscape-base-URL https://-Zertifizierungsstellen-*URL*/lautet, ist Netscape-CERT-Renewal-URL cgi-bin/Check-renew. cgi?, und die Seriennummer des Zertifikats ist 173420. die resultierende URL lautet: https://*Zertifizierungs* stellen-URL/cgi-bin/Check-renew.cgi? 02a56c. Das zurückgegebene Dokument sollte ein HTML-Formular sein, das es dem Benutzer ermöglicht, eine Erneuerung seines Zertifikats anzufordern.

Für die szoid \_ Netscape- \_ CERT- \_ Sequenz Erweiterung mit X509 \_ ASN- \_ Codierung wird das Zertifikat als PKCS-Inhalts Informationsstruktur codiert, die \_ \_ eine Sequenz beliebiger Daten umwickelt. Der Wert des **ContentType** -Members ist " **pszobjid**", während das Inhaltsfeld die folgende Struktur ist:

Sequenceofany:: = Sequenz beliebiger

Die [**crypt \_ - \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))s in der [**crypt \_ Content \_ Info \_ Sequence \_ eines \_ beliebigen**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any) **rgvalue** -Members zeigen auf codierte X509-Zertifikate.

Für szoid \_ Netscape \_ CERT \_ Type Extensions werden die folgenden Bits definiert.



| Bitwert | Entsprechender Typ                      |
|-----------|-----------------------------------------|
| 0x80      | Netscape \_ SSL-clientauthentifizierungstyp \_ \_ \_ \_ |
| 0x40      | Netscape- \_ SSL-Server- \_ \_ \_ \_ Authentifizierungstyp |
| 0x04      | Netscape \_ SSL- \_ ca-CERT- \_ \_ Typ           |



 

Für die szoid Netscape-Sperr- \_ \_ URL- \_ Erweiterungen kann ein relativer oder absolute URL verwendet werden, um den Sperr Status eines Zertifikats zu überprüfen. Die Sperr Überprüfung wird als HTTP Get-Methode durchgeführt, indem eine URL verwendet wird, bei der es sich um die Verkettung von "Widerruf-URL" und "Zertifikat-serielle Nummer" handelt. Die Seriennummer des Zertifikats ist als Zeichenfolge mit hexadezimalen ASCII-Ziffern codiert. Wenn z. b. die Netscape-base-URL https: \/ /www.certs-r-US.com/lautet, ist Netscape-Sperr-URL cgi-bin/Check-Rev. cgi?, und die Seriennummer des Zertifikats ist 173420. die resultierende URL lautet: https: \/ /www.certs-r-US.com/cgi-bin/Check-Rev.cgi?02a56c.

Der Server sollte ein Dokument mit dem Inhaltstyp "application/x-Netscape-Widerruf" zurückgeben. Das Dokument muss eine einzelne ASCII-Ziffer ("1") enthalten, wenn das Zertifikat derzeit nicht gültig ist, und "0", wenn es aktuell gültig ist.

Beachten Sie, dass für alle URLs, die die Seriennummer des Zertifikats enthalten, die Seriennummer als Zeichenfolge codiert wird, die aus einer geraden Anzahl von hexadezimalen Ziffern besteht. Wenn die Anzahl der signifikanten Ziffern ungerade ist, weist die Zeichenfolge eine einzige führende Null auf, um sicherzustellen, dass eine gerade Anzahl von Ziffern generiert wird.

 

 

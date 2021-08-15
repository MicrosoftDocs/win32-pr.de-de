---
description: Listet die von CryptoAPI bereitgestellten Funktionen auf.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: Kryptografiefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65c04d3cb1ff619d03d7f0340fc4f94826722f8ed6c0457987b8ec432a66128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768342"
---
# <a name="cryptography-functions"></a>Kryptografiefunktionen

Kryptografiefunktionen werden gemäß der Verwendung wie folgt kategorisiert:

-   [CryptXML-Funktionen](#cryptxml-functions)
-   [Signerfunktionen](#signer-functions)
-   [Grundlegende Kryptografiefunktionen](#base-cryptography-functions)
    -   [Dienstanbieterfunktionen](#service-provider-functions)
    -   [Schlüsselgenerierungs- und Exchange funktionen](#key-generation-and-exchange-functions)
    -   [Objektcodierungs- und Decodierungsfunktionen](#object-encoding-and-decoding-functions)
    -   [Datenverschlüsselungs- und Entschlüsselungsfunktionen](#data-encryption-and-decryption-functions)
    -   [Hash- und digitale Signaturfunktionen](#hash-and-digital-signature-functions)
-   [Certificate and Certificate Store Functions](#certificate-and-certificate-store-functions)
    -   [Certificate Store Functions](#certificate-and-certificate-store-functions)
    -   [Zertifikat- und Zertifikatswartungsfunktionen Store](#certificate-and-certificate-store-maintenance-functions)
    -   [Zertifikatfunktionen](#certificate-functions)
    -   [Funktionen der Zertifikatsperrliste](#certificate-revocation-list-functions)
    -   [Zertifikatvertrauenslistenfunktionen](#certificate-trust-list-functions)
    -   [Erweiterte Eigenschaftenfunktionen](#extended-property-functions)
-   [MakeCert-Funktionen](#makecert-functions)
-   [Zertifikatüberprüfungsfunktionen](#certificate-verification-functions)
    -   [Überprüfungsfunktionen mit CTLs](#verification-functions-using-ctls)
    -   [Überprüfungsfunktionen der Zertifikatkette](#certificate-chain-verification-functions)
-   [Nachrichtenfunktionen](#message-functions)
    -   [Nachrichtenfunktionen auf niedriger Ebene](#low-level-message-functions)
    -   [Vereinfachte Nachrichtenfunktionen](#simplified-message-functions)
-   [Zusatzfunktionen](#auxiliary-functions)
    -   [Datenverwaltung Functions](#data-management-functions)
    -   [Datenkonvertierungsfunktionen](#data-conversion-functions)
    -   [Erweiterte Schlüsselverwendungsfunktionen](#enhanced-key-usage-functions)
    -   [Schlüsselbezeichnerfunktionen](#key-identifier-functions)
    -   [OID-Unterstützungsfunktionen](#oid-support-functions)
    -   [Funktionen zum Abrufen von Remoteobjekten](#remote-object-retrieval-functions)
    -   [PFX-Funktionen](#pfx-functions)
-   [Sicherungs- und Wiederherstellungsfunktionen für Zertifikatdienste](#certificate-services-backup-and-restore-functions)
-   [Rückruffunktionen](#callback-functions)
-   [Katalogdefinitionsfunktionen](#catalog-definition-functions)
-   [Katalogfunktionen](#catalog-functions)
-   [WinTrust Functions](#wintrust-functions)
-   [Objektlocatorfunktionen](#object-locator-functions)

## <a name="cryptxml-functions"></a>CryptXML-Funktionen

Die kryptografischen XML-Funktionen stellen eine API zum Erstellen und Darstellen digitaler Signaturen mit xml-formatierten Daten bereit. Informationen zu XML-formatierten Signaturen finden Sie in der XML-Signature Syntax and Processing-Spezifikation unter <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Funktion                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ein \_ SHAFinal**](a-shafinal.md)                                                 | Berechnet den endgültigen Hash der von der MD5Update-Funktion eingegebenen Daten.                                                                                                                                                                                                                                           |
| [**Ein \_ SHAInit**](a-shainit.md)                                                   | Initiiert das Hashing eines Datenstroms.                                                                                                                                                                                                                                                                       |
| [**Ein \_ SHAUpdate**](a-shaupdate.md)                                               | Fügt einem angegebenen Hashobjekt Daten hinzu.                                                                                                                                                                                                                                                                            |
| [**CryptXmlCreateReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Erstellt einen Verweis auf eine XML-Signatur.                                                                                                                                                                                                                                                                         |
| [**CryptXmlAddObject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Fügt das **Object-Element** der Signatur im Dokumentkontext hinzu, der für die Codierung geöffnet wurde.                                                                                                                                                                                                                        |
| [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Schließt ein kryptografisches XML-Objekthandle.                                                                                                                                                                                                                                                                        |
| [**CryptXmlDigestReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Wird von einer Anwendung verwendet, um den aufgelösten Verweis zu verdauen. Diese Funktion wendet Transformationen an, bevor der Digest aktualisiert wird.                                                                                                                                                                                            |
| [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Gibt den \_ von \_ der [**CryptXmlDllCreateDigest-Funktion**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest) zugeordneten CRYPT XML DIGEST frei.                                                                                                                                                                                               |
| [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Erstellt ein Digestobjekt für die angegebene Methode.                                                                                                                                                                                                                                                                |
| [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Analysiert das **KeyValue-Element** und erstellt ein Cryptography API: Next Generation (CNG) BCrypt-Schlüsselhandle, um eine Signatur zu überprüfen.                                                                                                                                                                                   |
| [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Fügt Daten in den Digest ein.                                                                                                                                                                                                                                                                                       |
| [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Codiert **SignatureMethod-** oder **DigestMethod-Elemente** für agile Algorithmen mit Standardparametern.                                                                                                                                                                                                           |
| [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Codiert ein **KeyValue-Element.**                                                                                                                                                                                                                                                                                  |
| [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Ruft den Digestwert ab.                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Decodiert den XML-Algorithmus und gibt Informationen über den Algorithmus zurück.                                                                                                                                                                                                                                           |
| [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Ruft einen Zeiger auf die kryptografischen Erweiterungsfunktionen für den angegebenen Algorithmus ab.                                                                                                                                                                                                                        |
| [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Signiert Daten.                                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Überprüft eine Signatur.                                                                                                                                                                                                                                                                                            |
| [**CryptXmlEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Codiert Signaturdaten mithilfe der angegebenen RÜCKRUFFUNKTION des XML-Writers.                                                                                                                                                                                                                                       |
| [**CryptXmlGetAlgorithmInfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Decodiert die CRYPT \_ XML \_ ALGORITHM-Struktur und gibt Informationen zum Algorithmus zurück.                                                                                                                                                                                                                         |
| [**CryptXmlGetDocContext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Gibt den vom angegebenen Handle angegebenen Dokumentkontext zurück.                                                                                                                                                                                                                                                   |
| [**CryptXmlGetReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Gibt das vom angegebenen Handle angegebene **Reference-Element** zurück.                                                                                                                                                                                                                                              |
| [**CryptXmlGetSignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Gibt ein **XML-Signaturelement** zurück.                                                                                                                                                                                                                                                                            |
| [**CryptXmlGetStatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Gibt eine [**CRYPT \_ XML \_ STATUS-Struktur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) zurück, die Statusinformationen über das vom angegebenen Handle angegebene Objekt enthält.                                                                                                                                                           |
| [**CryptXmlGetTransforms**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Gibt Informationen zur Standardtransformationsketten-Engine zurück.                                                                                                                                                                                                                                                    |
| [**CryptXmlImportPublicKey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Importiert den öffentlichen Schlüssel, der vom angegebenen Handle angegeben wird.                                                                                                                                                                                                                                                         |
| [**CryptXmlOpenToEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Öffnet eine digitale XML-Signatur zum Codieren und gibt ein Handle des geöffneten **Signature-Elements** zurück. Das Handle kapselt einen Dokumentkontext mit einer einzelnen [**CRYPT \_ XML \_ SIGNATURE-Struktur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) und bleibt geöffnet, bis die [**CryptXmlClose-Funktion**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) aufgerufen wird. |
| [**CryptXmlOpenToDecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Öffnet eine digitale XML-Signatur zum Decodieren und gibt das Handle des Dokumentkontexts zurück, der eine [**CRYPT \_ XML \_ SIGNATURE-Struktur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) kapselt. Der Dokumentkontext kann ein oder mehrere **Signature-Elemente** enthalten.                                                                 |
| [**CryptXmlSetHMACSecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Legt das HMAC-Geheimnis auf dem Handle fest, bevor die [**CryptXmlSign-**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) oder [**CryptXmlVerify-Funktion**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) aufgerufen wird.                                                                                                                                                        |
| [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Erstellt eine kryptografische Signatur eines **SignedInfo-Elements.**                                                                                                                                                                                                                                                   |
| [**CryptXmlVerifySignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Führt eine kryptografische Signaturüberprüfung eines **SignedInfo-Elements** aus.                                                                                                                                                                                                                                       |
| [*PFN \_ CRYPT \_ XML \_ WRITE \_ CALLBACK*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Erstellt eine Transformation für einen angegebenen Datenanbieter.                                                                                                                                                                                                                                                               |
| [*PFN \_ CRYPT \_ XML \_ CREATE \_ TRANSFORM*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Schreibt kryptografische XML-Daten.                                                                                                                                                                                                                                                                                   |
| [*PFN \_ CRYPT \_ XML \_ DATA \_ PROVIDER \_ READ*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Liest kryptografische XML-Daten.                                                                                                                                                                                                                                                                                    |
| [*PFN \_ CRYPT \_ XML \_ DATA \_ PROVIDER \_ CLOSE*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Gibt den kryptografischen XML-Datenanbieter frei.                                                                                                                                                                                                                                                                    |
| [*PFN \_ CRYPT \_ XML \_ ENUM \_ ALG \_ INFO*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Listet vordefinierte und registrierte [**CRYPT \_ XML \_ ALGORITHM \_ INFO-Einträge**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) auf.                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Signerfunktionen

Stellt Funktionen zum Signieren und Zeitstempel von Daten bereit.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SignerFreeSignerContext**](signerfreesignercontext.md) | Gibt eine [**SIGNER \_ CONTEXT-Struktur frei,**](signer-context.md) die durch einen vorherigen Aufruf der [**SignerSignEx-Funktion**](signersignex.md) zugeordnet wurde.                                                                                                                                                                                                                                                                      |
| [**SignError**](signerror.md)                             | Ruft die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf und konvertiert den Rückgabecode in ein **HRESULT.**                                                                                                                                                                                                                                                                                                            |
| [**SignerSign**](signersign.md)                           | Signiert die angegebene Datei.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SignerSignEx**](signersignex.md)                       | Signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Signiert und zeitstempelt die angegebene Datei, sodass mehrere geschachtelte Signaturen möglich sind.                                                                                                                                                                                                                                                                                                                                      |
| [**SignerTimeStamp**](signertimestamp.md)                 | Zeitstempel des angegebenen Antragstellers. Diese Funktion unterstützt das Authenticode-Zeitstempeln. Verwenden Sie die [**SignerTimeStampEx2-Funktion,**](signertimestampex2.md) um den Zeitstempel der X.509 Public Key Infrastructure (RFC 3161) auszuführen.                                                                                                                                                                                       |
| [**SignerTimeStampEx**](signertimestampex.md)             | Zeitstempel des angegebenen Antragstellers und optional Rückgabe eines Zeigers auf eine [**SIGNER \_ CONTEXT-Struktur,**](signer-context.md) die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält. Diese Funktion unterstützt das Authenticode-Zeitstempeln. Verwenden Sie die [**SignerTimeStampEx2-Funktion,**](signertimestampex2.md) um den Zeitstempel der X.509 Public Key Infrastructure (RFC 3161) auszuführen. |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Zeitstempel des angegebenen Antragstellers und optional Rückgabe eines Zeigers auf eine [**SIGNER \_ CONTEXT-Struktur,**](signer-context.md) die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält. Diese Funktion kann verwendet werden, um X.509 Public Key Infrastructure, RFC 3161-konform, Zeitstempel auszuführen.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Zeitstempel des angegebenen Antragstellers und Unterstützung für das Festlegen von Zeitstempeln für mehrere Signaturen.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Grundlegende Kryptografiefunktionen

Grundlegende kryptografische Funktionen stellen die flexibelste Möglichkeit zum Entwickeln von Kryptografieanwendungen bereit. Die gesamte Kommunikation mit einem [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) erfolgt über diese Funktionen.

Ein CSP ist ein unabhängiges Modul, das alle kryptografischen Vorgänge ausführt. Für jede Anwendung, die kryptografische Funktionen verwendet, ist mindestens ein CSP erforderlich. Eine einzelne Anwendung kann gelegentlich mehr als einen CSP verwenden.

Wenn mehr als ein CSP verwendet wird, kann der zu verwendende CSP in den KryptoAPI-Kryptografiefunktionsaufrufen angegeben werden. Ein CSP, der Microsoft Base Cryptographic Provider, wird mit [*cryptoAPI*](../secgloss/c-gly.md)gebündelt. Dieser CSP wird von vielen CryptoAPI-Funktionen als Standardanbieter verwendet, wenn kein anderer CSP angegeben wird.

Jeder CSP bietet eine andere Implementierung der kryptografischen Unterstützung für CryptoAPI. Einige stellen stärkere kryptografische Algorithmen bereit. andere enthalten Hardwarekomponenten, z. B. [*Smartcards.*](../secgloss/s-gly.md) Darüber hinaus können einige CSPs gelegentlich direkt mit Benutzern kommunizieren, z. B. wenn [*digitale Signaturen*](../secgloss/d-gly.md) mithilfe des [*privaten Signaturschlüssels*](../secgloss/s-gly.md)des Benutzers ausgeführt werden.

Grundlegende kryptografische Funktionen befinden sich in den folgenden allgemeinen Gruppen:

-   Dienstanbieterfunktionen
-   Schlüsselgenerierungs- und Exchange funktionen
-   Objektcodierungs- und Decodierungsfunktionen
-   Datenverschlüsselungs- und Entschlüsselungsfunktionen
-   Hash- und digitale Signaturfunktionen

### <a name="service-provider-functions"></a>Dienstanbieterfunktionen

Anwendungen verwenden die folgenden Dienstfunktionen, um eine Verbindung mit einem [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) herzustellen und diese zu trennen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Übernimmt ein Handle für den <a href="/windows/desktop/SecGloss/k-gly"><em>Schlüsselcontainer</em></a> des aktuellen Benutzers innerhalb eines bestimmten CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>CryptContextAddRef</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erhöht den <a href="/windows/desktop/SecGloss/r-gly"><em>Verweiszähler</em></a> für ein <a href="hcryptprov.md"><strong>HCRYPTPROV-Handle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>CryptEnumProviders</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Listet die Anbieter auf einem Computer auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>CryptEnumProviderTypes</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Listet die Typen von Anbietern auf, die auf dem Computer unterstützt werden.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>CryptGetDefaultProvider</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Bestimmt den Standard-CSP für den aktuellen Benutzer oder für den Computer für einen angegebenen Anbietertyp.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft die Parameter ab, die die Vorgänge eines CSP steuern.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Installiert einen zuvor erworbenen <a href="hcryptprov.md"><strong>HCRYPTPROV-Kontext,</strong></a> der als Standardkontext verwendet werden soll.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>CryptReleaseContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt das von der <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext-Funktion erworbene Handle</strong></a> frei.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>CryptSetProvider</strong></a> und <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>CryptSetProviderEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt den Standard-CSP des Benutzers für einen bestimmten CSP-Typ an.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>CryptSetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt Attribute eines CSP an.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>CryptUninstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Entfernt einen Standardkontext, der zuvor von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext installiert wurde.</strong></a></td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>FreeCryptProvFromCertEx</strong></a></td>
<td>Gibt das Handle entweder an einen <a href="/windows/desktop/SecGloss/c-gly"><em>Kryptografiedienstanbieter</em></a> (Cryptographic Service Provider, CSP) oder einen CNG-Schlüssel (Cryptography API: Next Generation) frei.</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>Schlüsselgenerierung und Exchange Funktionen

Schlüsselgenerierungs- und [*Austauschfunktionen tauschen Schlüssel*](../secgloss/e-gly.md) mit anderen Benutzern aus und erstellen, konfigurieren und zerstören [*kryptografische Schlüssel.*](../secgloss/c-gly.md)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>CryptDeriveKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt einen von einem Kennwort abgeleiteten Schlüssel.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>CryptDestroyKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Zerstört einen Schlüssel.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>CryptDuplicateKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Macht eine genaue Kopie eines Schlüssels, einschließlich des <a href="/windows/desktop/SecGloss/s-gly"><em>Zustands</em></a> des Schlüssels.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überträgt einen Schlüssel aus dem CSP in ein <a href="/windows/desktop/SecGloss/k-gly"><em>SchlüsselBLOB</em></a> im Arbeitsspeicher der Anwendung.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt einen zufälligen Schlüssel.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Generiert zufällige Daten.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>CryptGetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft die Parameter eines Schlüssels ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft ein Handle für den Schlüsselaustausch oder Signaturschlüssel ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>CryptImportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überträgt einen Schlüssel aus einem <a href="/windows/desktop/SecGloss/k-gly"><em>SchlüsselBLOB</em></a> an einen CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt die Parameter eines Schlüssels an.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Objektcodierungs- und Decodierungsfunktionen

Dabei handelt es sich um generalisierte Codierungs- und Decodierungsfunktionen. Sie werden zum Codieren und Decodieren von Zertifikaten, [*Zertifikatsperrlisten*](../secgloss/c-gly.md)(Certificate [*Revocation Lists,*](../secgloss/c-gly.md) CRLs), Zertifikatanforderungen und [*Zertifikaterweiterungen*](../secgloss/c-gly.md)verwendet.

| Funktion                                           | BESCHREIBUNG                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Decodiert eine Struktur vom Typ *lpszStructType.*                                                                                                    |
| [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Decodiert eine Struktur vom Typ *lpszStructType.* [**CryptDecodeObjectEx unterstützt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) die Speicherzuordnungsoption mit einem Durchgang. |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Codiert eine Struktur vom Typ *lpszStructType*.                                                                                                    |
| [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Codiert eine Struktur vom Typ *lpszStructType*. [**CryptEncodeObjectEx unterstützt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) die Speicherzuordnungsoption mit einem Durchgang. |



 

### <a name="data-encryption-and-decryption-functions"></a>Datenverschlüsselungs- und Entschlüsselungsfunktionen

Die folgenden Funktionen unterstützen Verschlüsselungs- und Entschlüsselungsvorgänge. [**CryptEncrypt und**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) erfordern einen [*kryptografischen Schlüssel, bevor*](../secgloss/c-gly.md) sie aufgerufen werden. Dies erfolgt mithilfe der [**CryptGenKey-,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) [**CryptDeriveKey-**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)oder [**CryptImportKey-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) Der Verschlüsselungsalgorithmus wird beim Erstellen des Schlüssels angegeben. [**CryptSetKeyParam kann**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) zusätzliche Verschlüsselungsparameter festlegen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>CryptDecrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Entschlüsselt einen Abschnitt von <a href="/windows/desktop/SecGloss/c-gly"><em>Chiffretext mithilfe</em></a> des angegebenen Verschlüsselungsschlüssels.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Verschlüsselt einen Klartextabschnitt <a href="/windows/desktop/SecGloss/p-gly"><em>mithilfe</em></a> des angegebenen Verschlüsselungsschlüssels.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Führt die Verschlüsselung der Daten in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>einer</strong></a> DATA_BLOB aus.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>Verschlüsselt Arbeitsspeicher, um vertrauliche Informationen zu schützen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Führt eine Entschlüsselungs- und Integritätsprüfung der Daten in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>einem</strong></a>DATA_BLOB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>Entschlüsselt Arbeitsspeicher, der mit <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory verschlüsselt wurde.</strong></a></td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Hash- und Digital Signature-Funktionen

Diese Funktionen berechnen [*Datenhashes*](../secgloss/h-gly.md) und erstellen und überprüfen [*auch digitale Signaturen.*](../secgloss/d-gly.md) Hashes werden auch als Nachrichtenhashes bezeichnet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt ein leeres Hashobjekt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>CryptDestroyHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Zerstört ein Hashobjekt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>CryptDuplicateHash</strong></a></td>
<td>Dupliziert ein Hashobjekt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>Ruft einen Hashobjektparameter ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hasht einen Datenblock und fügt ihn dem angegebenen Hashobjekt hinzu.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>CryptHashSessionKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hasht einen Sitzungsschlüssel und fügt ihn dem angegebenen Hashobjekt hinzu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>CryptSetHashParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Legt einen Hashobjektparameter fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>CryptSignHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Signiert das angegebene Hashobjekt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a></td>
<td>Zeigt einen Assistenten an, der ein Dokument oder ein BLOB digital <a href="/windows/desktop/SecGloss/b-gly"><em>signiert.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>CryptUIWizFreeDigitalSignContext</strong></a></td>
<td>Gibt einen Zeiger auf eine <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> frei.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>CryptVerifySignature</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überprüft eine digitale Signatur, wenn ein Handle für das Hashobjekt angegeben wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>PFNCFILTERPROC</strong></a></td>
<td>Filtert die Zertifikate, die im Assistenten für digitale Signaturen angezeigt werden, der von der <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign-Funktion angezeigt</strong></a> wird.</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Certificate and Certificate Store Functions

Zertifikat- und Zertifikatspeicherfunktionen verwalten die Verwendung, speicherung und den Abruf von Zertifikaten, Zertifikatsperrlisten (Certificate [*Revocation Lists,*](../secgloss/c-gly.md) CRLs) und [*Zertifikatvertrauenslisten*](../secgloss/c-gly.md)(Certificate [*Trust Lists,*](../secgloss/c-gly.md) CTLs). Diese Funktionen sind in die folgenden Gruppen unterteilt:

-   Certificate Store Functions
-   Certificate and Certificate Store Maintenance Functions (Wartungsfunktionen für Zertifikat- und Zertifikatzertifikate)
-   Zertifikatfunktionen
-   Funktionen der Zertifikatsperrliste
-   Funktionen der Zertifikatvertrauensliste
-   Erweiterte Eigenschaftenfunktionen
-   MakeCert-Funktionen

### <a name="certificate-store-functions"></a>Certificate Store Functions

Eine Benutzerwebsite kann im Laufe der Zeit viele Zertifikate sammeln. In der Regel verfügt eine Website über Zertifikate für den Benutzer der Website sowie andere Zertifikate, die die Personen und Entitäten beschreiben, mit denen der Benutzer kommuniziert. Für jede Entität kann es mehrere Zertifikate geben. Für jedes einzelne Zertifikat sollte es eine Kette von Überprüfungszertifikaten geben, die einen Rückweg zu einem vertrauenswürdigen [*Stammzertifikat bietet.*](../secgloss/r-gly.md) [*Zertifikatspeicher*](../secgloss/c-gly.md) und die zugehörigen Funktionen bieten Funktionen zum Speichern, Abrufen, Aufzählen, Überprüfen und Verwenden der in den Zertifikaten gespeicherten Informationen.

| Funktion                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Fügt einem Sammlungszertifikatspeicher einen gleichgeordneten Zertifikatspeicher hinzu.                                                                                                                                                                                                                                                                       |
| [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Schließt ein Zertifikatspeicherhand handle.                                                                                                                                                                                                                                                                                                        |
| [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Ermöglicht es einer Anwendung, benachrichtigt zu werden, wenn es einen Unterschied zwischen dem Inhalt eines zwischengespeicherten Speichers und dem Inhalt des Speichers gibt, der im Speicher beibehalten wird. Außerdem bietet sie bei Bedarf eine Desynchronisierung des zwischengespeicherten Speichers und bietet eine Möglichkeit, änderungen, die im zwischengespeicherten Speicher vorgenommen wurden, in den persistenten Speicher zu übertragen.<br/> |
| [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Dupliziert ein Speicherhand handle, indem der [*Verweiszähler erhöht wird.*](../secgloss/r-gly.md)                                                                                                                                                                                            |
| [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Enumeriert die physischen Speicher für einen angegebenen Systemspeicher.                                                                                                                                                                                                                                                                              |
| [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Enumeriert alle verfügbaren Systemspeicher.                                                                                                                                                                                                                                                                                                   |
| [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Enumeriert alle Standorte, die über einen verfügbaren Systemspeicher verfügen.                                                                                                                                                                                                                                                                      |
| [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Ruft eine Store-Eigenschaft ab.                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Öffnet einen Zertifikatspeicher mit einem angegebenen Speicheranbietertyp.                                                                                                                                                                                                                                                                          |
| [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Öffnet einen Systemzertifikatspeicher basierend auf einem Subsystemprotokoll.                                                                                                                                                                                                                                                                           |
| [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Fügt einer Registrierungssystemspeichersammlung einen physischen Speicher hinzu.                                                                                                                                                                                                                                                                              |
| [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Registriert einen Systemspeicher.                                                                                                                                                                                                                                                                                                                 |
| [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Entfernt einen gleichgeordneten Zertifikatspeicher aus einem Sammlungsspeicher.                                                                                                                                                                                                                                                                              |
| [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Speichert den Zertifikatspeicher.                                                                                                                                                                                                                                                                                                              |
| [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Legt eine Store-Eigenschaft fest.                                                                                                                                                                                                                                                                                                                    |
| [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Entfernt einen physischen Speicher aus einer angegebenen Systemspeichersammlung.                                                                                                                                                                                                                                                                        |
| [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Aufheben der Registrierung eines angegebenen Systemspeichers.                                                                                                                                                                                                                                                                                                     |
| [**CryptUIWizExport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Stellt einen Assistenten vor, der ein Zertifikat, eine Zertifikatvertrauensliste (Certificate Trust List, CTL), eine Zertifikatsperrliste (Certificate Revocation List, CRL) oder einen Zertifikatspeicher exportiert.                                                                                                                                                                                                      |
| [**CryptUIWizImport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Stellt einen Assistenten vor, der ein Zertifikat, eine Zertifikatvertrauensliste (Certificate Trust List, CTL), eine Zertifikatsperrliste (Certificate Revocation List, CRL) oder einen Zertifikatspeicher importiert.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Certificate and Certificate Store Maintenance Functions (Wartungsfunktionen für Zertifikat- und Zertifikatzertifikate)

CryptoAPI stellt eine Reihe von allgemeinen Zertifikat- und Zertifikatspeicher-Wartungsfunktionen zur Verfügung.

| Funktion                                                                                                                              | BESCHREIBUNG                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Fügt dem Speicher das serialisierte Zertifikat oder das CRL-Element hinzu.                                   |
| [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Erstellt den angegebenen Kontext aus den codierten Bytes. Der neue Kontext wird nicht in einem Speicher gespeichert. |
| [**CertEnumSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Enumeriert die TrustedSubjects in einem sortierten CTL-Kontext.                                        |
| [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Sucht den angegebenen Betreff in einer CTL.                                                          |
| [**CertFindSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Sucht den angegebenen Betreff in einer sortierten CTL.                                                   |
| [**OpenPersonalTrustDBDialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) und [ **OpenPersonalTrustDBDialogEx**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Zeigt das **Dialogfeld Zertifikate** an.                                                      |



 

### <a name="certificate-functions"></a>Zertifikatfunktionen

Die [*meisten Zertifikatfunktionen*](../secgloss/c-gly.md) verfügen über verwandte Funktionen für den Umgang mit [*CRLs*](../secgloss/c-gly.md) und [*CTLs.*](../secgloss/c-gly.md) Weitere Informationen zu verwandten CRL- und CTL-Funktionen finden Sie unter Certificate Revocation List Functions und Certificate Trust List Functions.

| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Fügt dem Zertifikatspeicher einen Zertifikatkontext hinzu.                                                                                                                                                                                            |
| [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Fügt einem Zertifikatkontext in einem anderen Speicher einen Link in einem Zertifikatspeicher hinzu.                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Konvertiert das codierte Zertifikat in einen Zertifikatkontext und fügt den Kontext dann dem Zertifikatspeicher hinzu.                                                                                                                                  |
| [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Erhöht die Verweisanzahl für ein **HCERT \_ SERVER \_ OCSP \_ RESPONSE-Handle.**                                                                                                                                                                 |
| [**CertAddRefServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Erhöht die Verweisanzahl für eine [**\_ \_ OCSP \_ RESPONSE \_ CONTEXT-Struktur von CERT SERVER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context)                                                                                                              |
| [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Schließt ein OSP-Serverantworthand handle (Online [*Certificate Status Protocol).*](../secgloss/o-gly.md)                                               |
| [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Erstellt einen Zertifikatkontext aus einem codierten Zertifikat. Der erstellte Kontext wird nicht in einem Zertifikatspeicher gespeichert.                                                                                                                               |
| [**CertCreateSelfSignCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | Erstellen eines selbstsignierten Zertifikats                                                                                                                                                                                                              |
| [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Löscht ein Zertifikat aus dem Zertifikatspeicher.                                                                                                                                                                                               |
| [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Dupliziert einen Zertifikatkontext, indem die [*Verweisanzahl erhöht wird.*](../secgloss/r-gly.md)                                                                                           |
| [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Enumeriert die Zertifikatkontexte im Zertifikatspeicher.                                                                                                                                                                                   |
| [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Sucht den ersten oder nächsten Zertifikatkontext im Zertifikatspeicher, der ein Suchkriterium erfüllt.                                                                                                                                           |
| [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Gibt einen Zertifikatkontext frei.                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Ruft einen Zertifikatkontext aus dem Zertifikatspeicher für den ersten oder nächsten Aussteller des angegebenen Zertifikats des Betreffs ab.                                                                                                                      |
| [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Ruft einen nicht blockierenden, zeit gültigen OCSP-Antwortkontext [*(Online Certificate Status Protocol)*](../secgloss/o-gly.md) für das angegebene Handle ab. |
| [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Ruft aus dem Zertifikatspeicher den Zertifikatkontext des Betreffs ab, der durch seinen Aussteller und seine Seriennummer eindeutig identifiziert wird.                                                                                                                  |
| [**CertGetValidUsages**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Gibt ein Array von Verwendungen zurück, das aus der Schnittmenge der gültigen Verwendungen für alle Zertifikate in einem Array von Zertifikaten besteht.                                                                                                               |
| [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Öffnet ein Handle für eine OCSP-Antwort [*(Online Certificate Status Protocol),*](../secgloss/o-gly.md) die einer Serverzertifikatkette zugeordnet ist.       |
| [**CertRetrimetricLogoOrBiometricInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Führt einen URL-Abruf von Logo- oder biometrischen Informationen aus, die in der **Zertifikaterweiterung szOID \_ LOGOTYPE \_ EXT** oder **szOID \_ BIOMETRIC \_ EXT** angegeben sind.                                                                                  |
| [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Zeigt ein Dialogfeld an, in dem der Benutzer Zertifikate aus einer Gruppe von Zertifikaten auswählen kann, die einem bestimmten Kriterium entsprechen.                                                                                                                       |
| [**CertSelectCertificateChains**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Ruft Zertifikatketten basierend auf angegebenen Auswahlkriterien ab.                                                                                                                                                                             |
| [**CertSelectionGetSerializedBlob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Eine Hilfsfunktion, die verwendet wird, um ein serialisiertes [*ZertifikatBLOB*](../secgloss/b-gly.md) aus einer [**CERT \_ SELECTUI \_ INPUT-Struktur**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input) abzurufen.                                               |
| [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Serialisiert das codierte Zertifikat eines Zertifikatkontexts und eine codierte Darstellung seiner Eigenschaften.                                                                                                                                         |
| [**CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Führt die aktivierten Überprüfungsprüfungen für das Zertifikat des Betreffs mithilfe des Ausstellers durch.                                                                                                                                                           |
| [**CryptUIDlgCertMgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Zeigt ein Dialogfeld an, in dem der Benutzer Zertifikate verwalten kann.                                                                                                                                                                              |
| [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)                   | Zeigt ein Dialogfeld an, in dem ein Benutzer ein Zertifikat auswählen kann.                                                                                                                                                                               |
| [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Zeigt ein Dialogfeld an, das die Auswahl eines Zertifikats aus einem angegebenen Speicher ermöglicht.                                                                                                                                                        |
| [**CryptUIDlgViewCertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Zeigt ein Dialogfeld an, in dem ein angegebenes Zertifikat angezeigt wird.                                                                                                                                                                                    |
| [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Zeigt ein Zertifikat, eine Zertifikatsperrliste oder eine Zertifikatsperrliste an.                                                                                                                                                                                                            |
| [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)                         | Zeigt ein Dialogfeld an, das die Signaturinformationen für eine signierte Nachricht enthält.                                                                                                                                                                |
| [**GetFriendlyNameOfCert**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Ruft den Anzeigenamen für ein Zertifikat ab.                                                                                                                                                                                                   |
| [**RKeyCloseKeyService**](rkeyclosekeyservice.md)                                   | Schließt ein Schlüsseldiensthandle.                                                                                                                                                                                                                    |
| [**RKeyOpenKeyService**](rkeyopenkeyservice.md)                                     | Öffnet ein Schlüsseldiensthandle auf einem Remotecomputer.                                                                                                                                                                                                |
| [**RKeyPFXInstall**](rkeypfxinstall.md)                                             | Installiert ein Zertifikat auf einem Remotecomputer.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Funktionen der Zertifikatsperrliste

Diese Funktionen verwalten das Speichern und Abrufen von [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation Lists, CRLs).

| Funktion                                                             | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Fügt dem Zertifikatspeicher einen CRL-Kontext hinzu.                                                                                                                                          |
| [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Fügt einem CRL-Kontext in einem anderen Speicher einen Link in einem Speicher hinzu.                                                                                                                         |
| [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Konvertiert die codierte Zertifikatsperrliste in einen Zertifikatsperrlistenkontext und fügt dann den Kontext dem Zertifikatspeicher hinzu.                                                                                        |
| [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Erstellt einen Zertifikatsperrlistenkontext aus einer codierten Zertifikatsperrliste. Der erstellte Kontext wird nicht in einem Zertifikatspeicher gespeichert.                                                                                     |
| [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Löscht eine Zertifikatsperrliste aus dem Zertifikatspeicher.                                                                                                                                             |
| [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Dupliziert einen CRL-Kontext, indem der [*Verweiszähler*](../secgloss/r-gly.md)erhöht wird.                                         |
| [**CertEnumCRLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Listet die CRL-Kontexte in einem Speicher auf.                                                                                                                                               |
| [**CertFindCertificateInCRL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Durchsucht die [*Zertifikatsperrliste*](../secgloss/c-gly.md) (Certificate Revocation List, CRL) nach dem angegebenen Zertifikat. |
| [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Sucht den ersten oder nächsten CRL-Kontext im Zertifikatspeicher, der einem bestimmten Kriterium entspricht.                                                                                     |
| [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Gibt einen CRL-Kontext frei.                                                                                                                                                                  |
| [**CertGetCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Ruft den ersten oder nächsten CRL-Kontext aus dem Zertifikatspeicher für das angegebene Ausstellerzertifikat ab.                                                                                 |
| [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Serialisiert die codierte Zertifikatsperrliste des Zertifikatsperrlistenkontexts und ihre Eigenschaften.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Zertifikatvertrauenslistenfunktionen

Diese Funktionen verwalten das Speichern und Abrufen von [*Zertifikatvertrauenslisten*](../secgloss/c-gly.md) (Certificate Trust Lists, CTLs).

| Funktion                                                               | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Fügt dem Zertifikatspeicher einen CTL-Kontext hinzu.                                                                         |
| [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Fügt einem CRL-Kontext in einem anderen Speicher einen Link in einem Speicher hinzu.                                                        |
| [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Konvertiert die codierte CTL in einen CTL-Kontext und fügt dann den Kontext zum Zertifikatspeicher hinzu.                       |
| [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Erstellt einen CTL-Kontext aus einer codierten Zertifikatvertrauensliste. Der erstellte Kontext wird nicht in einem Zertifikatspeicher gespeichert. |
| [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Löscht eine CTL aus dem Zertifikatspeicher.                                                                            |
| [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Dupliziert einen CTL-Kontext, indem der Verweiszähler erhöht wird.                                                        |
| [**CertEnumCTLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Listet die CTL-Kontexte im Zertifikatspeicher auf.                                                                |
| [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Sucht den ersten oder nächsten CTL-Kontext im Zertifikatspeicher, der einem bestimmten Kriterium entspricht.                     |
| [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Gibt einen CTL-Kontext frei.                                                                                                 |
| [**CertModifyCertificatesToTrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Ändert den Satz von Zertifikaten in einer Zertifikatvertrauensliste für einen bestimmten Zweck.                                                       |
| [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Serialisiert die codierte CTL des CTL-Kontexts und seine Eigenschaften.                                                         |



 

### <a name="extended-property-functions"></a>Erweiterte Eigenschaftenfunktionen

Die folgenden Funktionen funktionieren mit erweiterten Eigenschaften von Zertifikaten, CRLs und CTLs.

| Funktion                                                                             | BESCHREIBUNG                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Listet die Eigenschaften für den angegebenen Zertifikatkontext auf. |
| [**CertEnumCRLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Listet die Eigenschaften für den angegebenen CRL-Kontext auf.         |
| [**CertEnumCTLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Listet die Eigenschaften für den angegebenen CTL-Kontext auf.         |
| [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Ruft Zertifikateigenschaften ab.                                |
| [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Ruft CRL-Eigenschaften ab.                                        |
| [**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Ruft CTL-Eigenschaften ab.                                        |
| [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Legt Zertifikateigenschaften fest.                                     |
| [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Legt CRL-Eigenschaften fest.                                             |
| [**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Legt CTL-Eigenschaften fest.                                             |



 

## <a name="makecert-functions"></a>MakeCert-Funktionen

Die folgenden Funktionen unterstützen das [MakeCert-Tool.](makecert.md)



| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCryptProvFromCert**](freecryptprovfromcert.md)                                 | Gibt das Handle an einen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) frei und löscht optional den temporären Container, der von der [**GetCryptProvFromCert-Funktion**](getcryptprovfromcert.md) erstellt wurde. |
| [**GetCryptProvFromCert**](getcryptprovfromcert.md)                                   | Ruft ein Handle für einen CSP und eine Schlüsselspezifikation für einen Zertifikatkontext ab.                                                                                                                                                                                                                                |
| [**PvkFreeCryptProv**](pvkfreecryptprov.md)                                           | Gibt das Handle für einen CSP frei und löscht optional den temporären Container, der von der [**PvkGetCryptProv-Funktion**](pvkgetcryptprov.md) erstellt wurde.                                                                                                                                                          |
| [**PvkGetCryptProv**](pvkgetcryptprov.md)                                             | Ruft ein Handle für einen CSP basierend auf einem Dateinamen des [*privaten Schlüssels*](../secgloss/p-gly.md) oder einem Schlüsselcontainernamen ab.                                                                                                                                          |
| [**PvkPrivateKeyAcquireContextFromMemory**](pvkprivatekeyacquirecontextfrommemory.md) | Erstellt einen temporären Container im CSP und lädt einen privaten Schlüssel aus dem Arbeitsspeicher in den Container.                                                                                                                                                                                                         |
| [**PvkPrivateKeySave**](pvkprivatekeysave.md)                                         | Speichert einen privaten Schlüssel und den entsprechenden [*öffentlichen Schlüssel*](../secgloss/p-gly.md) in einer angegebenen Datei.                                                                                                                                                          |
| [**SignError**](signerror.md)                                                         | Ruft [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf und konvertiert den Rückgabecode in ein **HRESULT.**                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Zertifikatüberprüfungsfunktionen

Zertifikate werden mithilfe von [*CTLs*](../secgloss/c-gly.md) oder Zertifikatketten überprüft. Funktionen werden für diese beiden Funktionen bereitgestellt:

-   Überprüfungsfunktionen mit CTLs
-   Überprüfungsfunktionen der Zertifikatkette

### <a name="verification-functions-using-ctls"></a>Überprüfungsfunktionen mit CTLs

Diese Funktionen verwenden CTLs im Überprüfungsprozess. Weitere Funktionen zum Arbeiten mit CTLs finden Sie unter Certificate Trust List Functions und Extended Property Functions.

Die folgenden Funktionen verwenden CTLs direkt für die Überprüfung.

| Funktion                                                         | BESCHREIBUNG                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Überprüft die Verwendung einer CTL.                 |
| [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Codiert und signiert eine CTL als Nachricht.        |
| [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Ruft eine CTL aus einer Nachricht ab und überprüft sie. |
| [**CryptMsgSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Signiert eine Nachricht, die eine CTL enthält.         |



 

### <a name="certificate-chain-verification-functions"></a>Überprüfungsfunktionen der Zertifikatkette

Zertifikatketten werden erstellt, um Vertrauensinformationen zu einzelnen Zertifikaten bereitzustellen.

| Funktionsname                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Erstellt eine neue, nicht standardmäßige Ketten-Engine für eine Anwendung.                                                                                                                                                          |
| [**CertCreateCTLEntryFromCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Erstellt einen CTL-Eintrag, dessen Attribute die Eigenschaften des Zertifikatkontexts sind.                                                                                                                                      |
| [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Dupliziert eine Zertifikatkette, indem der [*Verweiszähler*](../secgloss/r-gly.md) der Kette erhöht und ein Zeiger auf die Kette zurückgegeben wird.                    |
| [**CertFindChainInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Sucht den ersten oder nächsten Zertifikatkettenkontext in einem Speicher.                                                                                                                                                     |
| [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Gibt eine Zertifikatkette frei, indem derEn Verweiszähler reduziert wird.                                                                                                                                                          |
| [**CertFreeCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Gibt eine nicht standardmäßige Zertifikatketten-Engine frei.                                                                                                                                                                        |
| [**CertFreeCertificateChainList**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Gibt das Array von Zeigern frei, um Kontexte zu verketten.                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Erstellt einen Kettenkontext, der von einem Endzertifikat aus beginnt und nach Möglichkeit zu einem vertrauenswürdigen [*Stammzertifikat*](../secgloss/r-gly.md)zurückgeht.                |
| [**CertIsValidCRLForCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Überprüft eine [*Zertifikatsperrliste,*](../secgloss/c-gly.md) um zu ermitteln, ob sie ein bestimmtes Zertifikat enthalten würde, wenn dieses Zertifikat widerrufen würde. |
| [**CertSetCertificateContextPropertiesFromCTLEntry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Legt Eigenschaften für den Zertifikatkontext mithilfe der Attribute im CTL-Eintrag fest.                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Überprüft eine Zertifikatkette, um ihre Gültigkeit zu überprüfen, einschließlich der Konformität mit den angegebenen Gültigkeitsrichtlinienkriterien.                                                                                            |



 

## <a name="message-functions"></a>Nachrichtenfunktionen

[*CryptoAPI-Nachrichtenfunktionen*](../secgloss/c-gly.md) bestehen aus zwei Gruppen von Funktionen: Nachrichtenfunktionen auf niedriger Ebene und [*vereinfachte Nachrichtenfunktionen.*](../secgloss/s-gly.md)

Nachrichtenfunktionen auf niedriger Ebene erstellen und arbeiten direkt mit PKCS \# 7-Nachrichten. Diese Funktionen codieren PKCS \# 7-Daten für die Übertragung und decodieren empfangene PKCS \# 7-Daten. Außerdem werden die Signaturen empfangener Nachrichten entschlüsselt und überprüft. Eine Übersicht über die \# PKCS 7-Standardnachrichten und -Meldungen auf niedriger Ebene finden Sie unter [Low-level Messages (Meldungen auf niedriger Ebene).](low-level-messages.md)

Vereinfachte Nachrichtenfunktionen befinden sich auf einer höheren Ebene und umschließen mehrere Nachrichtenfunktionen und Zertifikatfunktionen auf niedriger Ebene in einzelne Funktionen, die eine bestimmte Aufgabe auf eine bestimmte Weise ausführen. Diese Funktionen reduzieren die Anzahl der Funktionsaufrufe, die zum Ausführen einer Aufgabe erforderlich sind, wodurch die CryptoAPI-Verwendung vereinfacht wird. Eine Übersicht über vereinfachte Nachrichten finden Sie unter [Vereinfachte Nachrichten.](simplified-messages.md)

-   Nachrichtenfunktionen auf niedriger Ebene
-   Vereinfachte Nachrichtenfunktionen

### <a name="low-level-message-functions"></a>Nachrichtenfunktionen auf niedriger Ebene

Nachrichtenfunktionen auf niedriger Ebene stellen die Funktionen bereit, die zum Codieren von Daten für die Übertragung und zum Decodieren empfangener PKCS \# 7-Nachrichten erforderlich sind. Funktionen werden auch bereitgestellt, um die Signaturen empfangener Nachrichten zu entschlüsseln und zu überprüfen. Die Verwendung dieser Nachrichtenfunktionen auf niedriger Ebene in den meisten Anwendungen wird nicht empfohlen. Für die meisten Anwendungen wird die Verwendung von vereinfachten Nachrichtenfunktionen bevorzugt, die mehrere Nachrichtenfunktionen auf niedriger Ebene in einen einzelnen Funktionsaufruf umschließen.

| Funktion                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Berechnet die Länge einer codierten kryptografischen Nachricht.                                                                                                                                                                     |
| [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Schließt ein Handle einer kryptografischen Nachricht.                                                                                                                                                                                    |
| [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Führt eine spezielle Steuerelementfunktion nach dem endgültigen [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einer codierten oder decodierten kryptografischen Nachricht aus.                                                                                   |
| [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Weist eine bereits vorhandene Signatur in einer Nachricht gegen.                                                                                                                                                                       |
| [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Signiert eine bereits vorhandene Signatur (codierte SignerInfo, wie in PKCS \# 7 definiert).                                                                                                                                       |
| [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Dupliziert ein kryptografisches Nachrichtenhandle, indem der [*Verweiszähler*](../secgloss/r-gly.md)erhöht wird. Mit dem Verweiszähler wird die Lebensdauer der Nachricht nachverfolgt. |
| [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Übernimmt einen Parameter nach dem Codieren oder Decodieren einer kryptografischen Nachricht.                                                                                                                                                       |
| [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Öffnet eine kryptografische Nachricht für die Decodierung.                                                                                                                                                                                    |
| [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Öffnet eine kryptografische Nachricht für die Codierung.                                                                                                                                                                                    |
| [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Aktualisiert den Inhalt einer kryptografischen Nachricht.                                                                                                                                                                               |
| [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Überprüft eine [*Gegensignatur*](../secgloss/c-gly.md) in Bezug auf die SignerInfo-Struktur (wie durch PKCS \# 7 definiert).                                                   |
| [**CryptMsgVerifyCountersignatureEncodedEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Überprüft, ob der *pbSignerInfoCounterSignature-Parameter* den verschlüsselten Hash des **felds encryptedDigest** der *pbSignerInfo-Parameterstruktur* enthält. [](../secgloss/h-gly.md)   |



 

### <a name="simplified-message-functions"></a>Vereinfachte Nachrichtenfunktionen

[*Vereinfachte Nachrichtenfunktionen umschließen*](../secgloss/s-gly.md) Nachrichtenfunktionen auf niedriger Ebene in eine einzelne Funktion, um eine angegebene Aufgabe auszuführen.

| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Decodiert eine kryptografische Nachricht.                                                                                                                                                                                                                                             |
| [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Entschlüsselt die angegebene Meldung und überprüft den Signator.                                                                                                                                                                                                                     |
| [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Entschlüsselt die angegebene Meldung.                                                                                                                                                                                                                                              |
| [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Verschlüsselt die Nachricht für den Empfänger oder empfänger.                                                                                                                                                                                                                        |
| [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Gibt den [*Zertifikatspeicher zurück,*](../secgloss/c-gly.md) der die Zertifikate und CRLs der [*Nachricht enthält.*](../secgloss/c-gly.md) |
| [**CryptGetMessageSignerCount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Gibt die Anzahl der Signierer in der signierten Nachricht zurück.                                                                                                                                                                                                                          |
| [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Erstellt einen Hash der Nachricht.                                                                                                                                                                                                                                               |
| [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Signiert die Nachricht und verschlüsselt sie dann für den Empfänger oder die Empfänger.                                                                                                                                                                                                     |
| [**CryptSignMessageWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Signiert eine Nachricht mithilfe des privaten Schlüssels eines CSP, der in den Parametern für die Funktion angegeben ist.                                                                                                                                                                                       |
| [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Signiert die Nachricht.                                                                                                                                                                                                                                                           |
| [**CryptVerifyDetachedMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Überprüft eine Hashnachricht, die einen getrennten Hash enthält.                                                                                                                                                                                                                     |
| [**CryptVerifyDetachedMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Überprüft eine signierte Nachricht, die eine getrennte Signatur oder Signaturen enthält.                                                                                                                                                                                                  |
| [**CryptVerifyMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Überprüft eine Hashnachricht.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Überprüft eine signierte Nachricht.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignatureWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Überprüft die Signatur einer signierten Nachricht mithilfe der angegebenen Öffentlichen Schlüsselinformationen.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Zusatzfunktionen

Die Hilfsfunktionen sind wie folgt gruppiert:

-   Datenverwaltung Funktionen
-   Datenkonvertierungsfunktionen
-   Erweiterte Schlüsselverwendungsfunktionen
-   Schlüsselbezeichnerfunktionen
-   OID-Unterstützungsfunktionen
-   Remote Object Retrieval Functions
-   PFX-Funktionen

### <a name="data-management-functions"></a>Datenverwaltung Funktionen

Die folgenden CryptoAPI-Funktionen verwalten Daten und Zertifikate.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>CertCompareCertificate</strong></a></td>
<td>Vergleicht zwei Zertifikate, um zu bestimmen, ob sie identisch sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>CertCompareCertificateName</strong></a></td>
<td>Vergleicht zwei Zertifikatnamen, um zu bestimmen, ob sie identisch sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>CertCompareIntegerBlob</strong></a></td>
<td>Vergleicht zwei <a href="/windows/desktop/SecGloss/b-gly"><em>ganzzahlige BLOBs.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>CertComparePublicKeyInfo</strong></a></td>
<td>Vergleicht zwei <a href="/windows/desktop/SecGloss/p-gly"><em>öffentliche Schlüssel,</em></a> um zu bestimmen, ob sie identisch sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>CertFindAttribute</strong></a></td>
<td>Sucht das erste Attribut, das durch seinen <a href="/windows/desktop/SecGloss/o-gly"><em>Objektbezeichner</em></a> (OID) identifiziert wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>CertFindExtension</strong></a></td>
<td>Sucht die erste erweiterung, die durch ihre OID identifiziert wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>CertFindRDNAttr</strong></a></td>
<td>Sucht das erste <a href="/windows/desktop/SecGloss/r-gly"><em>RDN-Attribut,</em></a> das durch seine OID in der Namensliste des <em>relativen Distinguished Names identifiziert wird.</em></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>CertGetIntendedKeyUsage</strong></a></td>
<td>Übernimmt die beabsichtigten Schlüsselverwendungsbytes aus dem Zertifikat.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>CertGetPublicKeyLength</strong></a></td>
<td>Übernimmt die Bitlänge des öffentlichen/privaten Schlüssels aus dem <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB des öffentlichen Schlüssels.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>CertIsRDNAttrsInCertificateName</strong></a></td>
<td>Vergleicht die Attribute im <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifikatnamen</em></a> <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong></strong></a> mit dem angegebenen CERT_RDN, um zu bestimmen, ob alle Attribute dort enthalten sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>CertIsStrongHashToSign</strong></a></td>
<td>Bestimmt, ob der angegebene Hashalgorithmus und der öffentliche Schlüssel im Signaturzertifikat verwendet werden können, um starke Signierung durchzuführen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>CertVerifyCRLRevocation</strong></a></td>
<td>Überprüft, ob das Zertifikat des Betreffs nicht in der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifikatsperrliste</em></a> (Certificate Revocation List, CRL) enthalten ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>CertVerifyCRLTimeValidity</strong></a></td>
<td>Überprüft die Zeitgültigkeit einer Zertifikatsperrliste.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>CertVerifyRevocation</strong></a></td>
<td>Überprüft, ob sich das Zertifikat des Betreffs nicht in der Zertifikatsperrliste befindet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>CertVerifyTimeValidity</strong></a></td>
<td>Überprüft die Gültigkeitsdauer eines Zertifikats.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>CertVerifyValidityNesting</strong></a></td>
<td>Überprüft, ob die Gültigkeitsdauer des Subjekts innerhalb der Gültigkeitsdauer des Ausstellers geschachtelt ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Diese Funktion wird durch die <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex-Funktion</strong></a> ersetzt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Exportiert den privaten Schlüssel im PKCS-#8 Format.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>Exportiert die Informationen zum öffentlichen Schlüssel, die dem entsprechenden privaten Schlüssel des Anbieters zugeordnet sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>CryptExportPublicKeyInfoEx</strong></a></td>
<td>Exportiert die Informationen zum öffentlichen Schlüssel, die dem entsprechenden privaten Schlüssel des Anbieters zugeordnet sind. Diese Funktion unterscheidet sich von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> dadurch, dass der Benutzer den Algorithmus für öffentliche Schlüssel angeben kann, wodurch der vom CSP bereitgestellte Standardwert überschrieben wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>CryptExportPublicKeyInfoFromBCryptKeyHandle</strong></a></td>
<td>Exportiert die Informationen zum öffentlichen Schlüssel, die dem entsprechenden privaten Schlüssel eines Anbieters zugeordnet sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>CryptFindCertificateKeyProvInfo</strong></a></td>
<td>Enumeriert die Kryptografieanbieter und ihre Schlüsselcontainer, um den privaten Schlüssel zu finden, der dem öffentlichen Schlüssel eines Zertifikats entspricht. <a href="/windows/desktop/SecGloss/k-gly"><em></em></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>CryptFindLocalizedName</strong></a></td>
<td>Sucht den lokalisierten Namen für einen angegebenen Namen, z. B. sucht den lokalisierten Namen für den Speichernamen des Stammsystems.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>CryptHashCertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hashes des codierten Inhalts.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Hashes eines Datenblocks mithilfe eines CNG-Hashanbieters (Cryptography API: Next Generation).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>CryptHashPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Berechnet den Hash der codierten Informationen des öffentlichen Schlüssels.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>CryptHashToBeSigned</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Berechnet den Hash der &quot; zu signierten &quot; Informationen im codierten signierten Inhalt (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Importiert den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a> im PKCS-#8-Format in einen <a href="/windows/desktop/SecGloss/c-gly"><em>Kryptografiedienstanbieter (Cryptographic Service Provider,</em></a> CSP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Konvertiert und importiert Informationen zu öffentlichen Schlüsseln in den Anbieter und gibt ein Handle des öffentlichen Schlüssels zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Konvertiert und importiert die Informationen des öffentlichen Schlüssels in den Anbieter und gibt ein Handle des öffentlichen Schlüssels zurück. Zusätzliche Parameter (über die von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a>angegebenen), die zum Überschreiben von Standardwerten verwendet werden können, werden bereitgestellt, um <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>zu ergänzen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Importiert einen öffentlichen Schlüssel in einen asymmetrischen CNG-Anbieter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a></td>
<td>Belegt Arbeitsspeicher für einen Puffer. Dieser Arbeitsspeicher wird von allen Crypt32.lib-Funktionen verwendet, die zugeordnete Puffer zurückgeben.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>CryptMemFree</strong></a></td>
<td>Gibt von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a> oder <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a>belegten Arbeitsspeicher frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a></td>
<td>Gibt Arbeitsspeicher frei, der derzeit für einen Puffer zugeordnet ist, und belegt Arbeitsspeicher für einen neuen Puffer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft Informationen zum Inhalt eines BLOB oder einer Datei ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>Codiert die &quot; zu signierten &quot; Informationen, signiert diese codierten Informationen und codiert die resultierenden signierten, codierten Informationen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>CryptSignCertificate</strong></a></td>
<td>Signiert die &quot; zu signierten &quot; Informationen im codierten, signierten Inhalt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a></td>
<td>Fügt ein Subject Interface Package (SIP) hinzu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>CryptSIPCreateIndirectData</strong></a></td>
<td>Gibt eine <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA-Struktur</strong></a> zurück, die einen <a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> der angegebenen <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a> Struktur, den Digestalgorithmus und ein Codierungsattribut enthält. Der Hash kann als indirekter Verweis auf die Daten verwendet werden.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>CryptSIPGetCaps</strong></a></td>
<td>Ruft die Funktionen eines SIP ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>CryptSIPGetSignedDataMsg</strong></a></td>
<td>Ruft eine Authenticode-Signatur aus der Datei ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>CryptSIPLoad</strong></a></td>
<td>Lädt die Dynamic Link Library, die ein Antragstellerschnittstellenpaket implementiert und einer <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> Struktur entsprechende Bibliotheksexportfunktionen zuweist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>CryptSIPPutSignedDataMsg</strong></a></td>
<td>Speichert eine Authenticode Signature in der Zieldatei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>CryptSIPRemoveProvider</strong></a></td>
<td>Entfernt ein durch einen vorherigen Aufruf der <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider-Funktion hinzugefügtes</strong></a> SIP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>CryptSIPRemoveSignedDataMsg</strong></a></td>
<td>Entfernt eine angegebene Authenticode-Signatur.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>CryptSIPRetrieveSubjectGuid</strong></a></td>
<td>Ruft eine GUID basierend auf den Headerinformationen in einer angegebenen Datei ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>CryptSIPRetrieveSubjectGuidForCatalogFile</strong></a></td>
<td>Ruft die der angegebenen Datei zugeordnete Antragsteller-GUID ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>CryptSIPVerifyIndirectData</strong></a></td>
<td>Überprüft die indirekten Hashdaten anhand des angegebenen Antragstellers.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>CryptUpdateProtectedState</strong></a></td>
<td>Migriert die Hauptschlüssel des aktuellen Benutzers, nachdem sich die <a href="/windows/desktop/SecGloss/s-gly"><em>Sicherheits-ID</em></a> (SID) des Benutzers geändert hat.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a></td>
<td>Überprüft die Signatur eines Antragstellerzertifikats oder einer <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifikatsperrliste</em></a> mithilfe der Informationen zum öffentlichen Schlüssel.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>CryptVerifyCertificateSignatureEx</strong></a></td>
<td>Eine erweiterte Version von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>GetEncSChannel</strong></a></td>
<td>Speichert den verschlüsselten Inhalt der Schannel-DLL im Arbeitsspeicher.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pCryptSIPGetCaps</strong></a></td>
<td>Wird von einem SIP implementiert, um Funktionen zu melden.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Datenkonvertierungsfunktionen

Die folgenden CryptoAPI-Funktionen konvertieren Zertifikatstrukturmember in verschiedene Formen.

| Funktion                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAlgIdToOID**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Konvertiert einen CryptoAPI-Algorithmusbezeichner \_ (ALG-ID) in eine ASN.1-Objektbezeichnerzeichenfolge [*(Abstract Syntax Notation One).*](../secgloss/a-gly.md) [](../secgloss/o-gly.md) |
| [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Übernimmt den Antragsteller- oder Ausstellernamen aus einem Zertifikat und konvertiert ihn in eine auf NULL endende Zeichenfolge.                                                                                                                                                                                                               |
| [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Konvertiert ein [*Zertifikatnamen-BLOB*](../secgloss/b-gly.md) in eine auf null endende Zeichenfolge.                                                                                                                                                                                                      |
| [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Konvertiert die ASN.1-Objektbezeichnerzeichenfolge in den CSP-Algorithmusbezeichner.                                                                                                                                                                                                                                                 |
| [**CertRDNValueToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Konvertiert einen Namenswert in eine auf NULL endende Zeichenfolge.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Konvertiert eine auf NULL endende [*X.500-Zeichenfolge*](../secgloss/x-gly.md) in einen codierten Zertifikatnamen.                                                                                                                                                                                          |
| [**CryptBinaryToString**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Konvertiert eine binäre Sequenz in eine formatierte Zeichenfolge.                                                                                                                                                                                                                                                                          |
| [**CryptFormatObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Formatiert codierte Daten und gibt eine Unicode-Zeichenfolge zurück.                                                                                                                                                                                                                                                                          |
| [**CryptStringToBinary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Konvertiert eine formatierte Zeichenfolge in eine binäre Sequenz.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Erweiterte Schlüsselverwendungsfunktionen

Die folgenden Funktionen befassen sich mit der [*Erweiterten Schlüsselverwendungserweiterung*](../secgloss/e-gly.md) (Enhanced Key Usage, EKU) und der erweiterten EKU-Eigenschaft von Zertifikaten. Die EKU-Erweiterung und die erweiterte Eigenschaft geben die gültige Verwendung eines Zertifikats an und schränken sie ein. Die Erweiterungen sind Teil des Zertifikats selbst. Sie werden vom Aussteller des Zertifikats festgelegt und sind schreibgeschützt. Eigenschaften mit erweiterten Zertifikaten sind Werte, die einem Zertifikat zugeordnet sind und in einer Anwendung festgelegt werden können.

| Funktion                                                                             | BESCHREIBUNG                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CertAddEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Fügt der EKU-Eigenschaft eines Zertifikats einen Nutzungsbezeichner hinzu.                       |
| [**CertGetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Übernimmt aus einem Zertifikat Informationen zur EKU-Erweiterung oder -Eigenschaft. |
| [**CertRemoveEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Entfernt den Nutzungsbezeichner aus der erweiterten EKU-Eigenschaft eines Zertifikats.       |
| [**CertSetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Legt die EKU-Eigenschaft für ein Zertifikat fest.                                       |



 

### <a name="key-identifier-functions"></a>Schlüsselbezeichnerfunktionen

Schlüsselbezeichnerfunktionen ermöglichen dem Benutzer das Erstellen, Festlegen, Abrufen oder Suchen eines Schlüsselbezeichners oder seiner Eigenschaften.

Ein Schlüsselbezeichner ist der eindeutige Bezeichner eines [*öffentlichen/privaten Schlüsselpaars.*](../secgloss/p-gly.md) Es kann ein beliebiger eindeutiger Bezeichner sein, ist aber in der Regel der 20-Byte-SHA1-Hash einer codierten [**CERT \_ PUBLIC KEY \_ \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) Ein Schlüsselbezeichner kann über die CERT KEY IDENTIFIER PROP ID des \_ \_ \_ Zertifikats \_ ermittelt werden. Der Schlüsselbezeichner ermöglicht die Verwendung dieses [*Schlüsselpaars*](../secgloss/k-gly.md) zum Verschlüsseln oder Entschlüsseln von Nachrichten ohne Verwendung des Zertifikats.

Schlüsselbezeichner sind nicht [*CRLs oder*](../secgloss/c-gly.md) [*CTLs zugeordnet.*](../secgloss/c-gly.md)

Ein Schlüsselbezeichner kann die gleichen Eigenschaften wie ein Zertifikatkontext aufweisen. Weitere Informationen finden Sie unter [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>CryptCreateKeyIdentifierFromCSP</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt einen Schlüsselbezeichner aus dem öffentlichen <a href="/windows/desktop/SecGloss/p-gly"><em>Schlüsselblob eines CSP.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>CryptEnumKeyIdentifierProperties</strong></a></td>
<td>Enumeriert Schlüsselbezeichner und deren Eigenschaften.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>CryptGetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Übernimmt eine bestimmte Eigenschaft aus einem angegebenen Schlüsselbezeichner.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>CryptSetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollte mit der Verwendung <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Legt eine Eigenschaft eines angegebenen Schlüsselbezeichners fest.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>OID-Unterstützungsfunktionen

Diese Funktionen bieten [*Unterstützung für Objektbezeichner*](../secgloss/o-gly.md) (Object Identifier, OID). Diese Funktionen installieren, registrieren und werden an OID- und Codierungstyp-spezifische Funktionen versendet.

Die folgenden CryptoAPI-Funktionen verwenden diese OID-Unterstützungsfunktionen:

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Eine Übersicht über diesen Prozess finden Sie unter [Erweitern der CryptoAPI-Funktionalität.](extending-cryptoapi-functionality.md)

Die folgenden Funktionen funktionieren mit OIDs.

| Funktion                                                                       | BESCHREIBUNG                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Listet die registrierten OID-Funktionen auf, die durch ihren Codierungstyp, Funktionsnamen und OID identifiziert werden.                                                                                                                 |
| [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Listet die registrierten OID-Informationen auf, die von ihrer Gruppe identifiziert werden, und ruft *pfnEnumOIDInfo* für Übereinstimmungen auf.                                                                                                       |
| [**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Verwendet den angegebenen Schlüssel und die angegebene Gruppe, um nach OID-Informationen zu suchen.                                                                                                                                                          |
| [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Gibt die Handleanzahl frei, die von [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) oder [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)erhöht und zurückgegeben wurde. |
| [**CryptGetDefaultOIDDllList**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Übernimmt die Liste der registrierten DLL-Standardeinträge für den angegebenen Funktionssatz und Codierungstyp.                                                                                                              |
| [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Übernimmt entweder die erste oder die nächste installierte Standardfunktion oder lädt die DLL, die die Standardfunktion enthält.                                                                                                 |
| [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Durchsucht die Liste der installierten Funktionen nach einem Codierungstyp und einer OID-Übereinstimmung. Wenn dort keine Übereinstimmung gefunden wird, wird die Registrierung nach einer Übereinstimmung durchsucht.                                                                  |
| [**CryptGetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Übernimmt den Wert für den angegebenen Codierungstyp, Funktionsnamen, OID und Wertnamen.                                                                                                                            |
| [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Initialisiert und gibt ein Handle des OID-Funktionssets zurück, der durch den angegebenen Funktionsnamen identifiziert wird.                                                                                                                 |
| [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Installiert einen Satz aufrufbarer OID-Funktionsadressen.                                                                                                                                                                 |
| [**CryptRegisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Registriert die DLL mit der Standardfunktion, die für den angegebenen Codierungstyp und Funktionsnamen aufgerufen werden soll.                                                                                               |
| [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Registriert die DLL, die die Funktion enthält, die für den angegebenen Codierungstyp, Funktionsnamen und die angegebene OID aufgerufen werden soll.                                                                                                 |
| [**CryptRegisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Registriert die in der [**CRYPT \_ OID \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) angegebenen OID-Informationen und hält sie in der Registrierung bei.                                                                                |
| [**CryptSetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Legt den Wert für den angegebenen Codierungstyp, Funktionsnamen, OID und Wertnamen fest.                                                                                                                                |
| [**CryptUnregisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Entfernt die Registrierung für die DLL, die die Standardfunktion enthält, die für den angegebenen Codierungstyp und Funktionsnamen aufgerufen werden soll.                                                                            |
| [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Entfernt die Registrierung für die DLL, die die Funktion enthält, die für den angegebenen Codierungstyp, Funktionsnamen und die angegebene OID aufgerufen werden soll.                                                                              |
| [**CryptUnregisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Entfernt die Registrierung für die angegebenen OID-Informationen.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Remote Object Retrieval Functions

Mit den folgenden Funktionen kann der Benutzer ein PKI-Objekt (Public Key Infrastructure) abrufen, die URL eines Zertifikats, einer CTL oder einer Zertifikatsperrliste abrufen oder eine URL aus einem Objekt extrahieren.

| Funktion                                                     | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**CryptGetObjectUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Übernimmt die URL des Remoteobjekts aus einem Zertifikat, einer Zertifikatsperrliste oder einer Zertifikatsperrliste. |
| [**CryptRetriobjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Ruft das PKI-Objekt von einem Durch eine URL angegebenen Speicherort ab.           |



 

### <a name="pfx-functions"></a>PFX-Funktionen

Die folgenden Funktionen unterstützen [*BLOBs*](../secgloss/b-gly.md)im PFX-Format (Personal Information Exchange).

| Funktion                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFXExportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | Exporte aus dem Zertifikat, auf [*das verwiesen wird,*](../secgloss/c-gly.md) speichern die Zertifikate und, falls verfügbar, die zugehörigen [*privaten Schlüssel.*](../secgloss/p-gly.md) |
| [**PFXExportCertStoreEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | Exporte aus dem Zertifikat, auf das verwiesen wird, speichern die Zertifikate und, falls verfügbar, die zugehörigen privaten Schlüssel.                                                                                                                                                             |
| [**PFXImportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Importiert ein PFX-BLOB und gibt das Handle eines Speichers zurück, der Zertifikate und alle zugeordneten privaten Schlüssel enthält.                                                                                                                                                            |
| [**PFXIsPFXBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Versucht, die äußere Ebene eines BLOB als PFX-Paket zu decodieren.                                                                                                                                                                                                                |
| [**PFXVerifyPassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Versucht, die äußere Ebene eines BLOB als PFX-Paket zu decodieren und mit dem angegebenen Kennwort zu entschlüsseln.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Sicherungs- und Wiederherstellungsfunktionen für Zertifikatdienste

Zertifikatdienste umfassen Funktionen zum Sichern und Wiederherstellen der Zertifikatdienst-Datenbank. Diese Sicherungs- und Wiederherstellungsfunktionen der Zertifikatdienste sind in Certadm.dll. Im Gegensatz zu den anderen API-Elementen, die Zertifikatdiensten zugeordnet sind, sind diese Funktionen nicht in einem Objekt gekapselt, das zum Aufrufen von Klassenmethoden verwendet werden kann. Stattdessen werden die Sicherungs- und Wiederherstellungs-APIs aufgerufen, indem zuerst die Certadm.dll-Bibliothek in den Arbeitsspeicher geladen wird, indem [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufgerufen wird und dann die Adresse der Funktionen durch Aufrufen von [**GetProcAddress bestimmt wird.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Wenn Sie mit dem Aufrufen der Sicherungs- und Wiederherstellungsfunktionen der Zertifikatdienste fertig sind, rufen Sie [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) auf, um Certadm.dll aus dem Arbeitsspeicher frei zu geben.

> [!Note]
> Sicherungs- und Wiederherstellungsfunktionen Certadm.dll die privaten Schlüssel des Zertifikatdiensts nicht [*sichern oder wiederherstellen.*](../secgloss/p-gly.md) Informationen zum Sichern der privaten Schlüssel der Zertifikatdienste finden Sie unter Sichern und Wiederherstellen des privaten [Schlüssels der Zertifikatdienste.](backing-up-and-restoring-the-certificate-services-private-key.md)
> 
> Zum Aufrufen der Sicherungs- und Wiederherstellungsfunktionen müssen Sie über sicherungs- und [*wiederherstellungsberechtigungen verfügen.*](../secgloss/p-gly.md) Weitere Informationen finden Sie unter [Festlegen der Sicherungs- und Wiederherstellungsberechtigungen.](setting-the-backup-and-restore-privileges.md)

 

> [!Note]  
> Wenn **CoInitializeEx** zuvor in demselben Thread aufgerufen wurde, der zum Aufrufen der Sicherungs- und Wiederherstellungs-APIs der Zertifikatdienste verwendet wurde, muss das FLAG COINIT \_ APARTMENTTHREADED an **CoInitializeEx** übergeben worden sein. Das heißt, wenn Sie denselben Thread verwenden, können Sie die Zertifikatdienste-API zum Sichern und Wiederherstellen nicht aufrufen, wenn der Thread zuvor das COINIT MULTITHREADED-Flag in einem Aufruf von \_ **CoInitializeEx übergeben hat.**

 

Die Sicherungs-APIs der Zertifikatdienste sind in "Certbcli.h" definiert. Wenn Sie das Programm erstellen, verwenden Sie jedoch Certsrv.h als Includedatei.

Die folgenden APIs werden von Certadm.dll.

| Funktion                                                                         | BESCHREIBUNG                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Schließt eine geöffnete Datei.                                                                                                |
| [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Beendet eine Sicherungssitzung.                                                                                                |
| [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Gibt einen Puffer frei, der von den Sicherungs- und Wiederherstellungs-APIs zugeordnet wird.                                                              |
| [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Gibt eine Liste der Protokolldateien zurück, die sichern werden müssen.                                                                |
| [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Gibt eine Liste der Datenbankdateien zurück, die sichern werden müssen.                                                           |
| [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Ruft die Liste der dynamischen Dateinamen der Zertifikatdienste ab, die für den angegebenen Sicherungskontext gesichert werden müssen. |
| [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Öffnet eine Datei als Vorbereitung für deren Sichern.                                                                        |
| [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Bereitet die Datenbank für die Onlinesicherung vor.                                                                          |
| [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Liest den Inhalt einer geöffneten Datei.                                                                                 |
| [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Schneidet die Protokolldateien ab.                                                                                              |
| [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Bestimmt, ob ein Zertifikatdienstserver online ist (aktiv ausgeführt).                                        |
| [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Beendet eine Wiederherstellungssitzung.                                                                                               |
| [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Ruft Datenbankstandorte ab (wird sowohl für Sicherungs- als auch für Wiederherstellungsszenarien verwendet).                                            |
| [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Startet eine Wiederherstellungssitzung.                                                                                             |
| [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Registriert einen Wiederherstellungsvorgang.                                                                                        |
| [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Schließt einen zuvor registrierten Wiederherstellungsvorgang ab.                                                                  |
| [**CertSrvRestoreRegisterThroughFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Registriert einen Wiederherstellungsvorgang.                                                                                        |
| [**CertSrvServerControl**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Sendet einen Steuerungsbefehl an die Certificate Services-Instanz.                                                         |



 

## <a name="callback-functions"></a>Rückruffunktionen

Die Rückruffunktionen in diesem Abschnitt werden verwendet, [](../secgloss/c-gly.md) um anwendungsdefinierte Zertifikatspeicheranbieter zu registrieren oder zu installieren und verwandte Funktionen über Rückruffunktionen zur Verfügung zu stellen. Rückruffunktionen werden von einer Anwendung implementiert und von [*CryptoAPI-Funktionen*](../secgloss/c-gly.md) aufgerufen. Rückruffunktionen ermöglichen es der Anwendung, teilweise zu steuern, wie CryptoAPI-Funktionen Daten bearbeiten.

| Rückruffunktion                                                                                                        | Zweck                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertChainFindByIssuerCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Eine anwendungsdefinierte Rückruffunktion, mit der die Anwendung Zertifikate filtern kann, die möglicherweise der Zertifikatkette hinzugefügt werden.                                                                                                                                                                                                     |
| [**CertDllOpenStoreProv**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Definiert die Open-Funktion des Speicheranbieters.                                                                                                                                                                                                                                                                                                     |
| [**CertEnumPhysicalStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Rückruffunktion, die von der [**CertEnumPhysicalStore-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und zu präsentieren.                                                                                                                                                                                 |
| [**CertEnumSystemStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Rückruffunktion, die von der [**CertEnumSystemStore-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und zu präsentieren.                                                                                                                                                                                     |
| [**CertEnumSystemStoreLocationCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Rückruffunktion, die von der [**CertEnumSystemStoreLocation-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und zu präsentieren.                                                                                                                                                                     |
| [**CertStoreProvCloseCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Bestimmt, was geschieht, wenn die Verweisanzahl eines [*geöffneten Speichers*](../secgloss/r-gly.md) 0 (null) wird.                                                                                                                                                                                    |
| [**CertStoreProvControl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Ermöglicht es einer Anwendung, benachrichtigt zu werden, wenn ein Unterschied zwischen dem Inhalt eines zwischengespeicherten Speichers und dem Inhalt dieses Speichers besteht, während er im Speicher beibehalten wird.                                                                                                                                                                   |
| [**CertStoreProvDeleteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Bestimmt aktionen, die vor dem Löschen eines Zertifikats aus einem Zertifikatspeicher durchgeführt werden sollen.                                                                                                                                                                                                                                                      |
| [**CertStoreProvDeleteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Bestimmt Aktionen, die vor dem Löschen einer [*Zertifikatsperrliste*](../secgloss/c-gly.md) (Certificate Revocation List, CRL) aus einem Zertifikatspeicher durchgeführt werden sollen.                                                                                                                        |
| [**CertStoreProvDeleteCTL**](certstoreprovdeletectl.md)                                                                 | Bestimmt, ob eine CTL gelöscht werden kann.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvFindCert**](certstoreprovfindcert.md)                                                                   | Sucht das erste oder nächste Zertifikat in einem Speicher, der den angegebenen Kriterien entspricht.                                                                                                                                                                                                                                                             |
| [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)                                                                     | Sucht die erste oder nächste CRL in einem Speicher, der den angegebenen Kriterien entspricht.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFindCTL**](certstoreprovfindctl.md)                                                                     | Sucht die erste oder nächste CTL in einem Speicher, der den angegebenen Kriterien entspricht.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFreeFindCert**](certstoreprovfreefindcert.md)                                                           | Gibt einen zuvor gefundenen Zertifikatkontext frei.                                                                                                                                                                                                                                                                                                 |
| [**CertStoreProvFreeFindCRL**](certstoreprovfreefindcrl.md)                                                             | Gibt einen zuvor gefundenen CRL-Kontext frei.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvFreeFindCTL**](certstoreprovfreefindctl.md)                                                             | Gibt einen zuvor gefundenen CTL-Kontext frei.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvGetCertProperty**](certstoreprovgetcertproperty.md)                                                     | Ruft eine angegebene Eigenschaft eines Zertifikats ab.                                                                                                                                                                                                                                                                                              |
| [**CertStoreProvGetCRLProperty**](certstoreprovgetcrlproperty.md)                                                       | Ruft eine angegebene Eigenschaft einer Sperrliste ab.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvGetCTLProperty**](certstoreprovgetctlproperty.md)                                                       | Ruft eine angegebene Eigenschaft einer CTL ab.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Wird derzeit nicht verwendet, kann aber in zukünftige CSPs exportiert werden.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Wird derzeit nicht verwendet, kann aber in zukünftige CSPs exportiert werden.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCTL**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Lesen Sie die Kopie des CTL-Kontexts des Anbieters, und erstellen Sie ggf. einen neuen CTL-Kontext.                                                                                                                                                                                                                                                     |
| [**CertStoreProvSetCertPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Bestimmt Aktionen, die vor einem Aufruf von [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) oder [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)ausgeführt werden sollen.                                                                                                                             |
| [**CertStoreProvSetCRLPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Bestimmt Aktionen, die vor einem Aufruf von [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) oder [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)ausgeführt werden sollen.                                                                                                                                                             |
| [**CertStoreProvSetCTLProperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Bestimmt, ob eine Eigenschaft für eine CTL festgelegt werden kann.                                                                                                                                                                                                                                                                                            |
| [**CertStoreProvWriteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Bestimmt Aktionen, die vor dem Hinzufügen eines Zertifikats zu einem Speicher ausgeführt werden sollen.                                                                                                                                                                                                                                                                        |
| [**CertStoreProvWriteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Bestimmt Aktionen, die vor dem Hinzufügen einer Sperrliste zu einem Speicher ausgeführt werden müssen.                                                                                                                                                                                                                                                                                |
| [**CertStoreProvWriteCTL**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Bestimmt, ob dem Speicher eine CTL hinzugefügt werden kann.                                                                                                                                                                                                                                                                                           |
| [**CRYPT \_ ENUM \_ KEYID \_ PROP**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Rückruffunktion, die von der [**CryptEnumKeyIdentifierProperties-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties) verwendet wird.                                                                                                                                                                                                                          |
| [**\_ \_ CRYPT-ENUM-OIDFUNKTION \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Rückruffunktion, die von der [**CryptEnumOIDFunction-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction) verwendet wird.                                                                                                                                                                                                                                                  |
| [**CRYPT \_ ENUM \_ OID \_ INFO**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Rückruffunktion, die von der [**CryptEnumOIDInfo-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo) verwendet wird.                                                                                                                                                                                                                                                          |
| [**CryptGetSignerCertificateCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Rückruffunktion, die mit der [**CRYPT \_ VERIFY MESSAGE \_ \_ PARA-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) verwendet wird, um das Zertifikat eines Nachrichten signierers abzurufen und zu überprüfen.                                                                                                                                                                                 |
| [**PCRYPT \_ DECRYPT \_ PRIVATE \_ KEY \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Rückruffunktion, die von der [**CryptImportPKCS8-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) verwendet wird.                                                                                                                                                                                                                                                          |
| [**PCRYPT \_ ENCRYPT \_ PRIVATE \_ KEY \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Rückruffunktion, die beim Erstellen der [**CRYPT \_ ENCRYPTED PRIVATE \_ KEY \_ \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) verwendet wird.                                                                                                                                                                                                          |
| [**PCRYPT \_ RESOLVE \_ HCRYPTPROV \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Rückruffunktion, die von der [**CryptImportPKCS8-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) verwendet wird.                                                                                                                                                                                                                                                          |
| [**PFN \_ CDF \_ PARSE \_ ERROR \_ CALLBACK**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Eine benutzerdefinierte Funktion, die für Katalogdefinitionsfunktionsfehler beim Analysieren einer Katalogdefinitionsdatei (CDF) aufgerufen wird.                                                                                                                                                                                                                          |
| [**PFN \_ CERT \_ CREATE \_ CONTEXT \_ SORT \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Wird für jeden sortierten Kontexteintrag aufgerufen, wenn ein Kontext erstellt wird.                                                                                                                                                                                                                                                                               |
| [**PFN \_ CMSG \_ CNG \_ IMPORT \_ CONTENT \_ ENCRYPT \_ KEY**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Eine installierbare [*CNG-Objektbezeichnerfunktion*](../secgloss/o-gly.md) (OID) zum Importieren eines bereits entschlüsselten Inhaltsverschlüsselungsschlüssels (Content Encryption Key, CEK).                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG \_ IMPORT \_ KEY \_ AGREE**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Importiert einen Inhaltsverschlüsselungsschlüssel für einen Schlüsseltransportempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG \_ IMPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Eine installierbare CNG-OID-Funktion zum Importieren und [*Entschlüsseln*](../secgloss/d-gly.md) eines Schlüsseltransportempfängers, verschlüsselten [*Inhaltsverschlüsselungsschlüssels*](../secgloss/e-gly.md) (Content Encryption Key, CEK).                                                                   |
| [**PFN \_ CMSG \_ EXPORT \_ KEY \_ AGREE**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Verschlüsselt und exportiert den Inhaltsverschlüsselungsschlüssel für einen Schlüsselvereinbarungsempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ EXPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Verschlüsselt und exportiert den Inhaltsverschlüsselungsschlüssel für einen Schlüsseltransportempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ EXPORT \_ MAIL \_ LIST**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Verschlüsselt und exportiert den Inhaltsverschlüsselungsschlüssel für einen Empfänger einer Adressenliste einer umschlageten Nachricht.                                                                                                                                                                                                                                         |
| [**PFN \_ CMSG \_ GEN \_ CONTENT \_ ENCRYPT \_ KEY**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Generiert den [*symmetrischen Schlüssel,*](../secgloss/s-gly.md) der zum Verschlüsseln von Inhalten für eine umschlagete Nachricht verwendet wird.                                                                                                                                                                                     |
| [**PFN \_ CMSG \_ IMPORT \_ KEY \_ AGREE**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Importiert einen Inhaltsverschlüsselungsschlüssel für einen Schlüsseltransportempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ IMPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Importiert einen Inhaltsverschlüsselungsschlüssel für einen Schlüsseltransportempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ IMPORT \_ MAIL \_ LIST**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Importiert einen Inhaltsverschlüsselungsschlüssel für einen Schlüsseltransportempfänger einer umschlageten Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CRYPT \_ EXPORT \_ PUBLIC \_ KEY \_ INFO \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Wird von [**CryptExportPublicKeyInfoEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) aufgerufen, um ein BLOB mit öffentlichem Schlüssel zu exportieren und zu codieren.                                                                                                                                                                                                                         |
| [**PFN \_ CRYPT \_ EXTRACT \_ ENCODED \_ SIGNATURE \_ PARAMETERS \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Wird aufgerufen, um den Hashalgorithmusbezeichner und optional die Signaturparameter zu decodieren und zurückzugeben.                                                                                                                                                                                                                                            |
| [**PFN \_ CRYPT \_ SIGN \_ AND \_ ENCODE \_ HASH \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Wird aufgerufen, um einen berechneten Hash zu signieren und zu codieren.                                                                                                                                                                                                                                                                                                    |
| [**PFN \_ CRYPT \_ VERIFY \_ ENCODED \_ SIGNATURE \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Wird aufgerufen, um eine codierte Signatur zu entschlüsseln und mit einem berechneten Hash zu vergleichen.                                                                                                                                                                                                                                                                     |
| [**PFN \_ IMPORT \_ PUBLIC \_ KEY \_ INFO \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Wird von [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) aufgerufen, um den Algorithmusbezeichner des [*öffentlichen Schlüssels*](../secgloss/p-gly.md) zu decodieren, den Algorithmusanbieter zu laden und das [*Schlüsselpaar*](../secgloss/k-gly.md)zu importieren. |
| [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)                                                                       | Eine benutzerdefinierte Rückruffunktion, mit der der Aufrufer der [**CryptUIDlgSelectCertificate-Funktion**](cryptuidlgselectcertificate.md) die Anzeige von Zertifikaten verarbeiten kann, die der Benutzer zur Anzeige auswählt.                                                                                                                               |
| [**PFNCMFILTERPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Filtert jedes Zertifikat, um zu entscheiden, ob es im Dialogfeld für die Zertifikatauswahl angezeigt wird, das von der [**CertSelectCertificate-Funktion**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) angezeigt wird.                                                                                                                                                                |
| [**PFNCMHOOKPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Wird aufgerufen, bevor Nachrichten vom Dialogfeld für die Zertifikatauswahl verarbeitet werden, das von der [**CertSelectCertificate-Funktion**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) erstellt wird.                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Katalogdefinitionsfunktionen

Diese Funktionen werden verwendet, um einen Katalog zu erstellen. Alle diese Funktionen werden von [MakeCat](makecat.md)aufgerufen.

| Funktion                                                                           | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATCDFClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Schließt eine Katalogdefinitionsdatei und gibt den Arbeitsspeicher für die entsprechende [**CRYPTCATCDF-Struktur**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) frei. |
| [**CryptCATCDFEnumAttributesWithCDFTag**](cryptcatcdfenumattributeswithcdftag.md) | Listet die Attribute von Memberdateien im Abschnitt **CatalogFiles** einer CDF auf.                                       |
| [**CryptCATCDFEnumCatAttributes**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Listet Attribute auf Katalogebene im **CatalogHeader-Abschnitt** einer CDF auf.                                        |
| [**CryptCATCDFEnumMembersByCDFTagEx**](cryptcatcdfenummembersbycdftagex.md)       | Listet die einzelnen Dateimember im Abschnitt **CatalogFiles** einer CDF auf.                                          |
| [**CryptCATCDFÖffnen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Öffnet eine vorhandene CDF zum Lesen und initialisiert eine [**CRYPTCATCDF-Struktur.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)                         |



 

## <a name="catalog-functions"></a>Katalogfunktionen

Diese Funktionen werden zum Verwalten eines Katalogs verwendet.

| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Übernimmt ein Handle für einen Katalogadministratorkontext. Dieses Handle kann von nachfolgenden Aufrufen der Funktionen [**CryptCATAdminAddCatalog,**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)und [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) verwendet werden. |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Übernimmt ein Handle für einen Katalogadministratorkontext für einen bestimmten Hashalgorithmus und eine Hashrichtlinie.                                                                                                                                                                                                                                   |
| [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Fügt der Katalogdatenbank einen Katalog hinzu.                                                                                                                                                                                                                                                                                            |
| [**CryptCATAdminCalcHashFromFileHandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Berechnet den Hash für eine Datei.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Berechnet den Hash für eine Datei mithilfe des angegebenen Algorithmus.                                                                                                                                                                                                                                                                   |
| [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Listet die Kataloge auf, die einen angegebenen Hash enthalten.                                                                                                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCatalogContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Gibt ein Handle für einen Katalogkontext frei, der zuvor von der [**CryptCATAdminAddCatalog-Funktion**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) zurückgegeben wurde.                                                                                                                                                                                             |
| [**CryptCATAdminReleaseContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Gibt das Zuvor von der [**CryptCATAdminAcquireContext-Funktion zugewiesene**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) Handle frei.                                                                                                                                                                                                        |
| [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | Löscht eine Katalogdatei und entfernt den Eintrag dieses Katalogs aus der Windows Katalogdatenbank.                                                                                                                                                                                                                                         |
| [**CryptCATAdminResolveCatalogPath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Ruft den vollqualifizierten Pfad des angegebenen Katalogs ab.                                                                                                                                                                                                                                                                       |
| [**CryptCATCatalogInfoFromContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Ruft Kataloginformationen aus einem angegebenen Katalogkontext ab.                                                                                                                                                                                                                                                                    |
| [**CryptCATClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Schließt ein Kataloghandle, das zuvor von der [**CryptCATOpen-Funktion**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) geöffnet wurde.                                                                                                                                                                                                                                    |
| [**CryptCATEnumerateAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Listet die Attribute auf, die einem Member eines Katalogs zugeordnet sind.                                                                                                                                                                                                                                                                   |
| [**CryptCATEnumerateCatAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Listet die einem Katalog zugeordneten Attribute auf.                                                                                                                                                                                                                                                                               |
| [**CryptCATEnumerateMember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Listet die Member eines Katalogs auf.                                                                                                                                                                                                                                                                                               |
| [**CryptCATGetAttrInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Ruft Informationen zu einem Attribut eines Members eines Katalogs ab.                                                                                                                                                                                                                                                                 |
| [**CryptCATGetMemberInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Ruft Elementinformationen aus pkcs 7 des Katalogs \# ab. Zusätzlich zum Abrufen der Memberinformationen für ein angegebenes Verweistag öffnet diese Funktion einen Memberkontext.                                                                                                                                                    |
| [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Öffnet einen Katalog und gibt ein Kontexthandle an den geöffneten Katalog zurück.                                                                                                                                                                                                                                                                 |
| [**IsCatalogFile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Ruft einen booleschen Wert ab, der angibt, ob die angegebene Datei eine Katalogdatei ist.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>WinTrust Functions

Die folgenden Funktionen werden verwendet, um verschiedene Vertrauensstellungen auszuführen.

| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Fügt dem System des Benutzers eine Vertrauensanbieteraktion hinzu.                                                                                                                   |
| [**WintrustGetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Ruft Richtlinienflags für einen Richtlinienanbieter ab.                                                                                                                        |
| [**WintrustAddDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Gibt den Standardverwendungsbezeichner und die Rückrufinformationen für einen Anbieter an.                                                                                       |
| [**WintrustGetDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Ruft den Standardverwendungsbezeichner und die Rückrufinformationen ab.                                                                                                     |
| [**WintrustLoadFunctionPointers**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Lädt Funktionseinstiegspunkte für eine angegebene Aktions-GUID.                                                                                                             |
| [**WintrustRemoveActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Entfernt eine Aktion, die von der [**WintrustAddActionID-Funktion**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) hinzugefügt wurde.                                                                          |
| [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Legt die Standardeinstellung fest, die bestimmt, ob Seitenhashes beim Erstellen indirekter DATEN des Subjektschnittstellenpakets (Subject Interface Package, SIP) für portable ausführbare Dateien enthalten sind. |
| [**WintrustSetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Legt Richtlinienflags für einen Richtlinienanbieter fest.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Führt eine Vertrauensüberprüfungsaktion für ein angegebenes -Objekt aus.                                                                                                          |
| [**WinVerifyTrustEx**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Führt eine Vertrauensüberprüfungsaktion für ein angegebenes Objekt und einen Zeiger auf eine WINTRUST \_ DATA-Struktur aus.                                                        |
| [**WTHelperCertCheckValidSignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Überprüft, ob eine Signatur gültig ist.                                                                                                                                 |
| [**WTHelperCertFindIssuerCertificate**](wthelpercertfindissuercertificate.md)         | Sucht ein Ausstellerzertifikat aus den angegebenen Zertifikatspeichern, das dem angegebenen Antragstellerzertifikat entspricht.                                                    |
| [**WTHelperCertIsSelfSigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Überprüft, ob ein Zertifikat selbstsignierend ist.                                                                                                                         |
| [**WTHelperGetFileHash**](wthelpergetfilehash.md)                                     | Überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.                                                            |
| [**WTHelperGetProvCertFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Ruft ein Vertrauensstellungsanbieterzertifikat aus der Zertifikatkette ab.                                                                                                   |
| [**WTHelperGetProvPrivateDataFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Empfängt eine [**CRYPT \_ PROVIDER \_ PRIVDATA-Struktur**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) aus der Kette unter Verwendung der Anbieter-ID.                                           |
| [**WTHelperGetProvSignerFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Ruft einen Signierer oder Gegensignierer nach Index aus der Kette ab.                                                                                                         |
| [**WTHelperProvDataFromStateData**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Ruft Vertrauensstellungsanbieterinformationen aus einem angegebenen Handle ab.                                                                                                        |



 

## <a name="object-locator-functions"></a>Objektlocatorfunktionen

Die folgenden Rückruffunktionen können von einem benutzerdefinierten Anbieter implementiert werden, der vom Schannel-Sicherheitspaket (Secure Channel) aufgerufen werden soll, um Zertifikate abzurufen.



| Funktion                                                                                                             | BESCHREIBUNG                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**PFN \_ CRYPT \_ OBJECT \_ LOCATOR \_ PROVIDER \_ FLUSH**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Gibt an, dass sich ein Objekt geändert hat.                   |
| [**PFN \_ CRYPT \_ OBJECT \_ LOCATOR \_ PROVIDER \_ GET**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Ruft ein -Objekt ab.                                    |
| [**RELEASE DES \_ PFN-CRYPT-OBJEKTLOCATORANBIETERS \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Gibt den Anbieter frei.                                  |
| [**PFN \_ CRYPT \_ OBJECT \_ LOCATOR \_ PROVIDER \_ FREE \_ PASSWORD**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Gibt das Kennwort frei, das zum Verschlüsseln eines PFX-Bytearrays verwendet wird. |
| [**PFN \_ CRYPT \_ OBJECT \_ LOCATOR \_ PROVIDER \_ FREE**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Gibt das vom Anbieter zurückgegebene Objekt frei.           |
| [**\_ \_ \_ \_ \_ FREE-BEZEICHNER DES PFN-CRYPT-OBJEKTLOCATORS \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Gibt Arbeitsspeicher für einen Objektbezeichner frei.               |
| [**INITIALISIEREN DES \_ PFN-CRYPT-OBJEKTLOCATORANBIETERS \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Initialisiert den Anbieter.                               |



 

 

 

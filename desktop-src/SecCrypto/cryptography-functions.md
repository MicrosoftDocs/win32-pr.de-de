---
description: Listet die von CryptoAPI bereitgestellten Funktionen auf.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: Kryptografiefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91338c4a1cea62e2ecc4a2fa1f7254f303ef9b2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104132205"
---
# <a name="cryptography-functions"></a>Kryptografiefunktionen

Kryptografiefunktionen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Cryptxml-Funktionen](#cryptxml-functions)
-   [Signatur Geber Funktionen](#signer-functions)
-   [Grundlegende Kryptografiefunktionen](#base-cryptography-functions)
    -   [Dienstanbieter Funktionen](#service-provider-functions)
    -   [Schlüsselgenerierung und Exchange-Funktionen](#key-generation-and-exchange-functions)
    -   [Objektcodierungsfunktionen](#object-encoding-and-decoding-functions)
    -   [Datenverschlüsselungs-und Entschlüsselungs Funktionen](#data-encryption-and-decryption-functions)
    -   [Hash-und digitale Signatur Funktionen](#hash-and-digital-signature-functions)
-   [Zertifikat-und Zertifikat Speicherfunktionen](#certificate-and-certificate-store-functions)
    -   [Zertifikat Speicherfunktionen](#certificate-and-certificate-store-functions)
    -   [Wartungsfunktionen für Zertifikat-und Zertifikat Speicher](#certificate-and-certificate-store-maintenance-functions)
    -   [Zertifikatfunktionen](#certificate-functions)
    -   [Funktionen der Zertifikat Sperr Liste](#certificate-revocation-list-functions)
    -   [Funktionen der Zertifikat Vertrauens Liste](#certificate-trust-list-functions)
    -   [Erweiterte Eigenschaften Funktionen](#extended-property-functions)
-   [Makecert-Funktionen](#makecert-functions)
-   [Funktionen zur Zertifikat Überprüfung](#certificate-verification-functions)
    -   [Überprüfungs Funktionen mit CTLs](#verification-functions-using-ctls)
    -   [Funktionen zur Überprüfung der Zertifikat Kette](#certificate-chain-verification-functions)
-   [Nachrichtenfunktionen](#message-functions)
    -   [Nachrichten Funktionen auf niedriger Ebene](#low-level-message-functions)
    -   [Vereinfachte Nachrichten Funktionen](#simplified-message-functions)
-   [Hilfsfunktionen](#auxiliary-functions)
    -   [Datenverwaltung Funktionen](#data-management-functions)
    -   [Daten Konvertierungs Funktionen](#data-conversion-functions)
    -   [Erweiterte Schlüssel Verwendungs Funktionen](#enhanced-key-usage-functions)
    -   [Schlüsselbezeichnerfunktionen](#key-identifier-functions)
    -   [OID-Unterstützungsfunktionen](#oid-support-functions)
    -   [Funktionen zum Abrufen von Remote Objekten](#remote-object-retrieval-functions)
    -   [PFX-Funktionen](#pfx-functions)
-   [Sicherungs-und Wiederherstellungs Funktionen für Zertifikat Dienste](#certificate-services-backup-and-restore-functions)
-   [Rückruffunktionen](#callback-functions)
-   [Katalog Definitions Funktionen](#catalog-definition-functions)
-   [Katalogfunktionen](#catalog-functions)
-   [Wintrust-Funktionen](#wintrust-functions)
-   [Objektlocator-Funktionen](#object-locator-functions)

## <a name="cryptxml-functions"></a>Cryptxml-Funktionen

Die kryptografischen XML-Funktionen stellen eine API zum Erstellen und darstellen digitaler Signaturen mithilfe von XML-formatierten Daten bereit. Informationen zu XML-formatierten Signaturen finden Sie in der XML-Signature-Syntax und-Verarbeitungs Spezifikation unter <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Funktion                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ein \_ shafinal**](a-shafinal.md)                                                 | Berechnet den abschließenden Hash der Daten, die von der MD5Update-Funktion eingegeben werden.                                                                                                                                                                                                                                           |
| [**Ein \_ shainit**](a-shainit.md)                                                   | Initiiert das hashdown eines Datenstroms.                                                                                                                                                                                                                                                                       |
| [**Ein " \_ shaupdate"**](a-shaupdate.md)                                               | Fügt einem angegebenen Hash Objektdaten hinzu.                                                                                                                                                                                                                                                                            |
| [**Cryptxmlkreatereferenzierung**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Erstellt einen Verweis auf eine XML-Signatur.                                                                                                                                                                                                                                                                         |
| [**Cryptxmladdobject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Fügt der Signatur im Dokument Kontext, der für die Codierung geöffnet wurde, das **Object** -Element hinzu.                                                                                                                                                                                                                        |
| [**Cryptxmlclose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Schließt ein kryptografisches XML-Objekt handle.                                                                                                                                                                                                                                                                        |
| [**Cryptxmldigestreferenzierung**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Wird von einer Anwendung verwendet, um den aufgelösten Verweis zu Digest. Diese Funktion wendet Transformationen an, bevor der Digest aktualisiert wird.                                                                                                                                                                                            |
| [**Cryptxmldllclosedigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Gibt den \_ \_ von der [**cryptxmldllkreatediererfunktion**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest) zugewiesenen Crypt XML-Digest frei.                                                                                                                                                                                               |
| [**Cryptxmldllkreatediering**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Erstellt ein Digest-Objekt für die angegebene Methode.                                                                                                                                                                                                                                                                |
| [**Cryptxmldllkreatekey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Analysiert das **KeyValue** -Element und erstellt ein CNG (Cryptography API: Next Generation) BCrypt-Schlüssel handle, um eine Signatur zu überprüfen.                                                                                                                                                                                   |
| [**Cryptxmldlldigestdata**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Verschiebt Daten in den Digest.                                                                                                                                                                                                                                                                                       |
| [**Cryptxmldllencodealgorithmus**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Codiert **SignatureMethod** -oder **DigestMethod** -Elemente für Agile-Algorithmen mit Standardparametern.                                                                                                                                                                                                           |
| [**Cryptxmldllencodkeyvalue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Codiert ein **KeyValue** -Element.                                                                                                                                                                                                                                                                                  |
| [**Cryptxmldllfinalizedigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Ruft den Digest-Wert ab.                                                                                                                                                                                                                                                                                      |
| [**Cryptxmldllgetalgorithminfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Decodiert den XML-Algorithmus und gibt Informationen über den Algorithmus zurück.                                                                                                                                                                                                                                           |
| [**Cryptxmldllgetinterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Ruft einen Zeiger auf die Funktionen der kryptografieerweiterung für den angegebenen Algorithmus ab.                                                                                                                                                                                                                        |
| [**Cryptxmldllsigndata**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Signiert Daten.                                                                                                                                                                                                                                                                                                      |
| [**Cryptxmldllverifysignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Überprüft eine Signatur.                                                                                                                                                                                                                                                                                            |
| [**Cryptxmlencode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Codiert Signatur Daten mithilfe der angegebenen XML-Writer-Rückruffunktion.                                                                                                                                                                                                                                       |
| [**Cryptxmlgetalgorithminfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Decodiert die crypt \_ \_ -XML-Algorithmusstruktur und gibt Informationen über den Algorithmus zurück.                                                                                                                                                                                                                         |
| [**Cryptxmlgetdoccontext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Gibt den Dokument Kontext zurück, der vom bereitgestellten handle angegeben wird.                                                                                                                                                                                                                                                   |
| [**Cryptxmlgetreferenzierung**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Gibt das vom angegebenen handle angegebene **Verweis** Element zurück.                                                                                                                                                                                                                                              |
| [**Cryptxmlgetsignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Gibt ein XML- **Signatur** Element zurück.                                                                                                                                                                                                                                                                            |
| [**Cryptxmlgetstatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Gibt eine [**crypt- \_ XML- \_ Status**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) Struktur zurück, die Status Informationen über das durch das angegebene handle angegebene Objekt enthält.                                                                                                                                                           |
| [**Cryptxmlgettransformationen**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Gibt Informationen über die standardmäßige Transformations Kette-Engine zurück.                                                                                                                                                                                                                                                    |
| [**Cryptxmlimportpublickey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Importiert den vom bereitgestellten handle angegebenen öffentlichen Schlüssel.                                                                                                                                                                                                                                                         |
| [**Cryptxmlopentoencode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Öffnet eine digitale XML-Signatur zum Codieren und zurückgibt eines Handles des geöffneten **Signatur** Elements. Das Handle kapselt einen Dokument Kontext mit einer einzelnen [**crypt- \_ XML- \_ Signatur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) Struktur und bleibt so lange geöffnet, bis die Funktion " [**cryptxmlclose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) " aufgerufen wird. |
| [**Cryptxmlopentodecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Öffnet eine digitale XML-Signatur, um das Handle des Dokument Kontexts zu decodieren und zurückgegeben, der eine [**crypt \_ XML- \_ Signatur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) Struktur kapselt. Der Dokument Kontext kann ein oder mehrere **Signatur** Elemente enthalten.                                                                 |
| [**Cryptxmlabthmacsecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Legt den HMAC-geheimen Schlüssel für das Handle vor dem Aufruf der Funktion [**cryptxmlsign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) oder [**cryptxmlverify**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) fest.                                                                                                                                                        |
| [**Cryptxmlsign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Erstellt eine kryptografische Signatur eines **signetdinfo** -Elements.                                                                                                                                                                                                                                                   |
| [**Cryptxmlverifysignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Führt eine kryptografische Signatur Überprüfung eines **signetdinfo** -Elements aus.                                                                                                                                                                                                                                       |
| [*PFN- \_ crypt- \_ XML- \_ Schreib \_ Rückruf*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Erstellt eine Transformation für einen angegebenen Datenanbieter.                                                                                                                                                                                                                                                               |
| [*PFN \_ crypt, \_ XML \_ Create \_ Transform*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Schreibt kryptografische XML-Daten.                                                                                                                                                                                                                                                                                   |
| [*PFN- \_ crypt- \_ XML- \_ Daten \_ Anbieter \_ Lesen*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Liest kryptografische XML-Daten.                                                                                                                                                                                                                                                                                    |
| [*PFN- \_ crypt- \_ XML- \_ Daten \_ Anbieter \_ Schließen*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Gibt den kryptografischen XML-Datenanbieter frei.                                                                                                                                                                                                                                                                    |
| [*PFN-Crypt-XML-Aufzählung von \_ \_ \_ \_ ALG- \_ Informationen*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Listet vordefinierte und registrierte [**crypt \_ XML- \_ Algorithmus- \_ Informations**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) Einträge auf.                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Signatur Geber Funktionen

Stellt Funktionen zum Signieren und Zeitstempel von Daten bereit.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Signerfresignercontext**](signerfreesignercontext.md) | Gibt eine [**Signatur Geber \_ Kontext**](signer-context.md) Struktur frei, die durch einen vorherigen-Befehl der [**signersignetx**](signersignex.md) -Funktion zugeordnet wurde.                                                                                                                                                                                                                                                                      |
| [**Signror**](signerror.md)                             | Ruft die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion auf und konvertiert den Rückgabecode in ein **HRESULT**.                                                                                                                                                                                                                                                                                                            |
| [**Signersign**](signersign.md)                           | Signiert die angegebene Datei.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Signersignetx**](signersignex.md)                       | Signiert die angegebene Datei und gibt einen Zeiger auf die signierten Daten zurück.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Signiert und Zeitstempel der angegebenen Datei, sodass mehrere Unterschriften zugelassen werden.                                                                                                                                                                                                                                                                                                                                      |
| [**Signertimestamp**](signertimestamp.md)                 | Zeitstempel des angegebenen Subjekts. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.                                                                                                                                                                                       |
| [**Signertimestampex**](signertimestampex.md)             | Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur zurück, die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen. |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur zurück, die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält. Diese Funktion kann verwendet werden, um die X. 509-Public Key-Infrastruktur, RFC 3161 – kompatible, Zeitstempel auszuführen.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Zeitstempel des angegebenen Subjekts und unterstützen das Festlegen von Zeitstempeln für mehrere Signaturen.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Grundlegende Kryptografiefunktionen

Grundlegende Kryptografiefunktionen bieten die flexibelsten Möglichkeiten der Entwicklung von Kryptografieanwendungen. Die gesamte Kommunikation mit einem [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) erfolgt über diese Funktionen.

Ein CSP ist ein unabhängiges Modul, das alle kryptografischen Vorgänge ausführt. Mindestens ein CSP ist für jede Anwendung erforderlich, die Kryptografiefunktionen verwendet. Eine einzelne Anwendung kann gelegentlich mehr als einen CSP verwenden.

Wenn mehr als ein CSP verwendet wird, kann der zu verwendende in den kryptografischen kryptografiefunktionsaufrufen von CryptoAPI angegeben werden. Ein CSP, der Microsoft-Basis Kryptografieanbieter, ist mit der [*CryptoAPI*](../secgloss/c-gly.md)gebündelt. Dieser CSP wird von vielen der kryptoapi-Funktionen als Standardanbieter verwendet, wenn kein anderer CSP angegeben wird.

Jeder CSP stellt eine andere Implementierung der Kryptografieunterstützung bereit, die CryptoAPI bereitstellt. Einige bieten stärkere Kryptografiealgorithmen. andere enthalten Hardwarekomponenten, z. b. [*Smartcards*](../secgloss/s-gly.md). Darüber hinaus können einige CSPs gelegentlich direkt mit Benutzern kommunizieren, z. b. Wenn [*digitale Signaturen*](../secgloss/d-gly.md) mithilfe des [*privaten Schlüssels der Signatur*](../secgloss/s-gly.md)des Benutzers ausgeführt werden.

Grundlegende Kryptografiefunktionen sind in den folgenden allgemeinen Gruppen aufgeführt:

-   Dienstanbieter Funktionen
-   Schlüsselgenerierung und Exchange-Funktionen
-   Objektcodierungsfunktionen
-   Datenverschlüsselungs-und Entschlüsselungs Funktionen
-   Hash-und digitale Signatur Funktionen

### <a name="service-provider-functions"></a>Dienstanbieter Funktionen

Anwendungen verwenden die folgenden Dienstfunktionen zum Verbinden und Trennen eines [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP).

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
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft ein Handle für den <a href="/windows/desktop/SecGloss/k-gly"><em>Schlüssel Container</em></a> des aktuellen Benutzers innerhalb eines bestimmten CSP ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>Cryptcontextadressf</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erhöht den <a href="/windows/desktop/SecGloss/r-gly"><em>Verweis Zähler</em></a> für ein <a href="hcryptprov.md"><strong>hcryptprov</strong></a> -handle.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>Cryptenum Providers</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Listet die Anbieter auf einem Computer auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>Cryptenum providertypes</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Listet die Typen von Anbietern auf, die auf dem Computer unterstützt werden.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>Cryptgetdefaultprovider</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Bestimmt den Standard-CSP entweder für den aktuellen Benutzer oder für den Computer für einen angegebenen Anbietertyp.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft die Parameter ab, die die Vorgänge eines CSP steuern.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>Cryptinstalldefaultcontext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Installiert einen zuvor erworbenen <a href="hcryptprov.md"><strong>hcryptprov</strong></a> -Kontext, der als Standardkontext verwendet werden soll.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>Cryptreleasecontext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt das von der <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a> -Funktion erworbene Handle frei.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>Cryptsetprovider</strong></a> und <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>cryptsetproviderex</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt den Benutzer standardcsp für einen bestimmten CSP-Typ an.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>Cryptsetprovparam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt die Attribute eines CSP an.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>Cryptuninstalldefaultcontext</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Entfernt einen Standardkontext, der zuvor von " <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>cryptinstalldefaultcontext</strong></a>" installiert wurde.</td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>Freecryptprovfromcertex</strong></a></td>
<td>Gibt das Handle entweder für einen <a href="/windows/desktop/SecGloss/c-gly"><em>Kryptografiedienstanbieter (kryptografischen Service Provider</em></a> , CSP) oder für einen CNG-Schlüssel (Cryptography API: Next Generation) frei.</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>Schlüsselgenerierung und Exchange-Funktionen

Schlüsselgenerierung und Exchange-Funktionen [*tauschen Schlüssel*](../secgloss/e-gly.md) mit anderen Benutzern aus und erstellen, konfigurieren und zerstören [*kryptografische Schlüssel*](../secgloss/c-gly.md).

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
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt einen Schlüssel, der von einem Kennwort abgeleitet ist.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>Cryptdestroykey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Zerstört eine Taste.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>Cryptduplicatekey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt eine exakte Kopie eines Schlüssels, einschließlich des <a href="/windows/desktop/SecGloss/s-gly"><em>Zustands</em></a> des Schlüssels.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überträgt einen Schlüssel vom CSP in ein <a href="/windows/desktop/SecGloss/k-gly"><em>Schlüsselblob</em></a> im Speicherbereich der Anwendung.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt eine zufällige Taste.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>Cryptgenrandom verwendet</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Generiert zufällige Daten.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>Cryptgetkeyparam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft die Parameter eines Schlüssels ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft ein Handle für den Schlüsselaustausch oder den Signatur Schlüssel ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>Cryptimportkey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überträgt einen Schlüssel von einem <a href="/windows/desktop/SecGloss/k-gly"><em>Schlüsselblob</em></a> an einen CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>Cryptsetkeyparam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Gibt die Parameter eines Schlüssels an.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Objektcodierungsfunktionen

Dies sind allgemeine Codierungs-und Decodierungs Funktionen. Sie werden zum Codieren und Decodieren von [*Zertifikaten*](../secgloss/c-gly.md), [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs), [*Zertifikat Anforderungen*](../secgloss/c-gly.md)und Zertifikat Erweiterungen verwendet.

| Funktion                                           | BESCHREIBUNG                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Decodiert eine Struktur des Typs *lpszstructtype*.                                                                                                    |
| [**Cryptdecodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Decodiert eine Struktur des Typs *lpszstructtype*. " [**Cryptdecodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) " unterstützt die 1-Pass-Speicher Belegungs Option. |
| [**Bei cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Codiert eine Struktur vom Typ *lpszstructtype*.                                                                                                    |
| [**Cryptencodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Codiert eine Struktur vom Typ *lpszstructtype*. " [**Cryptencodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) " unterstützt die 1-Pass-Speicher Belegungs Option. |



 

### <a name="data-encryption-and-decryption-functions"></a>Datenverschlüsselungs-und Entschlüsselungs Funktionen

Die folgenden Funktionen unterstützen Verschlüsselungs-und Entschlüsselungs Vorgänge. [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) und [**cryptentschlüsseln**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) benötigen vor dem Aufrufen einen [*kryptografischen Schlüssel*](../secgloss/c-gly.md) . Dies erfolgt mithilfe der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)-, [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)-oder [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) -Funktion. Der Verschlüsselungsalgorithmus wird angegeben, wenn der Schlüssel erstellt wird. Mit " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " können zusätzliche Verschlüsselungs Parameter festgelegt werden.

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
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>Cryptentschlüsseln</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Entschlüsselt einen Abschnitt mit verschlüsselter <a href="/windows/desktop/SecGloss/c-gly"><em>Text</em></a> mithilfe des angegebenen Verschlüsselungsschlüssels.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Verschlüsselt einen Abschnitt von <a href="/windows/desktop/SecGloss/p-gly"><em>Klartext</em></a> unter Verwendung des angegebenen Verschlüsselungsschlüssels.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Führt die Verschlüsselung der Daten in einer <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a> Struktur aus.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>Cryptprotectmemory</strong></a></td>
<td>Verschlüsselt den Arbeitsspeicher, um vertrauliche Informationen zu schützen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Führt eine Entschlüsselungs-und Integritäts Überprüfung der Daten in einem <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a>aus.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>Cryptunprotectmemory</strong></a></td>
<td>Entschlüsselt Speicher, der mithilfe von " <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>cryptprotectmemory</strong></a>" verschlüsselt wurde.</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Hash-und digitale Signatur Funktionen

Diese Funktionen berechnen [*Hashes*](../secgloss/h-gly.md) von Daten und erstellen und überprüfen auch [*digitale Signaturen*](../secgloss/d-gly.md). Hashes werden auch als Message Digests bezeichnet.

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
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>Bei cryptcreatehash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt ein leeres Hash Objekt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>Cryptdestroyhash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Zerstört ein Hash Objekt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>Cryptduplialisiehash</strong></a></td>
<td>Dupliziert ein Hash Objekt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>Bei cryptgethashparam</strong></a></td>
<td>Ruft einen Hash Objekt Parameter ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>Bei CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hashwert für einen Datenblock, der dem angegebenen Hash Objekt hinzugefügt wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>Crypthashsessionkey</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hashwert für einen Sitzungsschlüssel, der dem angegebenen Hash Objekt hinzugefügt wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>Cryptabthashparam</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Legt einen Hash Objekt Parameter fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>Cryptsignhash</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Signiert das angegebene Hash Objekt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>Cryptuiwizdigitalsign</strong></a></td>
<td>Zeigt einen Assistenten an, der ein Dokument oder ein <a href="/windows/desktop/SecGloss/b-gly"><em>BLOB</em></a>digital signiert.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>Cryptuiwizfredigitalsigncontext</strong></a></td>
<td>Gibt einen Zeiger auf eine <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> -Struktur frei.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>Cryptverifysignature</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Überprüft eine digitale Signatur, wenn ein Handle für das Hash Objekt angegeben ist.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>Pfncfilterproc</strong></a></td>
<td>Filtert die Zertifikate, die im Assistenten für digitale Signaturen angezeigt werden, der von der <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>cryptuiwizdigitalsign</strong></a> -Funktion angezeigt wird.</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Zertifikat-und Zertifikat Speicherfunktionen

Zertifikat-und Zertifikat Speicherfunktionen verwalten die Verwendung, Speicherung und den Abruf von [*Zertifikaten*](../secgloss/c-gly.md), [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs). Diese Funktionen sind in die folgenden Gruppen unterteilt:

-   Zertifikat Speicherfunktionen
-   Wartungsfunktionen für Zertifikat-und Zertifikat Speicher
-   Zertifikatfunktionen
-   Funktionen der Zertifikat Sperr Liste
-   Funktionen der Zertifikat Vertrauens Liste
-   Erweiterte Eigenschaften Funktionen
-   Makecert-Funktionen

### <a name="certificate-store-functions"></a>Zertifikat Speicherfunktionen

Eine Benutzer Website kann im Laufe der Zeit viele Zertifikate sammeln. In der Regel verfügt ein Standort über Zertifikate für den Benutzer der Site sowie über andere Zertifikate, die die einzelnen Personen und Entitäten beschreiben, mit denen der Benutzer kommuniziert. Für jede Entität kann mehr als ein Zertifikat vorhanden sein. Für jedes einzelne Zertifikat muss eine Kette der Überprüfung von Zertifikaten vorhanden sein, die einen Pfad zurück zu einem vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md)bereitstellt. [*Zertifikat Speicher*](../secgloss/c-gly.md) und die zugehörigen Funktionen bieten Funktionen zum Speichern, abrufen, auflisten, überprüfen und Verwenden der in den Zertifikaten gespeicherten Informationen.

| Funktion                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certaddstoreabcollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Fügt einem Sammlungs Zertifikat Speicher einen gleich geordneten Zertifikat Speicher hinzu.                                                                                                                                                                                                                                                                       |
| [**Certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Schließt ein Zertifikat Speicher handle.                                                                                                                                                                                                                                                                                                        |
| [**Certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Ermöglicht es, eine Anwendung zu benachrichtigen, wenn es einen Unterschied zwischen dem Inhalt eines zwischengespeicherten Speichers und dem Inhalt des Speichers gibt, der im Speicher persistent gespeichert wird. Außerdem wird die Synchronisierung des zwischengespeicherten Speichers ermöglicht, falls erforderlich, und es wird eine Möglichkeit bereitzustellen, Änderungen im zwischengespeicherten Speicher im beibehaltenen Speicher zu übernehmen.<br/> |
| [**Certduplikatestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Dupliziert ein Speicher handle, indem der [*Verweis Zähler*](../secgloss/r-gly.md)inkrementiert wird.                                                                                                                                                                                            |
| [**Certenumschlag physicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Listet die physischen Speicher für einen angegebenen Systemspeicher auf.                                                                                                                                                                                                                                                                              |
| [**Certenumschlag System Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Listet alle verfügbaren Systemspeicher auf.                                                                                                                                                                                                                                                                                                   |
| [**Certenumschlag systemstoreloation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Listet alle Speicherorte auf, die über einen verfügbaren Systemspeicher verfügen.                                                                                                                                                                                                                                                                      |
| [**Certgetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Ruft eine Speicher Eigenschaft ab.                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore übergebene**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Öffnet einen Zertifikat Speicher mit einem angegebenen Speicher Anbietertyp.                                                                                                                                                                                                                                                                          |
| [**Certopeinsystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Öffnet einen Systemzertifikat Speicher, der auf einem subsystemprotokoll basiert.                                                                                                                                                                                                                                                                           |
| [**Certregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Fügt einer Auflistung von Registrierungssystem speichern einen physischen Speicher hinzu.                                                                                                                                                                                                                                                                              |
| [**Certregistersystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Registriert einen Systemspeicher.                                                                                                                                                                                                                                                                                                                 |
| [**Certremuvestorefromcollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Entfernt einen gleich geordneten Zertifikat Speicher aus einem Sammlungs Speicher.                                                                                                                                                                                                                                                                              |
| [**Certsavestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Speichert den Zertifikat Speicher.                                                                                                                                                                                                                                                                                                              |
| [**Certsetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Legt eine Speicher Eigenschaft fest.                                                                                                                                                                                                                                                                                                                    |
| [**Certunregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Entfernt einen physischen Speicher aus einer angegebenen Systemspeicher Sammlung.                                                                                                                                                                                                                                                                        |
| [**Certunregistersystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Hebt die Registrierung eines angegebenen Systemspeicher auf.                                                                                                                                                                                                                                                                                                     |
| [**Cryptuiwizexport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Zeigt einen Assistenten an, der ein Zertifikat, eine Zertifikat Vertrauens Liste (Certificate Trust List, CTL), eine Zertifikat Sperr Liste oder einen Zertifikat Speicher exportiert.                                                                                                                                                                                                      |
| [**Cryptuiwizimport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Zeigt einen Assistenten an, mit dem ein Zertifikat, eine Zertifikat Vertrauens Liste (Certificate Trust List, CTL), eine Zertifikat Sperr Liste (CRL) oder ein Zertifikat Speicher importiert werden.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Wartungsfunktionen für Zertifikat-und Zertifikat Speicher

CryptoAPI bietet eine Reihe allgemeiner Wartungsfunktionen für Zertifikat-und Zertifikat Speicher.

| Funktion                                                                                                                              | BESCHREIBUNG                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Certaddserializedelta ementtostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Fügt dem Speicher das serialisierte Zertifikat oder CRL-Element hinzu.                                   |
| [**Certkreatecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Erstellt den angegebenen Kontext aus den codierten Bytes. Der neue Kontext wird nicht in einem Speicher abgelegt. |
| [**Certenresubjetinsortedctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Listet die Vertrauens Elemente in einem sortierten CTL-Kontext auf.                                        |
| [**Certfindsubjetinctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Sucht den angegebenen Betreff in einer CTL.                                                          |
| [**Certfindsubjetinsortedctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Sucht den angegebenen Betreff in einer sortierten CTL.                                                   |
| [**Openpersonaltrustdbdialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) und [ **openpersonaltrustdbdialogex**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Zeigt das Dialogfeld **Zertifikate** an.                                                      |



 

### <a name="certificate-functions"></a>Zertifikatfunktionen

Die meisten [*Zertifikat*](../secgloss/c-gly.md) Funktionen verfügen über verwandte Funktionen, die mit [*CRLs*](../secgloss/c-gly.md) und [*CTLs*](../secgloss/c-gly.md)zu tun haben. Weitere Informationen zu verwandten CRL-und CTL-Funktionen finden Sie unter Funktionen für Zertifikat Sperr Listen und Funktionen für Zertifikat Vertrauens Listen.

| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certaddcertificatcher econtextto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Fügt dem Zertifikat Speicher einen Zertifikat Kontext hinzu.                                                                                                                                                                                            |
| [**Certaddcertifialisielinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Fügt einen Link in einem Zertifikat Speicher einem Zertifikat Kontext in einem anderen Speicher hinzu.                                                                                                                                                               |
| [**Bei CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Konvertiert das codierte Zertifikat in einen Zertifikat Kontext und fügt dann dem Zertifikat Speicher den Kontext hinzu.                                                                                                                                  |
| [**Certadresssserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Erhöht den Verweis Zähler für ein **hcert- \_ Server- \_ OCSP- \_ Antwort** handle.                                                                                                                                                                 |
| [**Certadressvolltext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Erhöht den Verweis Zähler für eine [**Zertifikat \_ Server- \_ OCSP- \_ Antwort \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context) Struktur.                                                                                                              |
| [**Certcloseserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Schließt ein OCSP-Serverantwort handle ( [*Online Certificate Status Protocol*](../secgloss/o-gly.md) ).                                               |
| [**Certkreatecertifi-Econtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Erstellt einen Zertifikat Kontext aus einem codierten Zertifikat. Der erstellte Kontext wird nicht in einem Zertifikat Speicher abgelegt.                                                                                                                               |
| [**Certkreateselfsigncertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | Erstellen eines selbstsignierten Zertifikats                                                                                                                                                                                                              |
| [**Certdeletecertifipeefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Löscht ein Zertifikat aus dem Zertifikat Speicher.                                                                                                                                                                                               |
| [**Certduplierecertifi-Econtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Dupliziert einen Zertifikat Kontext, indem der [*Verweis Zähler*](../secgloss/r-gly.md)erhöht wird.                                                                                           |
| [**Certenrecertifieresinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Listet die Zertifikat Kontexte im Zertifikat Speicher auf.                                                                                                                                                                                   |
| [**Certfindcertifi. Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Sucht den ersten oder nächsten Zertifikat Kontext im Zertifikat Speicher, der einem Suchkriterium entspricht.                                                                                                                                           |
| [**Certfreecertififeecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Gibt einen Zertifikat kontextfrei.                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Ruft einen Zertifikat Kontext aus dem Zertifikat Speicher für den ersten oder nächsten Aussteller des angegebenen Antragsteller Zertifikats ab.                                                                                                                      |
| [**Certgetserverocspresponsecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Ruft eine nicht blockierende, Zeit gültige OCSP-Antwort Kontext ( [*Online Certificate Status Protocol*](../secgloss/o-gly.md) ) für das angegebene Handle ab. |
| [**Certgetsubjetcertifipeefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Ruft den Zertifikat Speicher des Antragstellers aus dem Zertifikat Speicher ab, der durch seinen Aussteller und seine Seriennummer eindeutig identifiziert wird.                                                                                                                  |
| [**Certgetvalidumps**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Gibt ein Array von Verwendungen zurück, die aus der Schnittmenge der gültigen Verwendungen für alle Zertifikate in einem Array von Zertifikaten bestehen.                                                                                                               |
| [**Certoptserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Öffnet ein Handle für eine OCSP-Antwort ( [*Online Certificate Status-Protokoll*](../secgloss/o-gly.md) ), die einer Serverzertifikat Kette zugeordnet ist.       |
| [**Certretrievelogoorbiometricinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Führt einen URL-Abruf von Logos oder biometrischen Informationen aus, die entweder in der **szoid- \_ Logotype \_** -oder **szoid- \_ Biometrie \_** -Zertifikats Erweiterung angegeben sind.                                                                                  |
| [**Certselectcertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Zeigt ein Dialogfeld an, in dem der Benutzerzertifikate aus einer Gruppe von Zertifikaten auswählen kann, die einem bestimmten Kriterium entsprechen.                                                                                                                       |
| [**Certselectcertificatechain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Ruft Zertifikat Ketten auf der Grundlage der angegebenen Auswahlkriterien ab.                                                                                                                                                                             |
| [**Certselectiongetserializedblob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Eine Hilfsfunktion, die verwendet wird, um ein serialisiertes [*zertifikatblob*](../secgloss/b-gly.md) aus einer [**CERT \_ selectui- \_ Eingabe**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input) Struktur abzurufen.                                               |
| [**Certserializecertifikatestoreelement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Serialisiert das verschlüsselte Zertifikat eines Zertifikat Kontexts und eine codierte Darstellung seiner Eigenschaften.                                                                                                                                         |
| [**Bei CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Führt die aktivierten überprüfungsprüfungen für das Antragsteller Zertifikat mithilfe des Ausstellers aus.                                                                                                                                                           |
| [**Cryptuidlgcertmgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Zeigt ein Dialogfeld an, in dem der Benutzerzertifikate verwalten kann.                                                                                                                                                                              |
| [**Cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md)                   | Zeigt ein Dialogfeld an, in dem Benutzer ein Zertifikat auswählen können.                                                                                                                                                                               |
| [**Cryptuidlgselectcertifipeefromstore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Zeigt ein Dialogfeld an, in dem ein Zertifikat aus einem angegebenen Speicher ausgewählt werden kann.                                                                                                                                                        |
| [**Cryptuidlgviewcertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Zeigt ein Dialogfeld an, in dem ein bestimmtes Zertifikat angezeigt wird.                                                                                                                                                                                    |
| [**Cryptuidlgviewcontext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Zeigt ein Zertifikat, eine CRL oder eine CTL an.                                                                                                                                                                                                            |
| [**Cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md)                         | Zeigt ein Dialogfeld an, in dem die Signatur Geber Informationen für eine signierte Nachricht enthalten sind.                                                                                                                                                                |
| [**Getfriendlynameof-Zertifikat**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Ruft den anzeigen Amen für ein Zertifikat ab.                                                                                                                                                                                                   |
| [**Rkeyclosekeyservice**](rkeyclosekeyservice.md)                                   | Schließt ein Schlüsseldienst handle.                                                                                                                                                                                                                    |
| [**Rkeyopenkeyservice**](rkeyopenkeyservice.md)                                     | Öffnet ein Schlüsseldienst Handle auf einem Remote Computer.                                                                                                                                                                                                |
| [**Rkeypfxinstall**](rkeypfxinstall.md)                                             | Hiermit wird ein Zertifikat auf einem Remote Computer installiert.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Funktionen der Zertifikat Sperr Liste

Diese Funktionen verwalten die Speicherung und den Abruf von [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs).

| Funktion                                                             | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certaddcrlcontextflistore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Fügt dem Zertifikat Speicher einen CRL-Kontext hinzu.                                                                                                                                          |
| [**Certaddcrllinkto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Fügt einem CRL-Kontext in einem anderen Speicher einen Link in einem Speicher hinzu.                                                                                                                         |
| [**Certaddencodedcrldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Konvertiert die codierte CRL in einen CRL-Kontext und fügt dann dem Zertifikat Speicher den Kontext hinzu.                                                                                        |
| [**Certkreatecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Erstellt einen CRL-Kontext aus einer codierten CRL. Der erstellte Kontext wird nicht in einem Zertifikat Speicher abgelegt.                                                                                     |
| [**Certdeletecrlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Löscht eine CRL aus dem Zertifikat Speicher.                                                                                                                                             |
| [**Certduplierecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Dupliziert einen CRL-Kontext, indem der [*Verweis Zähler*](../secgloss/r-gly.md)inkrementiert wird.                                         |
| [**Certenrecrlsinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Listet die CRL-Kontexte in einem Speicher auf.                                                                                                                                               |
| [**Certfindcertificr eincrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Durchsucht die [*Zertifikat Sperr Liste*](../secgloss/c-gly.md) nach dem angegebenen Zertifikat. |
| [**Certfindcrlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Sucht den ersten oder nächsten CRL-Kontext im Zertifikat Speicher, der einem bestimmten Kriterium entspricht.                                                                                     |
| [**Certfreecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Gibt einen CRL-kontextfrei.                                                                                                                                                                  |
| [**Certgetcrlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Ruft den ersten oder nächsten CRL-Kontext aus dem Zertifikat Speicher für das angegebene Aussteller Zertifikat ab.                                                                                 |
| [**Certserializecrlstoreelement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Serialisiert die codierte CRL und deren Eigenschaften des CRL-Kontexts.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Funktionen der Zertifikat Vertrauens Liste

Diese Funktionen verwalten die Speicherung und den Abruf von [*Zertifikat Vertrauens Listen (Certificate Trust Lists*](../secgloss/c-gly.md) , CTLs).

| Funktion                                                               | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Certaddctlcontextto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Fügt dem Zertifikat Speicher einen CTL-Kontext hinzu.                                                                         |
| [**Certaddctllinkto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Fügt einem CRL-Kontext in einem anderen Speicher einen Link in einem Speicher hinzu.                                                        |
| [**Certaddencodedctldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Konvertiert die codierte CTL in einen CTL-Kontext und fügt dann dem Zertifikat Speicher den Kontext hinzu.                       |
| [**Certkreatectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Erstellt einen CTL-Kontext aus einer codierten Zertifikats Vertrauens Liste. Der erstellte Kontext wird nicht in einem Zertifikat Speicher abgelegt. |
| [**Certdeletectlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Löscht eine CTL aus dem Zertifikat Speicher.                                                                            |
| [**Certduplierectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Dupliziert einen CTL-Kontext, indem der Verweis Zähler inkrementiert wird.                                                        |
| [**Certenumschlag ctlsinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Listet die CTL-Kontexte im Zertifikat Speicher auf.                                                                |
| [**Certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Sucht den ersten oder nächsten CTL-Kontext im Zertifikat Speicher, der einem bestimmten Kriterium entspricht.                     |
| [**Certfreectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Gibt einen CTL-kontextfrei.                                                                                                 |
| [**Certmodifycertifikatestotrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Ändert den Satz von Zertifikaten in einer CTL für einen bestimmten Zweck.                                                       |
| [**Certserializectlstoreelement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Serialisiert die codierte CTL und deren Eigenschaften des CTL-Kontexts.                                                         |



 

### <a name="extended-property-functions"></a>Erweiterte Eigenschaften Funktionen

Die folgenden Funktionen funktionieren mit erweiterten Eigenschaften von Zertifikaten, CRLs und CTLs.

| Funktion                                                                             | BESCHREIBUNG                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Certenrecertifiaseecontextproperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Listet die Eigenschaften für den angegebenen Zertifikat Kontext auf. |
| [**Certenrecrlcontextproperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Listet die Eigenschaften für den angegebenen CRL-Kontext auf.         |
| [**Certenumschlag ctlcontextproperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Listet die Eigenschaften für den angegebenen CTL-Kontext auf.         |
| [**Certgetcertifi-econtextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Ruft Zertifikat Eigenschaften ab.                                |
| [**Certgetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Ruft CRL-Eigenschaften ab.                                        |
| [**Certgetctlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Ruft CTL-Eigenschaften ab.                                        |
| [**Certsetcertifi-econtextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Legt Zertifikat Eigenschaften fest.                                     |
| [**Certsetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Legt CRL-Eigenschaften fest.                                             |
| [**Certsetctlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Legt CTL-Eigenschaften fest.                                             |



 

## <a name="makecert-functions"></a>Makecert-Funktionen

Die folgenden Funktionen unterstützen das [Makecert](makecert.md) -Tool.



| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Freecryptprovfromcert**](freecryptprovfromcert.md)                                 | Gibt das Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) frei und löscht optional den temporären Container, der von der [**getcryptprovfromcert**](getcryptprovfromcert.md) -Funktion erstellt wurde. |
| [**Getcryptprovfromcert**](getcryptprovfromcert.md)                                   | Ruft ein Handle für einen CSP und eine Schlüssel Spezifikation für einen Zertifikat Kontext ab.                                                                                                                                                                                                                                |
| [**Pvkfreecryptprov**](pvkfreecryptprov.md)                                           | Gibt das Handle für einen CSP frei und löscht optional den temporären Container, der von der [**pvkgetcryptprov**](pvkgetcryptprov.md) -Funktion erstellt wurde.                                                                                                                                                          |
| [**Pvkgetcryptprov**](pvkgetcryptprov.md)                                             | Ruft ein Handle für einen CSP auf der Grundlage eines Datei namens für den [*privaten Schlüssel*](../secgloss/p-gly.md) oder eines Schlüssel Container namens ab.                                                                                                                                          |
| [**Pvkprivatekeyacquirecontextfrommemory**](pvkprivatekeyacquirecontextfrommemory.md) | Erstellt einen temporären Container im CSP und lädt einen privaten Schlüssel aus dem Arbeitsspeicher in den Container.                                                                                                                                                                                                         |
| [**Pvkprivatekeysave**](pvkprivatekeysave.md)                                         | Speichert einen privaten Schlüssel und den zugehörigen [*öffentlichen Schlüssel*](../secgloss/p-gly.md) in einer angegebenen Datei.                                                                                                                                                          |
| [**Signror**](signerror.md)                                                         | Ruft [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf und konvertiert den Rückgabecode in ein **HRESULT**.                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Funktionen zur Zertifikat Überprüfung

Zertifikate werden mithilfe von [*CTLs*](../secgloss/c-gly.md) oder Zertifikat Ketten überprüft. Für beide werden Funktionen bereitgestellt:

-   Überprüfungs Funktionen mit CTLs
-   Funktionen zur Überprüfung der Zertifikat Kette

### <a name="verification-functions-using-ctls"></a>Überprüfungs Funktionen mit CTLs

Diese Funktionen verwenden CTLs im Überprüfungsprozess. Weitere Funktionen für die Arbeit mit CTLs finden Sie unter Funktionen für Zertifikat Vertrauens Listen und erweiterte Eigenschafts Funktionen.

Die folgenden Funktionen verwenden CTLs direkt für die Überprüfung.

| Funktion                                                         | BESCHREIBUNG                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**Certverifyctlusage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Überprüft die Verwendung einer CTL.                 |
| [**Cryptmsgencodeandsignctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Codiert und signiert eine CTL als Nachricht.        |
| [**Cryptmsggetandverifysigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Ruft eine CTL aus einer Meldung ab und überprüft sie. |
| [**Cryptmsgsignctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Signiert eine Nachricht, die eine CTL enthält.         |



 

### <a name="certificate-chain-verification-functions"></a>Funktionen zur Überprüfung der Zertifikat Kette

Zertifikat Ketten werden erstellt, um Vertrauens Informationen über einzelne Zertifikate bereitzustellen.

| Funktionsname                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certkreatecertificatechainengine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Erstellt eine neue, nicht standardmäßige Ketten-Engine für eine Anwendung.                                                                                                                                                          |
| [**Certkreatectlentryfromcertifiaseecontextproperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Erstellt einen CTL-Eintrag, dessen Attribute den Eigenschaften des Zertifikat Kontexts entsprechen.                                                                                                                                      |
| [**Certduplicatecertificatechain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Dupliziert eine Zertifikatskette, indem der [*Verweis Zähler*](../secgloss/r-gly.md) der Kette erhöht und ein Zeiger auf die Kette zurückgegeben wird.                    |
| [**Certfindchaininstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Sucht den ersten oder nächsten Zertifikat Ketten Kontext in einem Speicher.                                                                                                                                                     |
| [**Certfreecertificatechain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Gibt eine Zertifikat Kette frei, indem der Verweis Zähler reduziert wird.                                                                                                                                                          |
| [**Certfreecertificatechainengine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Gibt ein nicht standardmäßiges Zertifikat Ketten Modul frei.                                                                                                                                                                        |
| [**Certfreecertificatechainlist**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Gibt das Array von Zeigern auf Ketten Kontexte frei.                                                                                                                                                                      |
| [**CertGetCertificateChain dokumentiert**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Erstellt einen Ketten Kontext beginnend mit einem Endzertifikat und geht, wenn möglich, zu einem vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md)zurück.                |
| [**Certisvalidcrlforcertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Überprüft eine Zertifikat Sperr Liste, um zu bestimmen, ob Sie ein bestimmtes Zertifikat enthalten [*würde, wenn*](../secgloss/c-gly.md) dieses Zertifikat widerrufen wurde. |
| [**Certsetcertifierecontextpropertiesfromctlentry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Legt Eigenschaften für den Zertifikat Kontext mithilfe der Attribute im CTL-Eintrag fest.                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Überprüft eine Zertifikat Kette, um deren Gültigkeit zu überprüfen, einschließlich der Konformität mit angegebenen Kriterien für die Gültigkeits Richtlinie.                                                                                            |



 

## <a name="message-functions"></a>Nachrichtenfunktionen

[*CryptoAPI*](../secgloss/c-gly.md) -Nachrichten Funktionen bestehen aus zwei Funktionsgruppen: auf Low-Level-Nachrichten Funktionen und [*vereinfachten Nachrichten Funktionen*](../secgloss/s-gly.md).

-Nachrichten Funktionen auf niedriger Ebene erstellen und arbeiten direkt mit PKCS \# 7-Nachrichten. Diese Funktionen codieren PKCS \# 7-Daten für die Übertragung und Decodierung von PKCS 7-Daten, die \# empfangen wurden. Außerdem werden die Signaturen empfangener Nachrichten entschlüsselt und überprüft. Eine Übersicht über die PKCS \# 7-Standard-und Low-Level-Meldungen finden Sie unter [Nachrichten auf niedriger Ebene](low-level-messages.md).

Vereinfachte Nachrichten Funktionen befinden sich auf einer höheren Ebene und Wrappen mehrere Low-Level-Nachrichten Funktionen und Zertifikat Funktionen in einzelne Funktionen, die eine bestimmte Aufgabe auf bestimmte Weise ausführen. Diese Funktionen reduzieren die Anzahl von Funktionsaufrufen, die zum Ausführen einer Aufgabe erforderlich sind, wodurch die Verwendung der kryptoapi vereinfacht wird. Eine Übersicht über vereinfachte Meldungen finden Sie unter [vereinfachte nach](simplified-messages.md)richten.

-   Nachrichten Funktionen auf niedriger Ebene
-   Vereinfachte Nachrichten Funktionen

### <a name="low-level-message-functions"></a>Nachrichten Funktionen auf niedriger Ebene

Nachrichten auf niedriger Ebene bieten die Funktionalität, die zum Codieren von Daten für die Übertragung und zum Decodieren von PKCS \# 7-Nachrichten erforderlich ist. Funktionalität wird auch zum Entschlüsseln und Überprüfen der Signaturen empfangener Nachrichten bereitgestellt. Die Verwendung dieser Low-Level-Nachrichten Funktionen in den meisten Anwendungen wird nicht empfohlen. Bei den meisten Anwendungen wird die Verwendung von vereinfachten Nachrichten Funktionen, die mehrere Low-Level-Nachrichten Funktionen in einen einzelnen Funktions aufzurufen einschließen, bevorzugt.

| Funktion                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cryptmsgcalculateencodecodlength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Berechnet die Länge einer codierten kryptografienachricht.                                                                                                                                                                     |
| [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Schließt ein Handle einer kryptografischen Nachricht.                                                                                                                                                                                    |
| [**Cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Führt eine spezielle Steuerungsfunktion nach dem endgültigen [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einer codierten oder decodierten kryptografiemeldung aus.                                                                                   |
| [**Cryptmsgcountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Signiert eine bereits vorhandene Signatur in einer Nachricht gegen.                                                                                                                                                                       |
| [**Cryptmsgcountersignencoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Signiert eine bereits vorhandene Signatur (codierte SignerInfo, wie von PKCS \# 7 definiert).                                                                                                                                       |
| [**Cryptmsgduplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Dupliziert ein kryptografisches Nachrichten handle, indem der [*Verweis Zähler*](../secgloss/r-gly.md)inkrementiert wird. Der Verweis Zähler verfolgt die Lebensdauer der Nachricht. |
| [**Cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Ruft einen Parameter ab, nachdem eine kryptografiemeldung codiert oder decodiert wurde.                                                                                                                                                       |
| [**Cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Öffnet eine kryptografiemeldung zum Decodieren.                                                                                                                                                                                    |
| [**Cryptmsgopentoen-Code**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Öffnet eine kryptografiemeldung für die Codierung.                                                                                                                                                                                    |
| [**Cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Aktualisiert den Inhalt einer kryptografischen Nachricht.                                                                                                                                                                               |
| [**Cryptmsgverifycountersignaturecodiertes**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Überprüft eine [*gegen Signatur*](../secgloss/c-gly.md) in Bezug auf die SignerInfo-Struktur (wie von PKCS \# 7 definiert).                                                   |
| [**Cryptmsgverifycountersignatureencoderdex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Überprüft, ob der *pbsignerinfocountersignature* -Parameter den verschlüsselten [*Hash*](../secgloss/h-gly.md) des Felds " **verschlüsselteddigest** " der *pbsignerinfo* -Parameter Struktur enthält.   |



 

### <a name="simplified-message-functions"></a>Vereinfachte Nachrichten Funktionen

[*vereinfachte Nachrichten Funktionen*](../secgloss/s-gly.md) schließen Low-Level-Nachrichten Funktionen in eine einzelne Funktion ein, um eine bestimmte Aufgabe auszuführen.

| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cryptdecodemess**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Decodiert eine kryptografische Nachricht.                                                                                                                                                                                                                                             |
| [**Cryptdecryptandveriatymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Entschlüsselt die angegebene Nachricht und überprüft den Signatur Geber.                                                                                                                                                                                                                     |
| [**Cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Entschlüsselt die angegebene Meldung.                                                                                                                                                                                                                                              |
| [**Cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Verschlüsselt die Nachricht für den Empfänger oder die Empfänger.                                                                                                                                                                                                                        |
| [**Cryptgetmessagezertifikate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Gibt den [*Zertifikat Speicher*](../secgloss/c-gly.md) zurück, der die Zertifikate und [*CRLs*](../secgloss/c-gly.md)der Nachricht enthält. |
| [**Cryptgetmessagesignercount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Gibt die Anzahl der Signatur Geber in der signierten Nachricht zurück.                                                                                                                                                                                                                          |
| [**Crypthashmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Erstellt einen Hash der Nachricht.                                                                                                                                                                                                                                               |
| [**Cryptsignandverschlüsseltmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Signiert die Nachricht und verschlüsselt Sie dann für den Empfänger oder die Empfänger.                                                                                                                                                                                                     |
| [**Cryptsignmessagewithkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Signiert eine Meldung mithilfe des privaten Schlüssels eines CSP, der in den Parametern der Funktion angegeben ist.                                                                                                                                                                                       |
| [**Cryptsignmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Signiert die Meldung.                                                                                                                                                                                                                                                           |
| [**Cryptverifydetachedmessagehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Überprüft eine Hash Nachricht, die einen getrennten Hash enthält.                                                                                                                                                                                                                     |
| [**Cryptverifydetachedmessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Überprüft eine signierte Meldung, die eine getrennte Signatur oder Signaturen enthält.                                                                                                                                                                                                  |
| [**Cryptveritymessagehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Überprüft eine Hashnachricht.                                                                                                                                                                                                                                                   |
| [**Cryptveriatymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Überprüft eine signierte Meldung.                                                                                                                                                                                                                                                   |
| [**Cryptveritymessagesignaturewithkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Überprüft die Signatur einer signierten Nachricht mithilfe der angegebenen Informationen zum öffentlichen Schlüssel.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Hilfsfunktionen

Die zusätzlichen Funktionen werden wie folgt gruppiert:

-   Datenverwaltung Funktionen
-   Daten Konvertierungs Funktionen
-   Erweiterte Schlüssel Verwendungs Funktionen
-   Schlüsselbezeichnerfunktionen
-   OID-Unterstützungsfunktionen
-   Funktionen zum Abrufen von Remote Objekten
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
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>Certcomparecertificate</strong></a></td>
<td>Vergleicht zwei Zertifikate, um zu bestimmen, ob Sie identisch sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>Certcomparecertificatcher Name</strong></a></td>
<td>Vergleicht zwei Zertifikat Namen, um zu bestimmen, ob diese identisch sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>Certcompareintegerblob</strong></a></td>
<td>Vergleicht zwei ganzzahlige <a href="/windows/desktop/SecGloss/b-gly"><em>blobzahlen</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>Certcomparepublickeyinfo</strong></a></td>
<td>Vergleicht zwei <a href="/windows/desktop/SecGloss/p-gly"><em>öffentliche Schlüssel</em></a> , um zu bestimmen, ob diese identisch sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>Certfindattribute</strong></a></td>
<td>Sucht das erste Attribut, das durch seinen <a href="/windows/desktop/SecGloss/o-gly"><em>Objekt Bezeichner</em></a> (OID) identifiziert wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>Certfindextension</strong></a></td>
<td>Sucht die erste durch die OID identifizierte Erweiterung.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>Certfindrdnattr</strong></a></td>
<td>Sucht das erste von seiner OID identifizierte <a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a> -Attribut in der Namensliste der <em>relativen Distinguished Names</em>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>Certgetintenentdkeyusage</strong></a></td>
<td>Ruft die vorgesehenen Schlüssel Verwendungs Bytes aus dem Zertifikat ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>Certgetpublickeylength</strong></a></td>
<td>Ruft die Bit-Länge des öffentlichen/privaten Schlüssels aus dem <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB des öffentlichen Schlüssels</em></a>ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>Certisrdnattrsincertifisrename</strong></a></td>
<td>Vergleicht die Attribute im <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifikat Namen</em></a> mit dem angegebenen <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>CERT_RDN</strong></a> , um zu bestimmen, ob dort alle Attribute enthalten sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>Certishochashanmeldungs-Signatur</strong></a></td>
<td>Bestimmt, ob der angegebene Hash Algorithmus und der öffentliche Schlüssel im Signaturzertifikat verwendet werden können, um eine starke Signatur auszuführen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>Certverifycrllock</strong></a></td>
<td>Überprüft, ob das Antragsteller Zertifikat nicht in der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifikat Sperr Liste</em></a> (CRL) enthalten ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>Certverifycrltimegültigkeit</strong></a></td>
<td>Überprüft die Gültigkeitsdauer einer CRL.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>Certverifywiderruf</strong></a></td>
<td>Überprüft, ob sich das Zertifikat des Antragstellers nicht auf der CRL befindet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>Certverifytimegültigkeit</strong></a></td>
<td>Überprüft die Gültigkeitsdauer eines Zertifikats.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>Certverifyvaliditynist</strong></a></td>
<td>Überprüft, ob die Gültigkeitsdauer des Subjekts innerhalb der Gültigkeitsdauer des Ausstellers geschachtelt ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Diese Funktion wird durch die <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a> -Funktion ersetzt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Exportiert den privaten Schlüssel im PKCS-#8 Format.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>Bei CryptExportPublicKeyInfo</strong></a></td>
<td>Exportiert die Informationen des öffentlichen Schlüssels, die mit dem entsprechenden privaten Schlüssel des Anbieters verknüpft sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>Cryptexportpublickeyinfoex</strong></a></td>
<td>Exportiert die Informationen des öffentlichen Schlüssels, die mit dem entsprechenden privaten Schlüssel des Anbieters verknüpft sind. Diese Funktion unterscheidet sich von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> darin, dass der Benutzer den Algorithmus für öffentliche Schlüssel angeben kann, wodurch der vom CSP bereitgestellte Standardwert überschrieben wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>Cryptexportpublickeyinfofrombcryptkeyhandle</strong></a></td>
<td>Exportiert die öffentlichen Schlüsselinformationen, die mit dem entsprechenden privaten Schlüssel eines Anbieters verknüpft sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>Cryptfindcertificatekeyprovinfo</strong></a></td>
<td>Listet die Kryptografieanbieter und Ihre <a href="/windows/desktop/SecGloss/k-gly"><em>Schlüssel Container</em></a> auf, um den privaten Schlüssel zu finden, der dem öffentlichen Schlüssel eines Zertifikats entspricht.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>Cryptfindlocalizedname</strong></a></td>
<td>Sucht den lokalisierten Namen für einen angegebenen Namen, z. b. sucht nach dem lokalisierten Namen des Speicher namens des Stamm Systems.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>Crypthashcertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Hashes des codierten Inhalts.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Hashes eines Datenblocks mithilfe eines CNG-Hash Anbieters (Cryptography API: Next Generation).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>Crypthashpublickeyinfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Berechnet den Hash der codierten Informationen zum öffentlichen Schlüssel.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>Crypthashrebesigned</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Berechnet den Hash von, der als &quot; signierte &quot; Informationen im codierten signierten Inhalt (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>) signiert werden soll.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Importiert den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a> im PKCS-#8 Format in einen <a href="/windows/desktop/SecGloss/c-gly"><em>Kryptografiedienstanbieter</em></a> (CSP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>Cryptimportpublickeyinfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Konvertiert und importiert Informationen des öffentlichen Schlüssels in den Anbieter und gibt ein Handle des öffentlichen Schlüssels zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Konvertiert und importiert die Informationen des öffentlichen Schlüssels in den Anbieter und gibt ein Handle des öffentlichen Schlüssels zurück. Zusätzliche Parameter (über die von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>cryptimportpublickeyinfo</strong></a>festgelegte), die zum Überschreiben von Standardwerten verwendet werden können, werden zur Ergänzung <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>bereitgestellt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Importiert einen öffentlichen Schlüssel in einen asymmetrischen CNG-Anbieter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>Cryptmemzuweisung</strong></a></td>
<td>Weist Speicher für einen Puffer zu. Dieser Arbeitsspeicher wird von allen crypt32. lib-Funktionen verwendet, die zugeordnete Puffer zurückgeben.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>Cryptmemfree</strong></a></td>
<td>Gibt den von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>cryptmemzuzugeordneten</strong></a> und <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>cryptmemrebelegc</strong></a>zugeordneten Arbeitsspeicher frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>Cryptmemrezuweisung</strong></a></td>
<td>Gibt Arbeitsspeicher frei, der derzeit für einen Puffer reserviert ist, und ordnet Speicher für einen neuen Puffer zu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft Informationen zum Inhalt eines BLOBs oder einer Datei ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>Bei cryptsignandencodecertificate</strong></a></td>
<td>Codiert als &quot; signierte &quot; Informationen, signiert diese codierten Informationen und codiert die resultierenden signierten Informationen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>Cryptsigncertificate</strong></a></td>
<td>Signiert die als &quot; signierte &quot; Informationen in den codierten, signierten Inhalt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>Cryptsipaddprovider</strong></a></td>
<td>Fügt ein Subject Interface Package (SIP) hinzu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>Cryptsipkreatone directdata</strong></a></td>
<td>Gibt eine <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a> -Struktur zurück, die einen <a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> der angegebenen <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a> Struktur, des Digest-Algorithmus und eines Codierungs Attributs enthält. Der Hash kann als indirekter Verweis auf die Daten verwendet werden.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>Cryptsipgetcaps</strong></a></td>
<td>Ruft die Funktionen eines SIP ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>Cryptsipgetsigneddatamsg</strong></a></td>
<td>Ruft eine Authenticode-Signatur aus der Datei ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>Cryptsipload</strong></a></td>
<td>Lädt die Dynamic Link Library, die ein Subjekt Schnittstellen Paket implementiert, und weist entsprechende Bibliotheks Exportfunktionen einer <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> -Struktur zu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>Cryptsipputsigneddatamsg</strong></a></td>
<td>Speichert eine Authenticode-Signatur in der Zieldatei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>Cryptsipremuveprovider</strong></a></td>
<td>Entfernt einen SIP, der durch einen vorherigen-Rückruf der <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>cryptsipaddprovider</strong></a> -Funktion hinzugefügt wurde.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>Cryptsipremuvesigneddatamsg</strong></a></td>
<td>Entfernt eine angegebene Authenticode-Signatur.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>Cryptsipreidevesubjectguid</strong></a></td>
<td>Ruft eine GUID basierend auf den Header Informationen in einer angegebenen Datei ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>Cryptsiprezevesubjectguidforcatalogfile</strong></a></td>
<td>Ruft die der angegebenen Datei zugeordnete Betreff-GUID ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>Cryptsipverifyderetdata</strong></a></td>
<td>Überprüft die indirekten Hash Daten anhand des angegebenen Subjekts.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>Cryptupdateprotectedstate</strong></a></td>
<td>Migriert die Hauptschlüssel des aktuellen Benutzers, nachdem sich die <a href="/windows/desktop/SecGloss/s-gly"><em>Sicherheits</em></a> -ID (SID) des Benutzers geändert hat.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>Cryptverifycertificatesignature</strong></a></td>
<td>Überprüft die Signatur eines Antragsteller Zertifikats <a href="/windows/desktop/SecGloss/c-gly"><em>oder einer Zertifikat Sperr Liste anhand der</em></a> Informationen zum öffentlichen Schlüssel.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>Cryptverifycertificatesignatureex</strong></a></td>
<td>Eine erweiterte Version von <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>cryptverifycertificatesignature</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>Getencschannel</strong></a></td>
<td>Speichert den verschlüsselten Inhalt der Schannel-dll im Arbeitsspeicher.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pcryptsipgetcaps</strong></a></td>
<td>Wird von einem SIP zum Melden von Funktionen implementiert.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Daten Konvertierungs Funktionen

Die folgenden CryptoAPI-Funktionen konvertieren zertifikatstrukturmember in verschiedene Formen.

| Funktion                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certalgidttoid**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Konvertiert einen kryptografiealgorithmusbezeichner (ALG- \_ ID) in eine [*abstrakte Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) [*Object Identifier*](../secgloss/o-gly.md) -Zeichenfolge (OID). |
| [**Certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Ruft den Antragsteller-oder Aussteller Namen aus einem Zertifikat ab und konvertiert ihn in eine mit NULL endenden Zeichenfolge.                                                                                                                                                                                                               |
| [**Certnametostr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Konvertiert ein [*zertifikatnamensblob*](../secgloss/b-gly.md) in eine NULL terminierte Zeichenfolge.                                                                                                                                                                                                      |
| [**Certoidtoalgid**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Konvertiert die ASN. 1-objektbezeichnerzeichenfolge in den CSP-Algorithmus Bezeichner.                                                                                                                                                                                                                                                 |
| [**Certrdnvaluetostr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Konvertiert einen namens Wert in eine NULL-terminierte Zeichenfolge.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Konvertiert eine mit NULL endend beendete [*X. 500*](../secgloss/x-gly.md) -Zeichenfolge in einen codierten Zertifikat Namen.                                                                                                                                                                                          |
| [**Cryptbinarydestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Konvertiert eine binäre Sequenz in eine formatierte Zeichenfolge.                                                                                                                                                                                                                                                                          |
| [**Cryptformatobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Formatiert codierte Daten und gibt eine Unicode-Zeichenfolge zurück.                                                                                                                                                                                                                                                                          |
| [**Cryptstringto Binary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Konvertiert eine formatierte Zeichenfolge in eine binäre Sequenz.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Erweiterte Schlüssel Verwendungs Funktionen

Die folgenden Funktionen behandeln die erweiterte [*Schlüssel Verwendungs Erweiterung (Enhanced Key Usage*](../secgloss/e-gly.md) , EKU) und die erweiterte EKU-Eigenschaft von Zertifikaten. Mit der EKU-Erweiterung und der erweiterten Eigenschaft wird die gültige Verwendung eines Zertifikats angegeben und eingeschränkt. Die Erweiterungen sind Teil des Zertifikats selbst. Sie werden vom Aussteller des Zertifikats festgelegt und sind schreibgeschützt. Zertifikat: Erweiterte Eigenschaften sind Werte, die einem Zertifikat zugeordnet sind, das in einer Anwendung festgelegt werden kann.

| Funktion                                                                             | BESCHREIBUNG                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Certaddenhancedkeyus-ageidentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Fügt der EKU-Eigenschaft eines Zertifikats einen Verwendungs Bezeichner hinzu.                       |
| [**Certgetenhancedkeyusage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Ruft von einem Zertifikat Informationen über die EKU-Erweiterung oder-Eigenschaft ab. |
| [**Certremuveenhancedkeyceandentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Entfernt den Verwendungs Bezeichner aus der erweiterten EKU-Eigenschaft eines Zertifikats.       |
| [**Certstenhancedkeyusage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Legt die EKU-Eigenschaft für ein Zertifikat fest.                                       |



 

### <a name="key-identifier-functions"></a>Schlüsselbezeichnerfunktionen

Mit schlüsselbezeichnerfunktionen kann der Benutzer einen Schlüssel Bezeichner oder seine Eigenschaften erstellen, festlegen, Abrufen oder suchen.

Ein Schlüssel Bezeichner ist der eindeutige Bezeichner eines [*öffentlichen/privaten Schlüssel Paars*](../secgloss/p-gly.md). Dabei kann es sich um einen beliebigen eindeutigen Bezeichner handeln, aber in der Regel handelt es sich dabei um den 20-Byte-SHA1-Hash einer codierten [**Zertifikat \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) Ein Schlüssel Bezeichner kann durch die Zertifikat-ID der Zertifikat Schlüssel Kennung des Zertifikats abgerufen werden \_ \_ \_ \_ . Der Schlüssel Bezeichner ermöglicht die Verwendung dieses [*Schlüssel Paars*](../secgloss/k-gly.md) zum Verschlüsseln und Entschlüsseln von Nachrichten ohne Verwendung des Zertifikats.

Schlüssel Bezeichner sind nicht mit [*CRLs*](../secgloss/c-gly.md) oder [*CTLs*](../secgloss/c-gly.md)verknüpft.

Ein Schlüssel Bezeichner kann die gleichen Eigenschaften wie ein Zertifikat Kontext haben. Weitere Informationen finden Sie unter [**certkreatecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

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
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>Cryptkreatekeyidentifierfromcsp</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Erstellt einen Schlüssel Bezeichner aus dem <a href="/windows/desktop/SecGloss/p-gly"><em>BLOB des öffentlichen Schlüssels</em></a>eines CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>Cryptenrekeyidentifierproperties</strong></a></td>
<td>Listet die Schlüssel Bezeichner und ihre Eigenschaften auf.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>Cryptgetkeyidentifierproperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Ruft eine bestimmte Eigenschaft von einem angegebenen Schlüssel Bezeichner ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>Cryptsetkeyidentifierproperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Diese API ist veraltet. Neue und vorhandene Software sollten mit der Verwendung von <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation-APIs beginnen.</a> Microsoft kann diese API in zukünftigen Versionen entfernen.
</blockquote>
<br/> Legt eine Eigenschaft eines angegebenen Schlüssel Bezeichners fest.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>OID-Unterstützungsfunktionen

Diese Funktionen bieten Unterstützung für [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID). Diese Funktionen installieren, registrieren und verteilen in OID und Codieren typspezifische Funktionen.

Die folgenden CryptoAPI-Funktionen verwenden diese OID-Unterstützungsfunktionen:

-   [**Bei cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**Cryptencodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**Cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**Cryptdecodeobjectex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**Certverifywiderruf**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore übergebene**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Eine Übersicht über diesen Prozess finden Sie unter [Erweitern der kryptoapi-Funktionalität](extending-cryptoapi-functionality.md).

Die folgenden Funktionen können mit OIDs verwendet werden.

| Funktion                                                                       | BESCHREIBUNG                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cryptenumuidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Listet die registrierten OID-Funktionen auf, die durch den Codierungstyp, den Funktionsnamen und die OID identifiziert werden.                                                                                                                 |
| [**Cryptenumoidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Listet die registrierten OID-Informationen auf, die von Ihrer Gruppe identifiziert werden, und ruft *pfnenumoidinfo* für Übereinstimmungen auf.                                                                                                       |
| [**Cryptfindoidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Verwendet den angegebenen Schlüssel und die angegebene Gruppe, um OID-Informationen zu suchen.                                                                                                                                                          |
| [**Cryptfreoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Gibt die Anzahl der Handles frei, die von [**cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) oder [**cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)inkrementiert und zurückgegeben wurde. |
| [**Cryptgetdefaultoiddlllist**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Ruft die Liste der registrierten Standard-dll-Einträge für den angegebenen Funktions Satz und den Codierungstyp ab.                                                                                                              |
| [**Cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Ruft entweder die erste oder die nächste installierte Standardfunktion ab oder lädt die dll, die die Standardfunktion enthält.                                                                                                 |
| [**Cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Durchsucht die Liste der installierten Funktionen nach einem Codierungstyp und einer OID-Entsprechung. Wenn keine Entsprechung gefunden wird, wird die Registrierung nach einer Entsprechung durchsucht.                                                                  |
| [**Cryptgetoidfunctionvalue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Ruft den Wert für den angegebenen Codierungstyp, den Funktionsnamen, die OID und den Wert Namen ab.                                                                                                                            |
| [**Cryptinitoidfunctionset**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Initialisiert ein Handle des OID-Funktions Satzes, der durch den angegebenen Funktionsnamen identifiziert wird, und gibt es zurück.                                                                                                                 |
| [**Cryptinstalloidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Installiert eine Reihe von Aufruf baren OID-Funktions Adressen.                                                                                                                                                                 |
| [**Cryptregisterdefaultoidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Registriert die dll, die die Standardfunktion enthält, die für den angegebenen Codierungstyp und Funktionsnamen aufgerufen werden soll.                                                                                               |
| [**Cryptregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Registriert die dll, die die Funktion enthält, die für den angegebenen Codierungstyp, den Funktionsnamen und die OID aufgerufen werden soll.                                                                                                 |
| [**Cryptregisteroidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Registriert die in der [**crypt \_ OID \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) -Struktur angegebenen Oid-Informationen und speichert Sie in der Registrierung.                                                                                |
| [**Cryptstoidfunctionvalue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Legt den Wert für den angegebenen Codierungstyp, den Funktionsnamen, die OID und den Wert Namen fest.                                                                                                                                |
| [**Cryptunregisterdefaultoidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Entfernt die Registrierung für die dll, die die Standardfunktion enthält, die für den angegebenen Codierungstyp und Funktionsnamen aufgerufen werden soll.                                                                            |
| [**Cryptunregisteroidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Entfernt die Registrierung für die dll, die die Funktion enthält, die für den angegebenen Codierungstyp, den Funktionsnamen und die OID aufgerufen werden soll.                                                                              |
| [**Cryptunregisteroidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Entfernt die Registrierung für die angegebenen Oid-Informationen.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Funktionen zum Abrufen von Remote Objekten

Mithilfe der folgenden Funktionen kann der Benutzer ein PKI-Objekt (Public Key-Infrastruktur) abrufen, die URL eines Zertifikats, der CTL oder der CRL abrufen oder eine URL aus einem Objekt extrahieren.

| Funktion                                                     | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Cryptgetobjecturl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Ruft die URL des Remote Objekts von einem Zertifikat, einer CTL oder einer CRL ab. |
| [**CryptRetrieveObjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Ruft das PKI-Objekt von einem Speicherort ab, der durch eine URL angegeben ist.           |



 

### <a name="pfx-functions"></a>PFX-Funktionen

Die folgenden Funktionen unterstützen das PFX [*-Format (*](../secgloss/b-gly.md)Personal Information Exchange).

| Funktion                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pfxexportcertstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | Exporte aus dem Zertifikat, auf das verwiesen wird, [*Speichern*](../secgloss/c-gly.md) die Zertifikate und, falls verfügbar, die zugehörigen [*privaten Schlüssel*](../secgloss/p-gly.md). |
| [**Pfxexportcertstoreex**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | Exporte aus dem Zertifikat, auf das verwiesen wird, speichern die Zertifikate und, falls verfügbar, die zugehörigen privaten Schlüssel.                                                                                                                                                             |
| [**Pfximportcertstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Importiert ein PFX-BLOB und gibt das Handle eines Speichers zurück, der Zertifikate und alle zugeordneten privaten Schlüssel enthält.                                                                                                                                                            |
| [**Pfxispfxblob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Versucht, die äußere Ebene eines BLOB als PFX-Paket zu decodieren.                                                                                                                                                                                                                |
| [**Pfxverifypassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Versucht, die äußere Ebene eines Blobs als PFX-Paket zu decodieren und mit dem angegebenen Kennwort zu entschlüsseln.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Sicherungs-und Wiederherstellungs Funktionen für Zertifikat Dienste

Die Zertifikat Dienste enthalten Funktionen zum Sichern und Wiederherstellen der Zertifikat Dienst-Datenbank. Die Sicherungs-und Wiederherstellungs Funktionen der Zertifikat Dienste sind in Certadm.dll enthalten. Anders als die anderen API-Elemente, die den Zertifikat Diensten zugeordnet sind, sind diese Funktionen nicht in einem Objekt gekapselt, das zum Abrufen von Klassen Methoden verwendet werden kann. Stattdessen werden die Sicherungs-und Wiederherstellungs-APIs aufgerufen, indem zuerst die Certadm.dll Bibliothek in den Arbeitsspeicher geladen wird, indem [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufgerufen und anschließend die Adresse der Funktionen durch Aufrufen von [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)ermittelt wird. Wenn Sie die Funktionen zum Sichern und Wiederherstellen der Zertifikat Dienste aufgerufen haben, rufen Sie [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) auf, um Certadm.dll Ressourcen aus dem Arbeitsspeicher freizugeben.

> [!Note]
> Mithilfe der von Certadm.dll bereitgestellten Sicherungs-und Wiederherstellungs Funktionen werden die [*privaten Schlüssel*](../secgloss/p-gly.md)des Zertifikats Dienstanbieter nicht gesichert oder wieder hergestellt. Informationen zum Sichern der privaten Schlüssel der Zertifikat Dienste finden Sie unter [Sichern und Wiederherstellen des privaten Schlüssels für Zertifikat Dienste](backing-up-and-restoring-the-certificate-services-private-key.md).
> 
> Um die Sicherungs-und Wiederherstellungs Funktionen aufzurufen, müssen Sie über Sicherungs-und Wiederherstellungs [*Berechtigungen*](../secgloss/p-gly.md)verfügen. Weitere Informationen finden Sie unter [Festlegen der Sicherungs-und Wiederherstellungs Berechtigungen](setting-the-backup-and-restore-privileges.md).

 

> [!Note]  
> Wenn **CoInitializeEx** zuvor im gleichen Thread aufgerufen wurde, der zum Aufrufen der Zertifikat Dienst-APIs für die Sicherung und Wiederherstellung verwendet wurde, muss das coinit \_ Apartmentthreaded-Flag an **CoInitializeEx** übermittelt worden sein. Das heißt, wenn Sie denselben Thread verwenden, können Sie die Zertifikat Dienst-API zum Sichern und Wiederherstellen nicht aufrufen, wenn der Thread zuvor das coinit- \_ multithreadflag in einem **CoInitializeEx**-aufrufsvorgang übermittelt hat.

 

Die Sicherungs-APIs für Zertifikat Dienste werden in "certbcli. h" definiert. Wenn Sie das Programm erstellen, verwenden Sie jedoch certrv. h als Includedatei.

Die folgenden APIs werden von Certadm.dll exportiert.

| Funktion                                                                         | BESCHREIBUNG                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**Cerzrvbackupclose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Schließt eine geöffnete Datei.                                                                                                |
| [**Cerzrvbackupend**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Beendet eine Sicherungs Sitzung.                                                                                                |
| [**Cerzrvbackupfree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Gibt einen durch die Backup-und Restore-APIs zugewiesenen Puffer frei.                                                              |
| [**Cergs rvbackupgetbackuplogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Gibt eine Liste der Protokolldateien zurück, die gesichert werden müssen.                                                                |
| [**Cerzrvbackupgetdatabasenames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Gibt eine Liste von Datenbankdateien zurück, die gesichert werden müssen.                                                           |
| [**Cerzrvbackupgetdynamicfilelist**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Ruft die Liste der dynamischen Dateinamen für Zertifikat Dienste ab, die für den angegebenen Sicherungs Kontext gesichert werden müssen. |
| [**Cerzrvbackupopenfile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Öffnet eine Datei zur Vorbereitung der Sicherung.                                                                        |
| [**Cerzrvbackupprepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Bereitet die Datenbank auf die Online Sicherung vor.                                                                          |
| [**Cerzrvbackupread**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Liest den Inhalt einer geöffneten Datei.                                                                                 |
| [**Cerzrvbackuptruneurelogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Verkürzt die Protokolldateien.                                                                                              |
| [**Cerzrvisserveronline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Bestimmt, ob ein Zertifikat Dienste-Server Online ist (aktiv ausgeführt wird).                                        |
| [**Cerzrvrestoreend**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Beendet eine Wiederherstellungs Sitzung.                                                                                               |
| [**Cerzrvrestoregetdatabaselocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Ruft Daten Bank Speicherorte (die für Sicherungs-und Wiederherstellungs Szenarien verwendet werden) ab.                                            |
| [**Cerzrvrestoreprepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Startet eine Wiederherstellungs Sitzung.                                                                                             |
| [**Cerzrvrestoreregiester**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Registriert einen Wiederherstellungs Vorgang.                                                                                        |
| [**Cerzrvrestoreregistercomplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Schließt einen zuvor registrierten Wiederherstellungs Vorgang ab.                                                                  |
| [**Cerzrvrestoreregisterthrough-Datei**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Registriert einen Wiederherstellungs Vorgang.                                                                                        |
| [**Cerzrvservercontrol**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Sendet einen Steuerungs Befehl an die Instanz der Zertifikat Dienste.                                                         |



 

## <a name="callback-functions"></a>Rückruffunktionen

Die Rückruf Funktionen in diesem Abschnitt werden verwendet, um Anwendungs definierte [*Zertifikat Speicher*](../secgloss/c-gly.md) Anbieter zu registrieren oder zu installieren und um zugehörige Funktionen mithilfe von Rückruf Funktionen bereitzustellen. Rückruf Funktionen werden von einer Anwendung implementiert und von [*CryptoAPI*](../secgloss/c-gly.md) -Funktionen aufgerufen. Mit Rückruf Funktionen kann die Anwendung teilweise die Art und Weise steuern, wie kryptoapi-Funktionen Daten bearbeiten.

| Rückruffunktion                                                                                                        | Zweck                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certchainfindbyissuercallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Eine Anwendungs definierte Rückruffunktion, mit der die Anwendung Zertifikate filtern kann, die der Zertifikatskette hinzugefügt werden können.                                                                                                                                                                                                     |
| [**Certdllopenstoreprov**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Definiert die Open-Funktion für den Store-Anbieter.                                                                                                                                                                                                                                                                                                     |
| [**Certenumschlag physicalstorecallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Rückruffunktion, die von der [**certenumschlag physicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) -Funktion verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und darzustellen.                                                                                                                                                                                 |
| [**Certenresystemstorecallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Rückruffunktion, die von der [**certenumschlag System Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) -Funktion verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und darzustellen.                                                                                                                                                                                     |
| [**Certenumschlag systemstorelocationcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Rückruffunktion, die von der [**certenresystemstoreloation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) -Funktion verwendet wird, um Informationen zu jedem gefundenen physischen Speicher zu formatieren und darzustellen.                                                                                                                                                                     |
| [**Certstoreprovclosecallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Bestimmt, was passiert, wenn der [*Verweis Zähler*](../secgloss/r-gly.md) eines geöffneten Stores NULL wird.                                                                                                                                                                                    |
| [**Certstoreprovcontrol**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Ermöglicht es, eine Anwendung zu benachrichtigen, wenn es einen Unterschied zwischen dem Inhalt eines zwischengespeicherten Speichers und dem Inhalt dieses Speichers gibt, der im Speicher gespeichert ist.                                                                                                                                                                   |
| [**Certstoreprovdeletecertcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Bestimmt, welche Aktionen ausgeführt werden müssen, bevor ein Zertifikat aus einem Zertifikat Speicher gelöscht wird.                                                                                                                                                                                                                                                      |
| [**Certstoreprovdeletecrlcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Bestimmt, welche Aktionen ausgeführt werden müssen, bevor eine [*Zertifikat Sperr Liste*](../secgloss/c-gly.md) aus einem Zertifikat Speicher gelöscht wird.                                                                                                                        |
| [**Certstoreprovdeletectl**](certstoreprovdeletectl.md)                                                                 | Bestimmt, ob eine CTL gelöscht werden kann.                                                                                                                                                                                                                                                                                                      |
| [**Certstoreprovfindcert**](certstoreprovfindcert.md)                                                                   | Sucht das erste oder nächste Zertifikat in einem Speicher, das mit den angegebenen Kriterien übereinstimmt.                                                                                                                                                                                                                                                             |
| [**Certstoreprovfindcrl**](certstoreprovfindcrl.md)                                                                     | Sucht den ersten oder nächsten CRL-Wert in einem Speicher, der mit den angegebenen Kriterien übereinstimmt.                                                                                                                                                                                                                                                                     |
| [**Certstoreprovfindctl**](certstoreprovfindctl.md)                                                                     | Sucht die erste oder nächste CTL in einem Speicher, der den angegebenen Kriterien entspricht.                                                                                                                                                                                                                                                                     |
| [**Certstoreprovfreifindcert**](certstoreprovfreefindcert.md)                                                           | Gibt einen zuvor gefundenen Zertifikat kontextfrei.                                                                                                                                                                                                                                                                                                 |
| [**Certstoreprovfreifindcrl**](certstoreprovfreefindcrl.md)                                                             | Gibt einen zuvor gefundenen CRL-kontextfrei.                                                                                                                                                                                                                                                                                                         |
| [**Certstoreprovfreifindctl**](certstoreprovfreefindctl.md)                                                             | Gibt einen zuvor gefundenen CTL-kontextfrei.                                                                                                                                                                                                                                                                                                         |
| [**Certstoreprovgetcertproperty**](certstoreprovgetcertproperty.md)                                                     | Ruft eine angegebene Eigenschaft eines Zertifikats ab.                                                                                                                                                                                                                                                                                              |
| [**Certstoreprovgetcrlproperty**](certstoreprovgetcrlproperty.md)                                                       | Ruft eine angegebene Eigenschaft einer CRL ab.                                                                                                                                                                                                                                                                                                      |
| [**Certstoreprovgetctl-Eigenschaft**](certstoreprovgetctlproperty.md)                                                       | Ruft eine angegebene Eigenschaft einer CTL ab.                                                                                                                                                                                                                                                                                                      |
| [**Certstoreprovlescertcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Wird derzeit nicht verwendet, kann aber in zukünftige CSPs exportiert werden.                                                                                                                                                                                                                                                                                      |
| [**Certstoreprovlescrlcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Wird derzeit nicht verwendet, kann aber in zukünftige CSPs exportiert werden.                                                                                                                                                                                                                                                                                      |
| [**Certstoreprovumctl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Lesen Sie die Kopie des CTL-Kontexts des Anbieters, und erstellen Sie, sofern vorhanden, einen neuen CTL-Kontext.                                                                                                                                                                                                                                                     |
| [**Certstoreprovsetcertpropertycallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Bestimmt Aktionen, die vor dem Aufrufen von " [**certsetcertifiaseecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) " oder " [**certgetcertifiaseecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)" durchgeführt werden.                                                                                                                             |
| [**Certstoreprovsetcrlpropertycallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Bestimmt Aktionen, die vor dem Aufrufen von " [**certsetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) " oder " [**certgetcrlcontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)" durchgeführt werden.                                                                                                                                                             |
| [**Certstoreprovsetctlproperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Bestimmt, ob eine Eigenschaft für eine CTL festgelegt werden kann.                                                                                                                                                                                                                                                                                            |
| [**Certstoreprovschreitecertcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Bestimmt, welche Aktionen ausgeführt werden müssen, bevor einem Speicher ein Zertifikat hinzugefügt wird.                                                                                                                                                                                                                                                                        |
| [**Certstoreprovschreitecrlcallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Bestimmt, welche Aktionen ausgeführt werden müssen, bevor einem Speicher eine Zertifikat Sperr Liste hinzugefügt wird.                                                                                                                                                                                                                                                                                |
| [**Certstoreprovschreitectl**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Bestimmt, ob eine CTL zum Speicher hinzugefügt werden kann.                                                                                                                                                                                                                                                                                           |
| [**Crypt-Aufzählung \_ \_ keyid- \_ Prop**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Rückruffunktion, die von der [**cryptenrekeyidentifierproperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties) -Funktion verwendet wird.                                                                                                                                                                                                                          |
| [**Crypt- \_ Enum- \_ OID- \_ Funktion**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Rückruffunktion, die von der [**cryptenumuidfunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction) -Funktion verwendet wird.                                                                                                                                                                                                                                                  |
| [**Crypt-ergebenden \_ \_ OID- \_ Informationen**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Rückruffunktion, die von der [**cryptenumoidinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo) -Funktion verwendet wird.                                                                                                                                                                                                                                                          |
| [**Cryptgetsignercertifialisiecallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Rückruffunktion, die mit der [**crypt \_ Verify \_ Message \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) -Struktur verwendet wird, um das Zertifikat eines Nachrichten Signatur Gebers zu erhalten und zu überprüfen.                                                                                                                                                                                 |
| [**pcrypt \_ Entschlüsseln des \_ privaten \_ Schlüssels \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Rückruffunktion, die von der [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) -Funktion verwendet wird.                                                                                                                                                                                                                                                          |
| [**pcrypt- \_ Funktion zum Verschlüsseln des \_ privaten \_ Schlüssels \_**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Rückruffunktion, die beim Erstellen der Informationsstruktur mit [**\_ verschlüsseltem \_ privaten \_ Schlüssel \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) verwendet wird.                                                                                                                                                                                                          |
| [**pcrypt \_ Auflösen von \_ hcryptprov \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Rückruffunktion, die von der [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) -Funktion verwendet wird.                                                                                                                                                                                                                                                          |
| [**PFN \_ CDF-Analyse \_ \_ Fehler \_ Rückruf**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Eine benutzerdefinierte Funktion, die für Fehler bei der Katalog Definitions Funktion aufgerufen wird, während eine Katalog Definitionsdatei (CDF) verarbeitet wird.                                                                                                                                                                                                                          |
| [**PFN \_ CERT \_ Create \_ context \_ Sort \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Wird für jeden sortierten Kontext Eintrag aufgerufen, wenn ein Kontext erstellt wird.                                                                                                                                                                                                                                                                               |
| [**PFN \_ CMSG \_ CNG \_ Import \_ Content \_ Verschlüsselungs \_ Schlüssel**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Eine in der CNG- [*Objekt Kennung*](../secgloss/o-gly.md) (OID) installierbare Funktion für den Import eines bereits entschlüsselten Content Encryption Key (CEK).                                                                                                                                       |
| [**Schlüssel für PFN \_ CMSG \_ CNG- \_ Import \_ Schlüssel \_ zustimmen**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Importiert einen Inhalts Verschlüsselungsschlüssel für einen Schlüssel Transport Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG \_ Import \_ Schlüssel \_ Trans**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Eine CNG-OID-installierbare Funktion zum Importieren und [*entschlüsseln*](../secgloss/d-gly.md) eines Schlüssels (Key-Transport-Recipient, verschlüsselt, Content [*Encryption*](../secgloss/e-gly.md) Key, CEK).                                                                   |
| [**PFN \_ CMSG- \_ Export \_ Schlüssel \_ zustimmen**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Verschlüsselt und exportiert den Inhalts Verschlüsselungsschlüssel für einen Schlüssel Übereinstimmungs Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG- \_ Export \_ Schlüssel \_ Trans**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Verschlüsselt und exportiert den Inhalts Verschlüsselungsschlüssel für einen Schlüssel Transport Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG-Export-e- \_ Mail- \_ \_ Liste**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Verschlüsselt und exportiert den Inhalts Verschlüsselungsschlüssel für einen Mailinglisten Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                         |
| [**Schlüssel zum Verschlüsseln von PFN- \_ CMSG- \_ \_ Inhalten \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Generiert den [*symmetrischen Schlüssel*](../secgloss/s-gly.md) , der zum Verschlüsseln des Inhalts für eine eingehüllte Nachricht verwendet wird.                                                                                                                                                                                     |
| [**PFN \_ CMSG- \_ Import \_ Schlüssel \_ zustimmen**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Importiert einen Inhalts Verschlüsselungsschlüssel für einen Schlüssel Transport Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG- \_ Import \_ Schlüssel \_ Trans**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Importiert einen Inhalts Verschlüsselungsschlüssel für einen Schlüssel Transport Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG-e- \_ Mail- \_ \_ Liste importieren**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Importiert einen Inhalts Verschlüsselungsschlüssel für einen Schlüssel Transport Empfänger einer eingeschlossenen Nachricht.                                                                                                                                                                                                                                                       |
| [**PFN \_ crypt \_ , \_ Informationen zum öffentlichen \_ Schlüssel exportieren \_ \_ ex2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Wird von [**cryptexportpublickeyinfoex**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) aufgerufen, um ein öffentliches Schlüsselblob zu exportieren und zu codieren.                                                                                                                                                                                                                         |
| [**PFN \_ crypt \_ extrahieren \_ codierter \_ Signatur \_ Parameter \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Wird zum Decodieren und Zurückgeben des Hash Algorithmus Bezeichners und optional der Signatur Parameter aufgerufen.                                                                                                                                                                                                                                            |
| [**PFN \_ \_ -crypt-Signatur signieren \_ und \_ \_ Hashwert codieren \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Wird aufgerufen, um einen berechneten Hash zu signieren und zu codieren.                                                                                                                                                                                                                                                                                                    |
| [**PFN- \_ crypt, \_ \_ codierte \_ Signatur überprüfen \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Wird aufgerufen, um eine codierte Signatur zu entschlüsseln und mit einem berechneten Hash zu vergleichen.                                                                                                                                                                                                                                                                     |
| [**PFN \_ Importieren von \_ Informationen zum öffentlichen \_ Schlüssel \_ \_ ex2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Wird von [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) aufgerufen, um den [*Algorithmus für den Algorithmus des öffentlichen Schlüssels*](../secgloss/p-gly.md) zu decodieren, den Algorithmusanbieter zu laden und das [*Schlüsselpaar*](../secgloss/k-gly.md)zu importieren. |
| [**Pfnccertdisplayproc**](pfnccertdisplayproc.md)                                                                       | Eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der Funktion [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zum anzeigen auswählt.                                                                                                                               |
| [**Pfncmfilterproc**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Filtert jedes Zertifikat, um zu entscheiden, ob es im Dialogfeld Zertifikat Auswahl angezeigt wird, das von der [**certselectcertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) -Funktion angezeigt wird.                                                                                                                                                                |
| [**Pfncmhuokproc**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Wird aufgerufen, bevor Meldungen durch das von der [**certselectcertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) -Funktion erstellte Dialogfeld zur Zertifikat Auswahl verarbeitet werden.                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Katalog Definitions Funktionen

Diese Funktionen werden verwendet, um einen Katalog zu erstellen. Alle diese Funktionen werden von [MakeCat](makecat.md)aufgerufen.

| Funktion                                                                           | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Cryptcdfclose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Schließt eine Katalog Definitionsdatei und gibt den Arbeitsspeicher für die entsprechende [**cryptasecdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur frei. |
| [**Cryptovcdfenumschlag attributeswithcdftag**](cryptcatcdfenumattributeswithcdftag.md) | Listet die Attribute der Element Dateien im **catalogfiles** -Abschnitt einer CDF auf.                                       |
| [**Cryptccdfenumschlag-Attribute**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Listet Attribute auf Katalog Ebene innerhalb des **catalogheader** -Abschnitts einer CDF auf.                                        |
| [**Cryptccdfenumschlag mitgliedsbycdftagex**](cryptcatcdfenummembersbycdftagex.md)       | Listet die einzelnen dateimember im **catalogfiles** -Abschnitt einer CDF auf.                                          |
| [**Cryptcdfopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Öffnet eine vorhandene CDF zum Lesen und Initialisieren einer [**cryptingcdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur.                         |



 

## <a name="catalog-functions"></a>Katalogfunktionen

Diese Funktionen werden verwendet, um einen-Katalog zu verwalten.

| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cryptingadminacquirecontext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Ruft ein Handle für einen Katalog Administrator Kontext ab. Dieses Handle kann von nachfolgenden Aufrufen der Funktionen [**cryptgatadminaddcatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog), [**cryptgatadminenumcatalogfromhash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)und [**cryptgatadminremovecatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) verwendet werden. |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Ruft ein Handle für einen Katalog Administrator Kontext für einen angegebenen Hash Algorithmus und eine angegebene Hash Richtlinie ab.                                                                                                                                                                                                                                   |
| [**Cryptder adminaddcatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Fügt der Katalog Datenbank einen Katalog hinzu.                                                                                                                                                                                                                                                                                            |
| [**Cryptder admincalchashfromfilehandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Berechnet den Hash für eine Datei.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Berechnet den Hash für eine Datei unter Verwendung des angegebenen Algorithmus.                                                                                                                                                                                                                                                                   |
| [**Cryptgatadminenumcatalogfromhash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Listet die Kataloge auf, die einen angegebenen Hash enthalten.                                                                                                                                                                                                                                                                             |
| [**Cryptassadminreleasecatalogcontext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Gibt ein Handle für einen Katalog kontextfrei, der zuvor von der [**cryptaseadminaddcatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) -Funktion zurückgegeben wurde.                                                                                                                                                                                             |
| [**Cryptassadminreleasecontext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Gibt das Handle frei, das zuvor von der [**cryptaseadminacquirecontext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) -Funktion zugewiesen wurde.                                                                                                                                                                                                        |
| [**Cryptder adminremovecatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | Löscht eine Katalog Datei und entfernt den Eintrag dieses Katalogs aus der Windows-Katalog Datenbank.                                                                                                                                                                                                                                         |
| [**Cryptingadminresolvecatalogpath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Ruft den voll qualifizierten Pfad des angegebenen Katalogs ab.                                                                                                                                                                                                                                                                       |
| [**Cryptingcataloginfofromcontext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Ruft Katalog Informationen aus einem angegebenen Katalog Kontext ab.                                                                                                                                                                                                                                                                    |
| [**Crypt-close**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Schließt ein Katalog handle, das zuvor von der [**cryptkataopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) -Funktion geöffnet wurde.                                                                                                                                                                                                                                    |
| [**Crypt-enumerateattr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Listet die Attribute auf, die einem Member eines Katalogs zugeordnet sind.                                                                                                                                                                                                                                                                   |
| [**Crypt-enumeratecatattr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Listet die einem Katalog zugeordneten Attribute auf.                                                                                                                                                                                                                                                                               |
| [**Cryptkataenumeratemember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Listet die Member eines Katalogs auf.                                                                                                                                                                                                                                                                                               |
| [**Cryptplatgetattrinfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Ruft Informationen zu einem Attribut eines Katalogs eines Katalogs ab.                                                                                                                                                                                                                                                                 |
| [**Cryptplatgetmembership Info**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Ruft Element Informationen aus den PKCS 7 des Katalogs ab \# . Zusätzlich zum Abrufen der Element Informationen für ein angegebenes Verweistag öffnet diese Funktion einen Element Kontext.                                                                                                                                                    |
| [**Crypt. Open**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Öffnet einen Katalog und gibt ein Kontext Handle für den geöffneten Katalog zurück.                                                                                                                                                                                                                                                                 |
| [**Iscatalogfile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Ruft einen booleschen Wert ab, der angibt, ob es sich bei der angegebenen Datei um eine Katalog Datei handelt.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>Wintrust-Funktionen

Die folgenden Funktionen werden verwendet, um verschiedene Vertrauens Vorgänge auszuführen.

| Funktion                                                                               | BESCHREIBUNG                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wintrustaddactionid**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Fügt dem System des Benutzers eine Aktion zum vertrauenswürdigen Anbieter hinzu.                                                                                                                   |
| [**Wintrustgetregpolicyflags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Ruft Richtlinienflags für einen Richtlinien Anbieter ab.                                                                                                                        |
| [**Wintrustadddefaultforusage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Gibt den standardmäßigen Verwendungs Bezeichner und Rückruf Informationen für einen Anbieter an.                                                                                       |
| [**Wintrustgetdefaultforusage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Ruft den standardmäßigen Verwendungs Bezeichner und die Rückruf Informationen ab.                                                                                                     |
| [**Wintrustloadfunctionpointer**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Lädt Funktions Einstiegspunkte für eine angegebene Aktions-GUID.                                                                                                             |
| [**Wintrustremuveaktionkennung**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Entfernt eine Aktion, die von der [**wintrustaddactionid**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) -Funktion hinzugefügt wurde.                                                                          |
| [**Wintrustsetdefaultincludepeer-Werte**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Legt die Standardeinstellung fest, die bestimmt, ob Seitenhashes beim Erstellen der indirekten SIP-Daten (Subject Interface Package) für portable ausführbare Dateien enthalten sind. |
| [**Wintrust-tregpolicyflags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Legt Richtlinienflags für einen Richtlinien Anbieter fest.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Führt eine Überprüfung der Vertrauenswürdigkeit für ein angegebenes Objekt aus.                                                                                                          |
| [**Winverifytrustex**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Führt eine Überprüfung der Vertrauenswürdigkeit für ein angegebenes Objekt aus und übernimmt einen Zeiger auf eine wintrust- \_ Datenstruktur.                                                        |
| [**Wthelpercertcheckvalidsignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Überprüft, ob eine Signatur gültig ist.                                                                                                                                 |
| [**Wthelpercertfinrevoercertificate**](wthelpercertfindissuercertificate.md)         | Sucht ein Aussteller Zertifikat aus den angegebenen Zertifikat speichern, das mit dem angegebenen Antragsteller Zertifikat übereinstimmt.                                                    |
| [**Wthelpercertisselfsigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Überprüft, ob ein Zertifikat selbst signiert ist.                                                                                                                         |
| [**Wthelpergetflehash**](wthelpergetfilehash.md)                                     | Überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.                                                            |
| [**Wthelpergetprovcertfromchain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Ruft ein Vertrauens Anbieter Zertifikat von der Zertifikat Kette ab.                                                                                                   |
| [**Wthelpergetprovprivatedatafromchain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Empfängt mithilfe der Anbieter-ID eine [**\_ \_ privdata**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) -Struktur des Crypt-Anbieters von der Kette.                                           |
| [**Wthelpergetprovsignerfromchain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Ruft einen Signatur Geber oder gegen Signatur Geber anhand des Indexes aus der Kette ab.                                                                                                         |
| [**Wthelperprovdatafromstatedata**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Ruft Informationen zu Vertrauens Anbietern von einem angegebenen Handle ab.                                                                                                        |



 

## <a name="object-locator-functions"></a>Objektlocator-Funktionen

Die folgenden Rückruf Funktionen können von einem benutzerdefinierten Anbieter implementiert werden, der vom Sicherheitspaket Secure Channel (SChannel) zum Abrufen von Zertifikaten aufgerufen werden soll.



| Funktion                                                                                                             | BESCHREIBUNG                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**PFN- \_ crypt- \_ \_ objektlocatoranbieter leeren \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Gibt an, dass sich ein Objekt geändert hat.                   |
| [**PFN- \_ crypt- \_ \_ objektlocator- \_ Anbieter \_ Get**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Ruft ein-Objekt ab.                                    |
| [**PFN- \_ crypt- \_ \_ objektlocator- \_ Anbieter \_ Release**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Gibt den Anbieter frei.                                  |
| [**\_ \_ \_ \_ \_ Kostenloses \_ Kennwort für PFN-Crypt-objektlocator**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Gibt das zum Verschlüsseln eines PFX-Bytearrays verwendete Kennwort frei. |
| [**PFN- \_ crypt- \_ \_ objektlocatoranbieter \_ \_ kostenlos**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Gibt das vom Anbieter zurückgegebene Objekt frei.           |
| [**\_ \_ \_ \_ \_ kostenloser \_ Bezeichner für PFN-Crypt-objektlocator**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Gibt Arbeitsspeicher für einen Objekt Bezeichner frei.               |
| [**PFN- \_ crypt- \_ \_ objektlocatoranbieter \_ \_ initialisieren**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Initialisiert den Anbieter.                               |



 

 

 

---
description: Cryptxml ermöglicht Entwicklern das Erweitern von nativ unterstützten Kryptografiealgorithmen durch Registrieren einer systemweiten kryptografieerweiterungs-dll.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Kryptografieerweiterungen für die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869328"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Kryptografieerweiterungen für die digitale XML-Signatur

Cryptxml ermöglicht Entwicklern das Erweitern von nativ unterstützten Kryptografiealgorithmen durch Registrieren einer systemweiten kryptografieerweiterungs-dll. Erweiterungs-DLLs erweitern die Algorithmen, die von den XML-Elementen **SignatureMethod** und **DigestMethod** unterstützt werden. Erweiterungs-DLLs können Algorithmen unterstützen, die zusätzliche Parameter in die digitale XML-Signatur codieren.

Alle Erweiterungs-DLLs müssen die [**cryptxmldllgetinterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) -Funktion unterstützen, die einen Zeiger auf eine [**\_ \_ kryptografische \_ kryptografieschnittstellenstruktur von Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) zurückgibt. Diese Struktur stellt Funktionszeiger auf implementierte kryptografieerweiterungsfunktionen bereit. Welche Funktionen unterstützt werden, hängt vom Typ des unterstützten Kryptografiealgorithmus ab und davon, ob der Algorithmus Parameter in die digitale XML-Signatur codieren muss.

Funktionen für kryptografische Erweiterungen enthalten die folgenden Funktionszeiger:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Erforderliche Funktionen
</dt> <dd>

-   [**Cryptxmldllgetinterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**Cryptxmldllgetalgorithminfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest-Methoden Funktionen
</dt> <dd>

-   [**Cryptxmldllclosedigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**Cryptxmldllkreatediering**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**Cryptxmldlldigestdata**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**Cryptxmldllfinalizedigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funktionen der Signatur Methode
</dt> <dd>

-   [**Cryptxmldllsigndata**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**Cryptxmldllverifysignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**Cryptxmldllkreatekey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**Cryptxmldllencodkeyvalue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Für Algorithmen mit standardmäßigen codierten Parametern
</dt> <dd>

-   [**Cryptxmldllencodealgorithmus**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Kryptografieerweiterungs-DLLs werden auf systemweite Basis registriert. Administrator Rechte sind erforderlich, um eine kryptografieerweiterungs-dll zu registrieren.

Alle Kryptografieerweiterungen von cryptxml werden durch den URI-Wert registriert, der im **SignatureMethod** -oder algorithmusattributfeld des **DigestMethod** -Elements festgelegt ist.

Die Registrierungs Pfade für die Erweiterungs-DLLs lauten wie folgt:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32-Bit
</dt> <dd>

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64-Bit
</dt> <dd>

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*

</dd> </dl>

Jeder Schlüssel enthält die folgenden Einstellungen.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Daten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DLL<br/></td>
<td>Erweiterbare Zeichenfolge<br/></td>
<td>Erforderlich.<br/>Der absolute Pfad zur XML-Kryptografieanbieter-dll.
<blockquote>
<p><b>Hinweis: </b> Es wird empfohlen, dass sich kryptografieerweiterungs-DLLs in Verzeichnissen befinden, die nur von Anwendungen mit Administratorrechten geschrieben werden können.</p>
<p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> wird verwendet, um die dll der kryptografieerweiterung zu laden.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Name<br/></td>
<td><strong>String</strong></td>
<td>Dies ist optional.<br/> Der diesem URI zugeordnete Anzeige Name.<br/></td>
</tr>
<tr class="odd">
<td>GroupId<br/></td>
<td><strong>DWORD</strong></td>
<td>Erforderlich.<br/> Der diesem Kryptografiealgorithmus zugeordnete Gruppen Bezeichner. Folgende Werte sind möglich:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1<br/><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2<br/></td>
</tr>
<tr class="even">
<td>Cngalgid<br/></td>
<td><strong>String</strong></td>
<td>Erforderlich.<br/> Der Name des CNG-Algorithmus, der an die Funktionen bcrypt oder NCrypt übermittelt werden soll.<br/></td>
</tr>
<tr class="odd">
<td>Cngextraalgid<br/></td>
<td><strong>String</strong></td>
<td>Dies ist optional.<br/> Eine zusätzliche algorithmuszeichenfolge, die nicht die Zeichenfolge im cngalgid-Member ist, die an die CNG-Funktionen übergeben werden kann.<br/> Bei den Signatur Algorithmen (CRYPT_XML_GROUP_ID_SIGN) ist dieser Member die Algorithmus-Zeichenfolge für den öffentlichen Schlüssel, die an die CNG-Funktionen übergeben werden soll.<br/> Legen Sie für die anderen Werte von GroupID den <strong>pwszcngextraalgid</strong> -Member auf die leere Zeichenfolge L fest &quot; &quot; . <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[Kryptografiealgorithmen für die digitale XML-Signatur](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 

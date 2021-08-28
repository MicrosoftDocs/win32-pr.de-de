---
description: Mit CryptXML können Entwickler nativ unterstützte kryptografische Algorithmen erweitern, indem sie eine systemweite kryptografische Erweiterungs-DLL registrieren.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Kryptografische XML-Signaturerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf0f2d99b34d59e9817f8568b03be20e72dda1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474936"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Kryptografische XML-Signaturerweiterungen

Mit CryptXML können Entwickler nativ unterstützte kryptografische Algorithmen erweitern, indem sie eine systemweite kryptografische Erweiterungs-DLL registrieren. Erweiterungs-DLLs erweitern die algorithmen, die von **SignatureMethod-** und **DigestMethod-XML-Elementen** unterstützt werden. Erweiterungs-DLLs können Algorithmen unterstützen, die zusätzliche Parameter in die digitale XML-Signatur codieren.

Alle Erweiterungs-DLLs müssen die [**CryptXmlDllGetInterface-Funktion**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) unterstützen, die einen Zeiger auf eine [**CRYPT \_ XML CRYPTOGRAPHIC \_ \_ INTERFACE-Struktur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) zurückgibt. Diese Struktur stellt Funktionsze zeiger auf implementierte kryptografische Erweiterungsfunktionen zur Verfügung. Die unterstützten Funktionen hängen vom Typ des unterstützten kryptografischen Algorithmus ab und davon, ob der Algorithmus Parameter in die digitale XML-Signatur codieren muss.

Kryptografische Erweiterungsfunktionen enthalten die folgenden Funktionsze zeiger:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Erforderliche Funktionen
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest-Methodenfunktionen
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature-Methodenfunktionen
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Für Algorithmen mit codierten Standardparametern
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Kryptografische Erweiterungs-DLLs werden systemweit registriert. Administratorrechte sind erforderlich, um eine kryptografische Erweiterungs-DLL zu registrieren.

Alle kryptografischen CryptXML-Erweiterungen werden durch den URI-Wert registriert, der im **SignatureMethod-Feld** oder im Algorithmusattributfeld des **DigestMethod-Elements festgelegt** ist.

Die Registrierungspfade für die Erweiterungs-DLLs lauten wie folgt:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32-Bit
</dt> <dd>

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64-Bit
</dt> <dd>

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> </dl>

Jeder Schlüssel enthält die folgenden Einstellungen.




| Name | Typ | Daten | 
|------|------|------|
| DLL<br /> | Erweiterbare Zeichenfolge<br /> | Erforderlich.<br />Der absolute Pfad zur XML-Kryptografieanbieter-DLL.<blockquote><p><b>Hinweis: </b> Es wird empfohlen, sich kryptografische Erweiterungs-DLLs in Verzeichnissen zu befinden, in die nur Anwendungen mit Administratorrechten geschrieben werden können.</p><p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary wird</strong></a> verwendet, um die kryptografische Erweiterungs-DLL zu laden.<br /></p></blockquote><br /> | 
| Name<br /> | <strong>String</strong> | Optional.<br /> Der diesem URI zugeordnete Anzeigename.<br /> | 
| GroupId<br /> | <strong>DWORD</strong> | Erforderlich.<br /> Der diesem kryptografischen Algorithmus zugeordnete Gruppenbezeichner. Mögliche Werte sind:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \<strong> </strong> = 1<br /><strong></strong> \<strong> CRYPT_XML_GROUP_ID_SIGN </strong> = 2<br /> | 
| CNGAlgid<br /> | <strong>String</strong> | Erforderlich.<br /> Der CNG-Algorithmusname, der an BCrypt- oder NCrypt-Funktionen übergeben werden soll.<br /> | 
| CNGExtraAlgid<br /> | <strong>String</strong> | Optional.<br /> Eine zusätzliche Algorithmuszeichenfolge außer der Zeichenfolge im CNGAlgid-Member, die an die CNG-Funktionen übergeben werden kann.<br /> Für die Signaturalgorithmen (CRYPT_XML_GROUP_ID_SIGN) ist dieser Member die Algorithmuszeichenfolge für öffentliche Schlüssel, die an die CNG-Funktionen übergeben werden soll.<br /> Legen Sie für die anderen Werte von GroupId das <strong>pwszCNGExtraAlgid-Member</strong> auf die leere Zeichenfolge L" fest. <br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[Kryptografische Algorithmen für digitale XML-Signaturen](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 

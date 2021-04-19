---
description: Definiert Fehlercodes, die von CAPICOM zurückgegeben werden.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361970"
---
# <a name="capicom_error_code-enumeration"></a>CAPICOM- \_ Fehler \_ Code-Enumeration

Der-Enumerationstyp " **CAPICOM- \_ Fehler \_ Code** " definiert Fehlercodes, die von CAPICOM zurückgegeben werden.

> [!Note]  
> Visual Basic Scripting Edition Fehler geben einen **Err. Number** -Wert größer als 0 (null) zurück. Für diese Fehler enthalten **Err. Description** -Werte Informationen zur Ursache des Fehlers. Zusätzlich zu Visual Basic Scripting Edition Fehlern geben CAPICOM-Fehler die vom **CAPICOM- \_ Fehler \_ Code** definierten Codes zurück.

 

## <a name="members"></a>Member



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Member</th>
<th>BESCHREIBUNG</th>
<th>Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></td>
<td>Es wurde ein ungültiger Codierungstyp verwendet.<br/> In der folgenden Liste werden die gültigen Codierungs Typen angezeigt:
<ul>
<li>CAPICOM_ENCODE_ANY</li>
<li>CAPICOM_ENCODE_BASE64</li>
<li>CAPICOM_ENCODE_BINARY</li>
</ul>
<br/></td>
<td>0x80880100</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EKU_INVALID_OID</strong></td>
<td>Die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft des <a href="eku.md"><strong>EKU</strong></a> -Objekts kann nicht festgelegt werden, da die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft nicht auf CAPICOM_EKU_OTHER festgelegt ist.<br/> Legen Sie die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft auf CAPICOM_EKU_OTHER fest, bevor Sie die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft festlegen.<br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td>Die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft des <a href="eku.md"><strong>EKU</strong></a> -Objekts wurde nicht initialisiert. <br/> Legen Sie die <a href="eku-name.md"><strong>Name</strong></a> -Eigenschaft entweder auf einen anderen Wert als CAPICOM_EKU_OTHER fest, oder legen Sie die <strong>Name</strong> -Eigenschaft auf CAPICOM_EKU_OTHER und die <a href="eku-oid.md"><strong>OID</strong></a> -Eigenschaft auf einen Wert fest.<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td>Das <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt wurde nicht initialisiert.<br/> Normalerweise wird dieser Fehlercode zurückgegeben, wenn ein <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt instanziiert, aber keinem digitalen Zertifikat zugeordnet wird. Um das Objekt einem digitalen Zertifikat zuzuordnen, weisen Sie es entweder einem vorhandenen <strong>Zertifikat</strong> Objekt zu, oder wenden Sie die <a href="certificate-import.md"><strong>Import</strong></a> Methode an.<br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></td>
<td>Dem <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt ist kein privater Schlüssel zugeordnet.<br/> Dieser Fehlercode wird zurückgegeben, wenn versucht wird, Daten mit dem privaten Schlüssel des Signatur Gebers zu signieren, aber das <a href="certificate.md"><strong>Zertifikat</strong></a> Objekt, das dem <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt zugeordnet ist, kann nicht für den Signier Vorgang verwendet werden.<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td>Das <a href="chain.md"><strong>Ketten</strong></a> Objekt wurde nicht initialisiert. <br/> Um das <a href="chain.md"><strong>Ketten</strong></a> Objekt zu initialisieren, müssen Sie die Buildmethode aufzurufen. <a href="chain-build.md"><strong></strong></a><br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td>Das <a href="store.md"><strong>Speicher</strong></a> Objekt wurde nicht initialisiert. <br/> Um das <a href="store.md"><strong>Speicher</strong></a> Objekt zu initialisieren, nennen Sie die <a href="store-open.md"><strong>Open</strong></a> -Methode.<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td>Das <a href="store.md"><strong>Store</strong></a> -Objekt enthält keine <a href="certificate.md"><strong>Zertifikat</strong></a> Objekte.<br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td>Der <em>OpenMode</em> -Parameter der <a href="store-open.md"><strong>Store. Open</strong></a> -Methode enthält keinen gültigen Wert CAPICOM_STORE_OPEN_MODE.<br/> In der folgenden Liste werden die gültigen Werte CAPICOM_STORE_OPEN_MODE angezeigt:
<ul>
<li>CAPICOM_STORE_OPEN_READ_ONLY</li>
<li>CAPICOM_STORE_OPEN_READ_WRITE</li>
<li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li>
<li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li>
<li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li>
</ul>
<br/></td>
<td>0x80880232</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></td>
<td>Der an die <a href="store-export.md"><strong>Export</strong></a> -Methode des <a href="store.md"><strong>Speicher</strong></a> Objekts über gegebene <em>SaveAs</em> -Wert war ungültig. <br/> In der folgenden Liste werden die gültigen <em>SaveAs</em> -Werte angezeigt:
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>Die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts wurde nicht initialisiert. <br/> Legen Sie die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft fest.<br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>Die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts wurde nicht initialisiert. <br/> Legen Sie die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft fest.<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td>Die <a href="attribute-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts ist ungültig. <br/> In der folgenden Liste werden die gültigen Attributnamen angezeigt:
<ul>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li>
</ul>
<br/></td>
<td>0x80880242</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></td>
<td>Die <a href="attribute-value.md"><strong>value</strong></a> -Eigenschaft des <a href="attribute.md"><strong>Attribut</strong></a> Objekts ist ungültig, da der Datentyp nicht mit dem Datentyp identisch ist, der durch die <strong>Name</strong> -Eigenschaft angegeben wird. <br/> Wenn die <a href="attribute-value.md"><strong>Name</strong></a> -Eigenschaft beispielsweise auf CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME festgelegt ist, muss der Datentyp " <strong>Date</strong>" lauten.<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td>Das <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt wurde nicht initialisiert. <br/> Um das <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt zu initialisieren, legen Sie die Eigenschaft <a href="signer-certificate.md"><strong>Zertifikat</strong></a> fest.<br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>Der Signatur Geber wurde im <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt nicht gefunden. <br/> Dies geschieht in der Regel nicht mit einem <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt, das von CAPICOM erstellt wurde. Wenn das <strong>SignedData</strong> -Objekt jedoch von einem Drittanbieter Produkt erstellt wurde, ist das Zertifikat des Signatur Gebers möglicherweise nicht in der PKCS-#7 Struktur enthalten.<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>Ein <a href="chain.md"><strong>Ketten</strong></a> Objekt wurde im <a href="signer.md"><strong>Signatur</strong></a> Geber Objekt nicht gefunden.<br/></td>
<td>0x80880252//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>Es wurde versucht, den Signatur Geber auf eine ungültige Weise zu verwenden.<br/></td>
<td>hat folgenden//v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td>Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt wurde nicht initialisiert. <br/> Um das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu initialisieren, legen Sie die <a href="signeddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="signeddata-verify.md"><strong>Verify</strong></a> -Methode.<br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td>Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt enthält einen ungültigen Typ. <br/> Dies geschieht normalerweise, wenn versucht wird, eine eingeschlossene Nachricht mit einem <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu überprüfen, oder umgekehrt.<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td>Das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt wurde nicht signiert. <br/> Um das <a href="signeddata.md"><strong>SignedData</strong></a> -Objekt zu signieren, nennen Sie die <a href="signeddata-sign.md"><strong>Sign</strong></a> -Methode.<br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td>Der Algorithmuswert für die <a href="algorithm-name.md"><strong>Name</strong></a> -Eigenschaft des <a href="algorithm.md"><strong>Algorithmusobjekts</strong></a> ist ungültig. <br/> In der folgenden Liste werden die gültigen algorithmuswerte für die <a href="algorithm-name.md"><strong>Name</strong></a> -Eigenschaft angezeigt:
<ul>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li>
</ul>
<br/></td>
<td>0x80880270</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></td>
<td>Der Wert für die Schlüssellänge der <a href="algorithm-keylength.md"><strong>keylength</strong></a> -Eigenschaft des <a href="algorithm.md"><strong>Algorithmusobjekts</strong></a> ist ungültig. <br/> In der folgenden Liste werden die gültigen Schlüssellängen Werte für die <a href="algorithm-keylength.md"><strong>keylength</strong></a> -Eigenschaft angezeigt:
<ul>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li>
</ul>
<br/></td>
<td>0x80880271</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></td>
<td>Das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt wurde nicht initialisiert. <br/> Um das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt zu initialisieren, legen Sie entweder die <a href="envelopeddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="envelopeddata-decrypt.md"><strong>Entschlüsselungsmethode</strong></a> .<br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td>Das <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt enthält einen ungültigen Typ. <br/> Dies geschieht normalerweise, wenn versucht wird, eine signierte Nachricht mit einem <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt zu überprüfen, oder umgekehrt.<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>Im <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt ist kein Empfänger angegeben, wenn die <a href="envelopeddata-encrypt.md"><strong>Verschlüsselungs</strong></a> Methode eines <strong>EnvelopedData</strong> -Objekts aufgerufen wird. <br/> Um einen Empfänger hinzuzufügen, müssen Sie die Methode " <a href="recipients-add.md"><strong>Empfängers. Add</strong></a> " aufzurufen.<br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>Der Empfänger kann nicht im <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt gefunden werden. <br/> Dies geschieht in der Regel nicht mit einem <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> -Objekt, das von CAPICOM erstellt wurde. Wenn das <strong>EnvelopedData</strong> -Objekt jedoch von einem Drittanbieter Produkt erstellt wurde, ist das Zertifikat des Empfängers möglicherweise nicht in der PKCS-#7 Struktur enthalten.<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td>Das " <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> "-Objekt wurde nicht initialisiert. <br/> Um das <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekt zu initialisieren, legen Sie entweder die <a href="encrypteddata-content.md"><strong>Content</strong></a> -Eigenschaft fest, oder nennen Sie die <a href="encrypteddata-decrypt.md"><strong>Entschlüsselungsmethode</strong></a> .<br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td>Das <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekt ist kein gültiger Typ. <br/> In der Regel bedeutet dies, dass die Daten beschädigt sind.<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td>Das Geheimnis eines <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekts wurde nicht initialisiert. <br/> Um das Geheimnis eines <a href="encrypteddata.md"><strong>verschlüsselteddata</strong></a> -Objekts zu initialisieren, müssen Sie die <a href="encrypteddata-setsecret.md"><strong>setsecret</strong></a> -Methode aufrufen.<br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></td>
<td>Das <a href="privatekey.md"><strong>PrivateKey</strong></a> -Objekt wurde nicht initialisiert.<br/></td>
<td>0x80880300//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></td>
<td>Das <a href="privatekey.md"><strong>PrivateKey</strong></a> -Objekt kann nicht exportiert werden.<br/></td>
<td>0x80880301//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td>Das <a href="encodeddata.md"><strong>encoddata</strong></a> -Objekt wurde nicht initialisiert.<br/></td>
<td>0x80880320//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td>Das <a href="extension.md"><strong>Erweiterungs</strong></a> Objekt wurde nicht initialisiert.<br/></td>
<td>0x80880330//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td>Die <a href="extendedproperty-propid.md"><strong>PROPID</strong></a> -Eigenschaft des <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> -Objekts wurde nicht initialisiert.<br/></td>
<td>0x80880340//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>Der <em>FindType</em> -Parameter der " <a href="certificates-find.md"><strong>Zertifikate. Find</strong></a> "-Methode ist kein Wert der <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> -Enumeration.<br/></td>
<td>0x80880350//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>Die angegebene vordefinierte Richtlinie für den Suchvorgang ist ungültig.<br/></td>
<td>0x80880351//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td>Das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt wurde nicht initialisiert.<br/></td>
<td>0x80880360//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td>Das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt wurde nicht signiert.<br/> Um das <a href="signedcode.md"><strong>signedcode</strong></a> -Objekt zu signieren, nennen Sie die <a href="signedcode-sign.md"><strong>Sign</strong></a> -Methode.<br/></td>
<td>0x80880361//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td>Die <a href="signedcode-description.md"><strong>Description</strong></a> -Eigenschaft des <a href="signedcode.md"><strong>signedcode</strong></a> -Objekts wurde nicht initialisiert.<br/></td>
<td>0x80880362//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td>Die <a href="signedcode-descriptionurl.md"><strong>DescriptionUrl</strong></a> -Eigenschaft des <a href="signedcode.md"><strong>signedcode</strong></a> -Objekts wurde nicht initialisiert.<br/></td>
<td>0x80880363//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td>Der <em>URL</em> -Parameter der <a href="signedcode-timestamp.md"><strong>signedcode. Timestamp</strong></a> -Methode ist ungültig.<br/></td>
<td>0x80880364//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td>Das <a href="hasheddata.md"><strong>hashedData</strong></a> -Objekt enthält keine Daten.<br/></td>
<td>0x80880370//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>Der Typ "Convert" ist ungültig.<br/></td>
<td>0x80880380//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>Der angeforderte Vorgang wird von der aktuellen Plattform nicht unterstützt. <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>Beim Signieren wurde die <a href="signer-certificate.md"><strong>Certificate</strong></a> -Eigenschaft des <a href="signer.md"><strong>Signatur</strong></a> Geber Objekts nicht festgelegt, aber die Eingabeaufforderung für das Benutzerzertifikat wurde deaktiviert. <br/> Aktivieren Sie entweder die Eingabeaufforderung, indem Sie die <a href="settings-enablepromptforcertificateui.md"><strong>enablepromptforcertifitoreui</strong></a> -Eigenschaft des <a href="settings.md"><strong>Settings</strong></a> -Objekts festlegen, oder legen Sie die <a href="signer-certificate.md"><strong>Certificate</strong></a> -Eigenschaft des <a href="signer.md"><strong>Signatur</strong></a> Geber Objekts fest.<br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>Der Vorgang wurde vom Benutzer abgebrochen. <br/> Dies geschieht, wenn der Benutzer aufgefordert wird, eine Berechtigung zum Ausführen eines bestimmten Vorgangs zu erhalten, z. b. den Zugriff auf den privaten Schlüssel, und der Benutzer den Vorgang abbricht.<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>Der versuchte Vorgang ist nicht zulässig.<br/> Beispielsweise ist das Ändern der <a href="extendedproperty-propid.md"><strong>PROPID</strong></a> -Eigenschaft eines <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> -Objekts nicht zulässig, wenn das Objekt an ein Zertifikat angefügt wird.<br/></td>
<td>0x80880903//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>Für CAPICOM steht eine Ressource aus.<br/></td>
<td>0x80880904//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>Ein interner Fehler ist aufgetreten. <br/> Wenden Sie sich an den technischen Support von Microsoft.<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>Ein unbekannter Fehler ist aufgetreten. <br/> Sammeln Sie so viele Informationen wie möglich, und wenden Sie sich an den Hersteller.<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





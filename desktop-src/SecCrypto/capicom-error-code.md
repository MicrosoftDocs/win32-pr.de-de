---
description: Definiert Fehlercodes, die von CAPICOM zurückgegeben werden.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE-Enumeration (Capicom.h)
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
ms.openlocfilehash: abdd2556ace3e3c3c82ccdeedc907d77f9ce1702
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480696"
---
# <a name="capicom_error_code-enumeration"></a>CAPICOM \_ ERROR \_ CODE-Enumeration

Der **CAPICOM \_ ERROR CODE-Enumerationstyp \_** definiert Fehlercodes, die von CAPICOM zurückgegeben werden.

> [!Note]  
> Visual Basic Scripting Edition-Fehler geben einen **Err.number-Wert** größer als 0 (null) zurück. Für diese Fehler geben **die Werte von Err.Description** Informationen zur Ursache des Fehlers an. Zusätzlich zu Visual Basic Scripting Edition-Fehlern geben CAPICOM-Fehler die Codes zurück, die durch **DEN CAPICOM-FEHLERCODE \_ \_** definiert werden.

 

## <a name="members"></a>Member




| Member | BESCHREIBUNG | Wert | 
|--------|-------------|-------|
| <strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong> | Ein ungültiger Codierungstyp wurde verwendet.<br /> Die folgende Liste zeigt die gültigen Codierungstypen:<ul><li>CAPICOM_ENCODE_ANY</li><li>CAPICOM_ENCODE_BASE64</li><li>CAPICOM_ENCODE_BINARY</li></ul><br /> | 0x80880100 | 
| <strong>CAPICOM_E_EKU_INVALID_OID</strong> | Die <a href="eku-oid.md"><strong>OID-Eigenschaft</strong></a> des <a href="eku.md"><strong>EKU-Objekts</strong></a> kann nicht festgelegt werden, da die <a href="eku-name.md"><strong>Name-Eigenschaft</strong></a> nicht auf CAPICOM_EKU_OTHER festgelegt ist.<br /> Legen Sie die <a href="eku-name.md"><strong>Name-Eigenschaft</strong></a> auf CAPICOM_EKU_OTHER fest, bevor Sie die <a href="eku-oid.md"><strong>OID-Eigenschaft</strong></a> festlegen.<br /> | 0x80880200 | 
| <strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong> | Die <a href="eku-oid.md"><strong>OID-Eigenschaft</strong></a> des <a href="eku.md"><strong>EKU-Objekts</strong></a> wurde nicht initialisiert. <br /> Legen Sie entweder die <a href="eku-name.md"><strong>Name-Eigenschaft</strong></a> auf einen anderen Wert als CAPICOM_EKU_OTHER fest, oder legen Sie die <strong>Name-Eigenschaft</strong> auf CAPICOM_EKU_OTHER und die <a href="eku-oid.md"><strong>OID-Eigenschaft</strong></a> auf einen Wert fest.<br /> | 0x80880201 | 
| <strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong> | Das <a href="certificate.md"><strong>Certificate-Objekt</strong></a> wurde nicht initialisiert.<br /> In der Regel wird dieser Fehlercode zurückgegeben, wenn ein <a href="certificate.md"><strong>Certificate-Objekt</strong></a> instanziiert, aber keinem digitalen Zertifikat zugeordnet wird. Um das Objekt einem digitalen Zertifikat zuzuordnen, weisen Sie es entweder einem vorhandenen <strong>Certificate-Objekt</strong> zu, oder rufen Sie die <a href="certificate-import.md"><strong>Import-Methode</strong></a> auf.<br /> | 0x80880210 | 
| <strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong> | Dem <a href="certificate.md"><strong>Certificate-Objekt</strong></a> ist kein privater Schlüssel zugeordnet.<br /> Dieser Fehlercode wird zurückgegeben, wenn versucht wird, Daten mit dem privaten Schlüssel des Signaturgebers zu signieren, aber das <a href="certificate.md"><strong>Certificate-Objekt,</strong></a> das dem <a href="signer.md"><strong>Signierungsobjekt</strong></a> zugeordnet ist, nicht für den Signierungsvorgang verwendet werden kann.<br /> | 0x80880211 | 
| <strong>CAPICOM_E_CHAIN_NOT_BUILT</strong> | Das <a href="chain.md"><strong>Chain-Objekt</strong></a> wurde nicht initialisiert. <br /> Um das <a href="chain.md"><strong>Chain-Objekt</strong></a> zu initialisieren, rufen Sie die <a href="chain-build.md"><strong>Build-Methode</strong></a> auf.<br /> | 0x80880220 | 
| <strong>CAPICOM_E_STORE_NOT_OPENED</strong> | Das <a href="store.md"><strong>Store</strong></a> -Objekt wurde nicht initialisiert. <br /> Um das <a href="store.md"><strong>Store-Objekt</strong></a> zu initialisieren, rufen Sie die <a href="store-open.md"><strong>Open-Methode auf.</strong></a><br /> | 0x80880230 | 
| <strong>CAPICOM_E_STORE_EMPTY</strong> | Das <a href="store.md"><strong>Store-Objekt</strong></a> enthält keine <a href="certificate.md"><strong>Certificate-Objekte.</strong></a><br /> | 0x80880231 | 
| <strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong> | Der <em>OpenMode-Parameter</em> des <a href="store-open.md"><strong>Store. Open-Methode</strong></a> enthält keinen gültigen Wert von CAPICOM_STORE_OPEN_MODE.<br /> Die folgende Liste zeigt die gültigen Werte von CAPICOM_STORE_OPEN_MODE:<ul><li>CAPICOM_STORE_OPEN_READ_ONLY</li><li>CAPICOM_STORE_OPEN_READ_WRITE</li><li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li><li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li><li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li></ul><br /> | 0x80880232 | 
| <strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong> | Der an die <a href="store-export.md"><strong>Export-Methode</strong></a> des <a href="store.md"><strong>Store-Objekts</strong></a> übergebene <em>SaveAs-Wert</em> war ungültig. <br /> Die folgende Liste zeigt die gültigen <em>SaveAs-Werte:</em><ul><li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li><li>CAPICOM_STORE_SAVE_AS_PKCS7</li></ul><br /> | 0x80880233 | 
| <strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong> | Die <a href="attribute-name.md"><strong>Name-Eigenschaft</strong></a> des <a href="attribute.md"><strong>Attribute-Objekts</strong></a> wurde nicht initialisiert. <br /> Legen Sie die <a href="attribute-name.md"><strong>Name-Eigenschaft</strong></a> fest.<br /> | 0x80880240 | 
| <strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong> | Die <a href="attribute-value.md"><strong>Value-Eigenschaft</strong></a> des <a href="attribute.md"><strong>Attribute-Objekts</strong></a> wurde nicht initialisiert. <br /> Legen Sie die <a href="attribute-value.md"><strong>Value-Eigenschaft</strong></a> fest.<br /> | 0x80880241 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong> | Die <a href="attribute-name.md"><strong>Name-Eigenschaft</strong></a> des <a href="attribute.md"><strong>Attribute-Objekts</strong></a> ist ungültig. <br /> Die folgende Liste zeigt die gültigen Attributnamen:<ul><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li></ul><br /> | 0x80880242 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong> | Die <a href="attribute-value.md"><strong>Value-Eigenschaft</strong></a> des <a href="attribute.md"><strong>Attribute-Objekts</strong></a> ist ungültig, da der Datentyp nicht mit dem datentyp übereinstimmt, der durch die <strong>Name-Eigenschaft</strong> angegeben wird. <br /> Wenn die <a href="attribute-value.md"><strong>Name-Eigenschaft</strong></a> beispielsweise auf CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME festgelegt ist, muss der Datentyp <strong>DATE</strong>sein.<br /> | 0x80880243 | 
| <strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong> | Das <a href="signer.md"><strong>Signer-Objekt</strong></a> wurde nicht initialisiert. <br /> Um das <a href="signer.md"><strong>Signer-Objekt</strong></a> zu initialisieren, legen Sie die <a href="signer-certificate.md"><strong>Certificate-Eigenschaft</strong></a> fest.<br /> | 0x80880250 | 
| <strong>CAPICOM_E_SIGNER_NOT_FOUND</strong> | Der Signaturgeber wurde im <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> nicht gefunden. <br /> In der Regel geschieht dies nicht bei einem <a href="signeddata.md"><strong>SignedData-Objekt,</strong></a> das von CAPICOM erstellt wurde. Wenn das <strong>SignedData-Objekt</strong> jedoch von einem Drittanbieterprodukt erstellt wurde, ist das Zertifikat des Signaturgebers möglicherweise nicht in der PKCS #7-Struktur enthalten.<br /> | 0x80880251 | 
| <strong>CAPICOM_E_SIGNER_NO_CHAIN</strong> | Ein <a href="chain.md"><strong>Chain-Objekt</strong></a> wurde im <a href="signer.md"><strong>Signer-Objekt</strong></a> nicht gefunden.<br /> | 0x80880252 / v2.0 | 
| <strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong> | Es wird versucht, den Signierer auf ungültige Weise zu verwenden.<br /> | 0x80880253 "/v2.0" | 
| <strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong> | Das <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> wurde nicht initialisiert. <br /> Um das <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> zu initialisieren, legen Sie die <a href="signeddata-content.md"><strong>Content-Eigenschaft</strong></a> fest, oder rufen Sie die <a href="signeddata-verify.md"><strong>Verify-Methode</strong></a> auf.<br /> | 0x80880260 | 
| <strong>CAPICOM_E_SIGN_INVALID_TYPE</strong> | Das <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> enthält einen ungültigen Typ. <br /> Dies geschieht in der Regel, wenn versucht wird, eine umschlagete Nachricht mit einem <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> zu überprüfen oder umgekehrt.<br /> | 0x80880261 | 
| <strong>CAPICOM_E_SIGN_NOT_SIGNED</strong> | Das <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> wurde nicht signiert. <br /> Um das <a href="signeddata.md"><strong>SignedData-Objekt</strong></a> zu signieren, rufen Sie die <a href="signeddata-sign.md"><strong>Sign-Methode</strong></a> auf.<br /> | 0x80880262 | 
| <strong>CAPICOM_E_INVALID_ALGORITHM</strong> | Der Algorithmuswert für die <a href="algorithm-name.md"><strong>Name-Eigenschaft</strong></a> des <a href="algorithm.md"><strong>Algorithm-Objekts</strong></a> ist ungültig. <br /> Die folgende Liste zeigt die gültigen Algorithmuswerte für die <a href="algorithm-name.md"><strong>Name-Eigenschaft:</strong></a><ul><li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li><li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li><li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li><li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li></ul><br /> | 0x80880270 | 
| <strong>CAPICOM_E_INVALID_KEY_LENGTH</strong> | Der Schlüssellängenwert für die <a href="algorithm-keylength.md"><strong>KeyLength-Eigenschaft</strong></a> des <a href="algorithm.md"><strong>Algorithm-Objekts</strong></a> ist ungültig. <br /> Die folgende Liste zeigt die gültigen Schlüssellängenwerte für die <a href="algorithm-keylength.md"><strong>KeyLength-Eigenschaft:</strong></a><ul><li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li></ul><br /> | 0x80880271 | 
| <strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong> | Das <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> wurde nicht initialisiert. <br /> Um das <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> zu initialisieren, legen Sie entweder die <a href="envelopeddata-content.md"><strong>Content-Eigenschaft</strong></a> fest, oder rufen Sie die <a href="envelopeddata-decrypt.md"><strong>Decrypt-Methode auf.</strong></a><br /> | 0x80880280 | 
| <strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong> | Das <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> enthält einen ungültigen Typ. <br /> Dies geschieht in der Regel, wenn versucht wird, eine signierte Nachricht mit einem <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> zu überprüfen oder umgekehrt.<br /> | 0x80880281 | 
| <strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong> | Im <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> ist kein Empfänger angegeben, wenn die <a href="envelopeddata-encrypt.md"><strong>Encrypt-Methode</strong></a> eines <strong>EnvelopedData-Objekts</strong> aufgerufen wird. <br /> Um einen Empfänger hinzuzufügen, rufen Sie die <a href="recipients-add.md"><strong>Recipients.Add-Methode</strong></a> auf.<br /> | 0x80880282 | 
| <strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong> | Der Empfänger kann im <a href="envelopeddata.md"><strong>EnvelopedData-Objekt</strong></a> nicht gefunden werden. <br /> In der Regel geschieht dies nicht bei einem <a href="envelopeddata.md"><strong>EnvelopedData-Objekt,</strong></a> das von CAPICOM erstellt wurde. Wenn das <strong>EnvelopedData-Objekt</strong> jedoch von einem Drittanbieterprodukt erstellt wurde, ist das Zertifikat des Empfängers möglicherweise nicht in der PKCS #7-Struktur enthalten.<br /> | 0x80880283 | 
| <strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong> | Das <a href="encrypteddata.md"><strong>EncryptedData-Objekt</strong></a> wurde nicht initialisiert. <br /> Um das <a href="encrypteddata.md"><strong>EncryptedData-Objekt</strong></a> zu initialisieren, legen Sie entweder die <a href="encrypteddata-content.md"><strong>Content-Eigenschaft</strong></a> fest, oder rufen Sie die <a href="encrypteddata-decrypt.md"><strong>Decrypt-Methode auf.</strong></a><br /> | 0x80880290 | 
| <strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong> | Das <a href="encrypteddata.md"><strong>EncryptedData-Objekt</strong></a> ist kein gültiger Typ. <br /> In der Regel bedeutet dies, dass die Daten beschädigt sind.<br /> | 0x80880291 | 
| <strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong> | Das Geheimnis eines <a href="encrypteddata.md"><strong>EncryptedData-Objekts</strong></a> wurde nicht initialisiert. <br /> Um das Geheimnis eines <a href="encrypteddata.md"><strong>EncryptedData-Objekts</strong></a> zu initialisieren, rufen Sie die <a href="encrypteddata-setsecret.md"><strong>SetSecret-Methode</strong></a> auf.<br /> | 0x80880292 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong> | Das <a href="privatekey.md"><strong>PrivateKey-Objekt</strong></a> wurde nicht initialisiert.<br /> | 0x80880300 / v2.0 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong> | Das <a href="privatekey.md"><strong>PrivateKey-Objekt</strong></a> kann nicht exportiert werden.<br /> | 0x80880301 / v2.0 | 
| <strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong> | Das <a href="encodeddata.md"><strong>EncodedData-Objekt</strong></a> wurde nicht initialisiert.<br /> | 0x80880320 / v2.0 | 
| <strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong> | Das <a href="extension.md"><strong>Extension-Objekt</strong></a> wurde nicht initialisiert.<br /> | 0x80880330 / v2.0 | 
| <strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong> | Die <a href="extendedproperty-propid.md"><strong>PropID-Eigenschaft</strong></a> des <a href="extendedproperty.md"><strong>ExtendedProperty-Objekts</strong></a> wurde nicht initialisiert.<br /> | 0x80880340 / v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_TYPE</strong> | Der <em>FindType-Parameter</em> der <a href="certificates-find.md"><strong>Certificates.Find-Methode</strong></a> ist kein Wert der <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE-Enumeration.</strong></a><br /> | 0x80880350 / v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong> | Die angegebene vordefinierte Richtlinie für den Suchvorgang ist ungültig.<br /> | 0x80880351 / v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong> | Das <a href="signedcode.md"><strong>SignedCode-Objekt</strong></a> wurde nicht initialisiert.<br /> | 0x80880360 / v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_SIGNED</strong> | Das <a href="signedcode.md"><strong>SignedCode-Objekt</strong></a> wurde nicht signiert.<br /> Um das <a href="signedcode.md"><strong>SignedCode-Objekt</strong></a> zu signieren, rufen Sie die <a href="signedcode-sign.md"><strong>Sign-Methode</strong></a> auf.<br /> | 0x80880361 / v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong> | Die <a href="signedcode-description.md"><strong>Description-Eigenschaft</strong></a> des <a href="signedcode.md"><strong>SignedCode-Objekts</strong></a> wurde nicht initialisiert.<br /> | 0x80880362 / v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong> | Die <a href="signedcode-descriptionurl.md"><strong>DescriptionURL-Eigenschaft</strong></a> des <a href="signedcode.md"><strong>SignedCode-Objekts</strong></a> wurde nicht initialisiert.<br /> | 0x80880363 / v2.0 | 
| <strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong> | Der <em>URL-Parameter</em> der <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp-Methode</strong></a> ist ungültig.<br /> | 0x80880364 / v2.0 | 
| <strong>CAPICOM_E_HASH_NO_DATA</strong> | Das <a href="hasheddata.md"><strong>HashedData-Objekt</strong></a> enthält keine Daten.<br /> | 0x80880370 / v2.0 | 
| <strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong> | Der Konvertierungstyp ist ungültig.<br /> | 0x80880380 / v2.0 | 
| <strong>CAPICOM_E_NOT_SUPPORTED</strong> | Der angeforderte Vorgang wird auf der aktuellen Plattform nicht unterstützt. <br /> | 0x80880900 | 
| <strong>CAPICOM_E_UI_DISABLED</strong> | Beim Signieren wurde die <a href="signer-certificate.md"><strong>Certificate-Eigenschaft</strong></a> des <a href="signer.md"><strong>Signer-Objekts</strong></a> nicht festgelegt, aber die Eingabeaufforderung für das Benutzerzertifikat wurde deaktiviert. <br /> Aktivieren Sie entweder die Eingabeaufforderung, indem Sie die <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI-Eigenschaft</strong></a> des <a href="settings.md"><strong>Einstellungen-Objekts</strong></a> festlegen, oder legen Sie die <a href="signer-certificate.md"><strong>Certificate-Eigenschaft</strong></a> des <a href="signer.md"><strong>Signer-Objekts</strong></a> fest.<br /> | 0x80880901 | 
| <strong>CAPICOM_E_CANCELLED</strong> | Der Vorgang wurde vom Benutzer abgebrochen. <br /> Dies geschieht, wenn der Benutzer aufgefordert wird, die Berechtigung zum Ausführen eines bestimmten Vorgangs zu erteilen, z. B. den Zugriff auf den privaten Schlüssel, und der Benutzer den Vorgang abbricht.<br /> | 0x80880902 | 
| <strong>CAPICOM_E_NOT_ALLOWED</strong> | Der versuchte Vorgang ist nicht zulässig.<br /> Beispielsweise ist das Ändern der <a href="extendedproperty-propid.md"><strong>PropID-Eigenschaft</strong></a> eines <a href="extendedproperty.md"><strong>ExtendedProperty-Objekts</strong></a> nicht zulässig, wenn das Objekt an ein Zertifikat angefügt ist.<br /> | 0x80880903 / v2.0 | 
| <strong>CAPICOM_E_OUT_OF_RESOURCE</strong> | CAPICOM ist keine Ressource mehr.<br /> | 0x80880904 / v2.0 | 
| <strong>CAPICOM_E_INTERNAL</strong> | Ein interner Fehler ist aufgetreten. <br /> Wenden Sie sich an den technischen Support von Microsoft, um Unterstützung zu erhalten.<br /> | 0x80880911 | 
| <strong>CAPICOM_E_UNKNOWN</strong> | Unbekannter Fehler. <br /> Sammeln Sie so viele Informationen wie möglich, und wenden Sie sich an Ihren Anbieter.<br /> | 0x80880999 | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 





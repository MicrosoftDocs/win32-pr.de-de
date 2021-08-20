---
description: Im Folgenden finden Sie die in Cryptxml.h definierten Laufzeitfehlercodes, die von den CryptXML-Funktionen zurückgegeben werden können.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: CryptXML-Fehlercodes (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb4b06070ca77f8b55f96d3e6c4732abc22c26970b83b6a70c720b7bade8a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767977"
---
# <a name="cryptxml-error-codes"></a>CryptXML-Fehlercodes

Im Folgenden finden Sie die in Cryptxml.h definierten Laufzeitfehlercodes, die von den CryptXML-Funktionen zurückgegeben werden können.



| Konstante/Wert                                                                                                                                                                                                                                                                             | Beschreibung                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**CRYPT \_ XML \_ E \_ LARGE**</dt> <dt>0x80092101L</dt> </dl>                                               | Der angegebene Wert ist zu groß.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**CRYPT \_ XML \_ E \_ ENCODING**</dt> <dt>0x80092103L</dt> </dl>                                      | Die angegebene XML-Codierung wird nicht unterstützt.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**CRYPT \_ XML \_ E \_ ALGORITHM**</dt> <dt>0x80092104L</dt> </dl>                                   | Der angegebene XML-Algorithmus wird nicht unterstützt.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**CRYPT \_ XML \_ E \_ TRANSFORM**</dt> <dt>0x80092105L</dt> </dl>                                   | Die angegebene Transformation wird nicht unterstützt.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**CRYPT \_ XML \_ E \_ HANDLE**</dt> <dt>0x80092106L</dt> </dl>                                            | Das angegebene Handle ist ungültig.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**CRYPT \_ XML \_ E \_ OPERATION**</dt> <dt>0x80092107L</dt> </dl>                                   | Der Vorgang ist ungültig.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**CRYPT \_ XML \_ E \_ UNRESOLVED \_ REFERENCE**</dt> <dt>0x80092108L</dt> </dl> | Das **Reference-Element** kann nicht aufgelöst werden.<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ DIGEST**</dt> <dt>0x80092109L</dt> </dl>                   | Der Digestwert ist ungültig.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ SIGNATURE**</dt> <dt>0x8009210AL</dt> </dl>          | Der Signaturwert ist ungültig.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ HASH \_ FAILED**</dt> <dt>0x8009210BL</dt> </dl>                            | Der Hash kann nicht erstellt oder berechnet werden.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGN \_ FAILED**</dt> <dt>0x8009210CL</dt> </dl>                            | Fehler beim Kryptosignaturvorgang.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ VERIFY \_ FAILED**</dt> <dt>0x8009210DL</dt> </dl>                      | Die Signaturüberprüfung ist fehlgeschlagen.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**CRYPT \_ XML \_ E TOO MANY \_ \_ \_ SIGNATURES**</dt> <dt>0x8009210EL</dt> </dl>   | Die Anzahl der **Signature-Elemente** im Dokument hat den maximal zulässigen Grenzwert für die Verarbeitung überschritten.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ KEYVALUE**</dt> <dt>0x8009210FL</dt> </dl>             | Der angegebene Schlüsselwert ist ungültig.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**CRYPT \_ XML \_ E \_ UNEXPECTED \_ XML**</dt> <dt>0x80092110L</dt> </dl>                   | Ungültiger oder unerwarteter XML-Code wurde gefunden.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGNER**</dt> <dt>0x80092111L</dt> </dl>                                            | Der Schlüssel des Signierers konnte nicht gefunden werden.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**CRYPT \_ XML \_ E NON UNIQUE \_ \_ \_ ID**</dt> <dt>0x80092112L</dt> </dl>                     | Ein nicht unmerkliches **ID-Attribut** wurde gefunden.<br/>                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 





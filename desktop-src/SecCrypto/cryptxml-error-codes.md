---
description: Im folgenden finden Sie die Lauf Zeit Fehlercodes, die in "cryptxml. h" definiert sind und von den cryptxml-Funktionen zurückgegeben werden können.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Cryptxml-Fehler Codes (cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364243"
---
# <a name="cryptxml-error-codes"></a>Cryptxml-Fehler Codes

Im folgenden finden Sie die Lauf Zeit Fehlercodes, die in "cryptxml. h" definiert sind und von den cryptxml-Funktionen zurückgegeben werden können.



| Konstante/Wert                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Crypt \_ XML \_ E \_ Large**</dt> <dt>0x80092101l</dt> </dl>                                               | Der angegebene Wert ist zu groß.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Crypt \_ XML \_ E \_ Encoding**</dt> <dt>0x80092103l</dt> </dl>                                      | Die angegebene XML-Codierung wird nicht unterstützt.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Crypt \_ XML \_ E- \_ Algorithmus**</dt> <dt>0x80092104l</dt> </dl>                                   | Der angegebene XML-Algorithmus wird nicht unterstützt.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Crypt \_ XML \_ E \_ Transform**</dt> <dt>0x80092105l</dt> </dl>                                   | Die angegebene Transformation wird nicht unterstützt.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Crypt \_ XML \_ E \_ handle**</dt> <dt>0x80092106l</dt> </dl>                                            | Das angegebene Handle ist ungültig.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Crypt \_ XML \_ E- \_ Vorgang**</dt> <dt>0x80092107l</dt> </dl>                                   | Der Vorgang ist ungültig.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Crypt \_ Nicht \_ aufgelöster XML- \_ \_ Verweis**</dt> <dt>0x80092108l</dt> </dl> | Das **Verweis** Element kann nicht aufgelöst werden.<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Crypt \_ \_ \_ Ungültiger \_ XML**</dt> -Code (Digest) <dt>0x80092109l</dt> </dl>                   | Der Digest-Wert ist ungültig.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Crypt \_ XML \_ E \_ ungültige \_ Signatur**</dt> <dt>0x8009210al</dt> </dl>          | Der Signatur Wert ist ungültig.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Crypt \_ Fehler beim XML- \_ E- \_ \_ Hash**</dt> <dt>0x8009210bl</dt> . </dl>                            | Der Hash kann nicht erstellt oder berechnet werden.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Crypt \_ Fehler bei der XML- \_ E- \_ Signatur \_**</dt> <dt>0x8009210cl</dt> </dl>                            | Fehler bei der kryptografischen Signatur.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Crypt \_ XML \_ E \_ Verify \_**</dt> Fehler <dt>0x8009210dl</dt> </dl>                      | Die Signaturüberprüfung ist fehlgeschlagen.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Crypt \_ XML \_ E \_ zu \_ viele \_ Signaturen**</dt> <dt>0x8009210el</dt> </dl>   | Die Anzahl der **Signatur** Elemente im Dokument hat das maximal zulässige Limit für die Verarbeitung überschritten.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Crypt \_ XML \_ E \_ ungültige \_ KeyValue**</dt> <dt>0x8009210fl</dt> </dl>             | Der angegebene Schlüsselwert ist ungültig.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Crypt \_ XML \_ E \_ unerwartetes \_ XML**</dt> <dt>0x80092110l</dt> </dl>                   | Ungültiges oder unerwartetes XML wurde gefunden.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Crypt \_ XML \_ E \_ Signatur**</dt> Geber <dt>0x80092111l</dt> </dl>                                            | Der Schlüssel des Signatur Gebers konnte nicht gefunden werden.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Crypt \_ \_Nicht eindeutige XML E- \_ \_ \_ ID**</dt> <dt>0x80092112l</dt> </dl>                     | Es wurde ein nicht eindeutiges **ID** -Attribut gefunden.<br/>                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 





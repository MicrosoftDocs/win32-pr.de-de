---
description: Cryptxml definiert die folgenden globalen Grenzwerte in der Header Datei "cryptxml. h".
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Cryptxml-Limits (cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484598"
---
# <a name="cryptxml-limits"></a>Kryptotxml-Limits

Cryptxml definiert die folgenden globalen Grenzwerte in der Header Datei "cryptxml. h".



| Konstante/Wert                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**Crypt \_ XML- \_ BLOB \_ Max**</dt> <dt>0x7ffffff8</dt> </dl>                             | Codierte Daten dürfen 2 Gigabyte (GB) nicht überschreiten.<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**Crypt \_ XML- \_ ID \_ Max**</dt> . <dt>256</dt> </dl>                                          | Die ID darf nicht länger als 256 Zeichen sein.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**Crypt \_ \_ \_ Maximale XML-URI**</dt> <dt>8 \* 1024</dt> </dl>                                   | Die URI-Länge darf nicht länger als 8192 Zeichen sein.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**Crypt \_ XML- \_ Signaturen \_ Max**</dt> . <dt>16</dt> </dl>                   | Die standardmäßige maximale Anzahl von **Signatur** Elementen pro Dokument. Dieser Wert kann überschrieben werden, indem ein neuer Höchstwert angegeben wird, wenn Eigenschaftswerte als [**crypt \_ XML- \_ Eigenschafts**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) Strukturen übergeben werden.<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**Crypt \_ \_ \_ Maximal**</dt> <dt>16</dt> XML-Transformation </dl>                      | Die maximale Anzahl von Transformationen (dargestellt durch [**crypt- \_ XML- \_ algorithmusstrukturen**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) ) pro Verweis, dargestellt durch eine [**crypt XML- \_ \_ Verweis**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) Struktur.<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**Crypt \_ XML- \_ Signatur \_ Wert \_ Max**</dt> . <dt>2048</dt> </dl> | Die maximale Länge einer [**crypt- \_ XML- \_ Signatur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) Struktur in Bytes.<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**Crypt \_ XML \_ Digest- \_ Wert \_ Max**</dt> <dt>128</dt> </dl>           | Die maximale Länge eines Digest in Byte.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**Crypt \_ XML- \_ Objekte \_ Max**</dt> . <dt>256</dt> </dl>                           | Wird intern verwendet, um die maximale Anzahl der pro Signatur zulässigen **Objekt** Elemente anzugeben.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**Crypt \_ XML- \_ Verweise \_ Max**</dt> <dt>0x7ff8</dt> </dl>               | Die maximal zulässige Anzahl von **Verweis** Elementen.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 





---
description: CryptXML definiert die folgenden globalen Grenzwerte in der Headerdatei Cryptxml.h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: CryptXML-Grenzwerte (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a0dcdf5dc8f8bd9efed4dcdb15ca316ecb1645e5775f3d714f46c6835b3a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100920"
---
# <a name="cryptxml-limits"></a>CryptXML-Grenzwerte

CryptXML definiert die folgenden globalen Grenzwerte in der Headerdatei Cryptxml.h.



| Konstante/Wert                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**CRYPT \_ XML \_ BLOB \_ MAX**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | Codierte Daten dürfen 2 GIGABYTE (GB) nicht überschreiten.<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**CRYPT \_ \_XML-ID \_ MAX.**</dt> <dt>256</dt> </dl>                                          | Die ID-Länge darf 256 Zeichen nicht überschreiten.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**CRYPT \_ \_XML-URI \_ MAX**</dt> <dt>8 \* 1024</dt> </dl>                                   | Die URI-Länge darf 8192 Zeichen nicht überschreiten.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**CRYPT \_ XML \_ SIGNATURES \_ MAX**</dt> <dt>16</dt> </dl>                   | Die maximale Standardanzahl von **Signaturelementen** pro Dokument. Dieser Wert kann überschrieben werden, indem beim Übergeben von Eigenschaftswerten als [**CRYPT \_ XML \_ PROPERTY-Strukturen**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) ein neues Maximum angegeben wird.<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**CRYPT \_ XML \_ TRANSFORM \_ MAX**</dt> <dt>16</dt> </dl>                      | Die maximale Anzahl von Transformationen, dargestellt durch [**CRYPT \_ XML \_ ALGORITHM-Strukturen,**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) pro Verweis, dargestellt durch eine [**CRYPT XML \_ \_ REFERENCE-Struktur.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference)<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**CRYPT \_ XML SIGNATURE \_ \_ VALUE \_ MAX**</dt> <dt>2048</dt> </dl> | Die maximale Länge einer [**CRYPT \_ XML \_ SIGNATURE-Struktur**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) in Bytes.<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**CRYPT \_ XML \_ DIGEST \_ VALUE \_ MAX**</dt> <dt>128</dt> </dl>           | Die maximale Länge eines Digests in Bytes.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**CRYPT \_ \_XML-OBJEKTE \_ MAX.**</dt> <dt>256</dt> </dl>                           | Wird intern verwendet, um die maximale Anzahl von **Object-Elementen** anzugeben, die pro Signatur zulässig sind.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**CRYPT \_ XML \_ REFERENCES \_ MAX**</dt> <dt>0x7FF8</dt> </dl>               | Die maximal zulässige Anzahl von **Verweiselementen.**<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 





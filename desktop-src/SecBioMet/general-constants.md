---
title: Allgemeine Konstanten (winbio \_ types. h)
description: Geben Sie maximale SID-Länge, Handles, IDs, maximale Zeichen folgen Länge und maximale Puffergröße an.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956465"
---
# <a name="general-constants-winbio_typesh"></a>Allgemeine Konstanten (winbio \_ types. h)

Die folgenden Konstanten werden in der Windows-Biometrieframework verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_Maximale \_ sid- \_ Größe der Sicherheit**</dt> </dl>                                                                                          | Die maximale Länge eines SID-Werts (Security Identifier). Derzeit ist dies 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**winbio- \_ Einheits- \_ ID**</dt> </dl>                                                                                                                | ID-Nummer einer biometrischen Einheit.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**winbio- \_ Sitzungs \_ handle**</dt> </dl>                                                                                           | Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine geöffnete biometrische Sitzung enthält.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**winbio \_ Framework- \_ handle**</dt> </dl>                                                                                     | Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine geöffnete Framework-Sitzung enthält.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**winbio- \_ UUID**</dt> </dl>                                                                                                                          | Ein GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**winbio- \_ Zeichenfolge**</dt> </dl>                                                                                                                    | Ein Bytearray, das eine NULL-terminierte Unicode-Zeichenfolge enthält.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**Winbio \_ Max. \_ Zeichenfolge \_ len**</dt> </dl>                                                                                       | Die maximale Länge eines **winbio- \_ Zeichen** folgen Werts. Derzeit ist dies 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**Winbio \_ Maximale \_ \_ Puffer \_ Größe**</dt> <dt>0x7FFFFFFF</dt> </dl> | Die maximale Anzahl von Bytes in einer einzelnen biometrischen Datenerfassung.<br/>                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 






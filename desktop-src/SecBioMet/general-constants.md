---
title: Allgemeine Konstanten (Winbio \_ types.h)
description: Geben Sie die maximale SID-Länge, Handles, IDs, die maximale Zeichenfolgenlänge und die maximale Stichprobenpuffergröße an.
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
ms.openlocfilehash: 686e94c936855d3b5466071fba7d8b629a492579de11a53a62d8b23345707c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740449"
---
# <a name="general-constants-winbio_typesh"></a>Allgemeine Konstanten (Winbio \_ types.h)

Die folgenden Konstanten werden im gesamten Biometrieframework Windows verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                   | Beschreibung                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**MAXIMALE \_ \_ SICHERHEITS-SID-GRÖßE \_**</dt> </dl>                                                                                          | Die maximale Länge eines SID-Werts (Security Identifier). Derzeit ist dies 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_WINBIO-EINHEITEN-ID \_**</dt> </dl>                                                                                                                | ID-Nummer einer biometrischen Einheit.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_WINBIO-SITZUNGSHAND \_ HANDLE**</dt> </dl>                                                                                           | Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine offene biometrische Sitzung enthält.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**WINBIO \_ \_ FRAMEWORK-HANDLE**</dt> </dl>                                                                                     | Eine lange ganze Zahl ohne Vorzeichen, die das Handle für eine geöffnete Frameworksitzung enthält.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**WINBIO \_ UUID**</dt> </dl>                                                                                                                          | Ein GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**WINBIO \_ STRING**</dt> </dl>                                                                                                                    | Ein Bytearray, das eine auf NULL terminierte Unicode-Zeichenfolge enthält.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ MAX \_ STRING \_ LEN**</dt> </dl>                                                                                       | Die maximale Länge eines **WINBIO \_ STRING-Werts.** Derzeit ist dies 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ MAX \_ SAMPLE BUFFER SIZE \_ \_ 0X7FFFFFFF**</dt> <dt></dt> </dl> | Die maximale Anzahl von Bytes in einer einzelnen biometrischen Datenerfassung.<br/>                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungskonstant](client-application-constants.md)
</dt> </dl>

 

 






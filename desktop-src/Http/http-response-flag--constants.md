---
title: HTTP_RESPONSE_FLAG_ Konstanten (http. h)
description: Definieren Sie die Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337503"
---
# <a name="http_response_flag_-constants"></a>HTTP \_ - \_ antwortflag- \_ Konstanten

Die **http \_ - \_ antwortflag \_** -Konstanten definieren Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.

Diese Konstanten werden im **Flags** -Member der HTTP- [**\_ Antwort \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) -Struktur verwendet.

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP- \_ Antwort Kennzeichen \_ \_ mehrere \_ Codierungen \_ verfügbar**
</dt> <dd> <dl> <dt>



Andere Codierungen als das Identitäts Formular sind für diese Ressource verfügbar. Dieses Flag wird ignoriert, wenn die Anwendung nicht zum Zwischenspeichern aufgefordert wurde. Sie wird als Hinweis für die HTTP-Server-API für die Aushandlung von Inhalten verwendet, wenn Sie aus dem Kernel-Antwort Cache bedient wird.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[HTTP-Server-API, Version 2,0, Konstanten](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP- \_ Antwort \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 






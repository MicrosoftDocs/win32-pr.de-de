---
title: HTTP_RESPONSE_FLAG_ Konstanten (Http.h)
description: Definieren Sie Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.
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
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394408"
---
# <a name="http_response_flag_-constants"></a>HTTP \_ RESPONSE \_ \_ FLAG-Konstanten

Die **HTTP \_ RESPONSE \_ \_ FLAG-Konstanten** definieren Optionen zum Konfigurieren von Antworten in der HTTP-Server-API.

Diese Konstanten werden im **Flags-Member** der [**HTTP RESPONSE \_ \_ V1-Struktur**](/windows/desktop/api/Http/ns-http-http_response_v1) verwendet.

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_ \_ HTTP-ANTWORTFLAG: \_ MEHRERE \_ CODIERUNGEN \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>



Für diese Ressource sind andere Codierungen als identitätsformulare verfügbar. Dieses Flag wird ignoriert, wenn die Anwendung nicht angefordert hat, dass die Antwort zwischengespeichert wird. Sie wird als Hinweis auf die HTTP-Server-API für die Inhaltsaushandlung verwendet, wenn sie aus dem Kernelantwortcache bereitgestellt wird.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[HTTP-Server-API- Version 2.0-Konstanten](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP \_ RESPONSE \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 






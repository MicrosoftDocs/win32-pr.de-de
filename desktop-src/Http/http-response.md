---
title: HTTP_RESPONSE (Http.h)
description: 'Die Version der HTTP \_ RESPONSE-Struktur hängt von der Version der Anforderungswarteschlange ab, die wie folgt verwendet wird: HTTP Server API Version 1.0 request queue (Http-Anforderungswarteschlange Version 1.0). Dies ist eine HTTP \_ REQUEST \_ V1-Struktur. HTTP-Server-API Version 2.0 Anforderungswarteschlange Dies ist eine HTTP \_ REQUEST \_ V2-Struktur.'
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1dea22be8727307a403d17ff383228187ead294128b4c0f0b05b8c0e84301b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996316"
---
# <a name="http_response"></a>\_HTTP-ANTWORT

Die Version der **HTTP \_ RESPONSE-Struktur** hängt von der Version der Anforderungswarteschlange ab, die wie folgt verwendet wird:

-   HTTP Server API Version 1.0 request queue (Anforderungswarteschlange der HTTP-Server-API Version 1.0): Dies ist eine [**HTTP \_ REQUEST \_ V1-Struktur.**](/windows/desktop/api/Http/ns-http-http_request_v1)
-   HTTP Server API Version 2.0 request queue (Anforderungswarteschlange für HTTP-Server-API Version 2.0): Dies ist eine [**HTTP \_ REQUEST \_ V2-Struktur.**](/windows/desktop/api/Http/ns-http-http_request_v2)

Verwenden Sie [**HTTP \_ REQUEST \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) und [**HTTP REQUEST \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) nicht direkt in Ihrem Code. Die Verwendung von **HTTP \_ RESPONSE** stellt stattdessen sicher, dass die richtige Version der Struktur basierend auf der Version der Anforderungswarteschlange verwendet wird.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**\_HTTP-ANTWORT**
</dt> <dd>

Die Anforderung stammte aus einer v1-Anforderungswarteschlange.

</dd> <dt>

**\_HTTP-ANTWORT**
</dt> <dd>

Die Anforderung stammte aus einer v2-Anforderungswarteschlange.

</dd> <dt>

**\_PHTTP-ANTWORT**
</dt> <dd>

Zeiger auf eine **HTTP \_ RESPONSE-Struktur.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



 

 






---
title: HTTP_RESPONSE (http. h)
description: Die Version der HTTP- \_ Antwort Struktur ist abhängig von der Version der Anforderungs Warteschlange, die der HTTP-Server-API Version 1,0-Anforderungs Warteschlange verwendet wird. Dies ist eine HTTP- \_ Anforderung \_ v1-Struktur. Http-Server-API Version 2,0 Anforderungs Warteschlange Dies ist eine HTTP- \_ Anforderung \_ v2-Struktur.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391782"
---
# <a name="http_response"></a>HTTP- \_ Antwort

Die Version der **http- \_ Antwort** Struktur ist abhängig von der Version der Anforderungs Warteschlange, die wie folgt verwendet wird:

-   Http Server-API, Version 1,0, Anforderungs Warteschlange: Dies ist eine [**http- \_ Anforderung \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) -Struktur.
-   Http-Server-API, Version 2,0, Anforderungs Warteschlange: Dies ist eine [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) -Struktur.

Verwenden Sie [**http- \_ Anforderungen \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) und [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) nicht direkt in Ihrem Code. bei Verwendung der **http- \_ Antwort** wird stattdessen sichergestellt, dass die richtige Version der Struktur basierend auf der Version der Anforderungs Warteschlange verwendet wird.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**HTTP- \_ Antwort**
</dt> <dd>

Die Anforderung erfolgte aus einer v1-Anforderungs Warteschlange.

</dd> <dt>

**HTTP- \_ Antwort**
</dt> <dd>

Die Anforderung erfolgte aus einer v2-Anforderungs Warteschlange.

</dd> <dt>

**Phttp- \_ Antwort**
</dt> <dd>

Zeiger auf eine **http- \_ Antwort** Struktur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http. h</dt> </dl> |



 

 






---
description: Gibt einen Socketdeskriptor an, der von Sende- und Empfangsanforderungen mit den bei Winsock registrierten E/A-Erweiterungen verwendet wird.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162b87d1ae320bfa0e74f08e5a0ef7493c053f39573249246e8b2884e74f599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993580"
---
# <a name="rio_rq"></a>RIO \_ RQ

Die **\_ RQ-Typedef** von RIO gibt einen Socketdeskriptor an, der von Sende- und Empfangsanforderungen mit den bei Winsock registrierten E/A-Erweiterungen verwendet wird.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

Ein Datentyp, der einen Socketdeskriptor angibt, der von Sende- und Empfangsanforderungen verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die bei Winsock registrierten E/A-Erweiterungen arbeiten in erster Linie mit einem **\_ RQ-Objekt** von AME anstelle eines Sockets. Eine Anwendung erhält mithilfe der [**FUNKTION RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) eine **RIO \_ RQ** für einen vorhandenen Socket. Der Eingabesocket muss erstellt worden sein, indem die [**WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mit dem im *dwFlags-Parameter* festgelegten **Flag WSA \_ FLAG FLAG \_ ERSTELLT** wurde.

Nach dem Abrufen eines **RIO \_ RQ-Objekts** bleibt der zugrunde liegende Socketdeskriptor gültig. Eine Anwendung verwendet möglicherweise weiterhin den zugrunde liegenden Socket zum Festlegen und Abfragen von Socketoptionen, gibt IOCTLs aus und schließt schließlich den Socket.

> [!Note]  
> Aus Effizienzgründen wird der Zugriff auf die Vervollständigungswarteschlangen [**(RIO \_ CQ-Strukturen)**](riocqueue.md) und Anforderungswarteschlangen **(RIO \_ RQ-Strukturen)** nicht durch Synchronisierungsprimitiven geschützt. Wenn Sie von mehreren Threads aus auf eine Abschluss- oder Anforderungswarteschlange zugreifen müssen, sollte der Zugriff von einem kritischen Abschnitt, einer Schreibsperre für Den Reader oder einem ähnlichen Mechanismus koordiniert werden. Diese Sperrung ist für den Zugriff durch einen einzelnen Thread nicht erforderlich. Verschiedene Threads können ohne Sperren auf separate Anforderungen/Vervollständigungswarteschlangen zugreifen. Die Synchronisierung ist nur erforderlich, wenn mehrere Threads versuchen, auf dieselbe Warteschlange zu zugreifen. Eine Synchronisierung ist auch erforderlich, wenn mehrere Threads über denselben Socket senden und empfangen, da die Sende- und Empfangsvorgänge die Anforderungswarteschlange des Sockets verwenden.

 

Die [**\_ TYPDEFINITION FÜR DIE RQ**](riocqueue.md) wird in der *Headerdatei "Mswsockdef.h"* definiert, die automatisch in der *Headerdatei "Mswsock.h"* enthalten ist. Die *Headerdatei "Mswsockdef.h"* sollte nie direkt verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mswsockdef.h (einschließlich Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 

---
description: Gibt einen registrierten Pufferdeskriptor an, der mit den bei Winsock registrierten E/A-Erweiterungen verwendet wird.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bde67e14a1cb591922ddc180ab8f308b8429c2b36c5998d313876200cd3a26c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097550"
---
# <a name="rio_bufferid"></a>RIO \_ BUFFERID

Die **RIO \_ BUFFERID-Typdefinition** gibt einen registrierten Pufferdeskriptor an, der mit den registrierten E/A-Erweiterungen von Winsock verwendet wird.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ BUFFERID**
</dt> <dd>

Ein -Datentyp, der einen registrierten Pufferdeskriptor angibt, der mit Sende- und Empfangsanforderungen verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die registrierten E/A-Erweiterungen von Winsock arbeiten hauptsächlich mit registrierten Puffern mithilfe von **RIO \_ BUFFERID-Objekten.** Eine Anwendung ruft mithilfe der [**RIORegisterBuffer-Funktion**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) eine **RIO \_ BUFFERID** für einen vorhandenen Puffer ab. Eine Anwendung kann eine Registrierung mithilfe der [**RIODeregisterBuffer-Funktion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) freigeben.

Wenn ein vorhandener Puffer mithilfe der [**FUNKTION RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) als **RIO \_ BUFFERID-Objekt** registriert wird, werden bestimmte interne Ressourcen aus dem physischen Speicher zugeordnet, und der vorhandene Anwendungspuffer wird in den physischen Speicher gesperrt. Die [**RIODeregisterBuffer-Funktion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) wird aufgerufen, um die Registrierung des Puffers aufzuheben, diese internen Ressourcen freizugeben und zuzulassen, dass der Puffer entsperrt und aus dem physischen Speicher freigegeben wird.

Die wiederholte Registrierung und Deregistrierung von Anwendungspuffern mithilfe der bei Winsock registrierten E/A-Erweiterungen kann zu erheblichen Leistungseinbußen führen. Die folgenden Pufferverwaltungsansätze sollten beim Entwerfen einer Anwendung mithilfe der bei Winsock registrierten E/A-Erweiterungen berücksichtigt werden, um die wiederholte Registrierung und Deregistrierung von Anwendungspuffern zu minimieren:

-   • Maximieren der Wiederverwendung von Puffern.
-   • Verwalten Sie einen begrenzten Pool von nicht verwendeten registrierten Puffern für die Verwendung durch die Anwendung.
-   • Verwalten Sie einen begrenzten Pool registrierter Puffer, und führen Sie Pufferkopien zwischen diesen registrierten Puffern und anderen nicht registrierten Puffern aus.

Die **RIO \_ BUFFERID-Typdefinition** wird in der *Headerdatei Mswsockdef.h* definiert, die automatisch in der *Headerdatei "Mswsock.h"* enthalten ist. Die *Headerdatei Mswsockdef.h* sollte nie direkt verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mswsockdef.h (einschließlich Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RIO \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 

---
description: Gibt einen registrierten Puffer Deskriptor an, der mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (mtausockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042011"
---
# <a name="rio_bufferid"></a>Rio \_ -bufferid

Die " **Rio \_ bufferid** typedef" gibt einen registrierten Puffer Deskriptor an, der mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**Rio \_ -bufferid**
</dt> <dd>

Ein Datentyp, der einen registrierten Puffer Deskriptor angibt, der mit Sende-und Empfangs Anforderungen verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die registrierten Winsock-e/a-Erweiterungen arbeiten hauptsächlich bei registrierten Puffern mit **Rio \_ -bufferid-** Objekten. Eine Anwendung erhält mit der [**rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) -Funktion eine **Rio \_ -bufferid** für einen vorhandenen Puffer. Eine Anwendung kann mithilfe der [**rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) -Funktion eine Registrierung freigeben.

Wenn ein vorhandener Puffer mithilfe der [**rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) -Funktion als **Rio \_ -bufferid-** Objekt registriert wird, werden bestimmte interne Ressourcen aus physischem Speicher zugeordnet, und der vorhandene Anwendungs Puffer wird in den physischen Speicher gesperrt. Die [**rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) -Funktion wird aufgerufen, um die Registrierung des Puffers aufzuheben, diese internen Ressourcen freizugeben und zuzulassen, dass der Puffer entsperrt und aus physischem Speicher freigegeben werden kann.

Die wiederholte Registrierung und Aufhebung der Registrierung von Anwendungs Puffern mithilfe der registrierten e/a-Erweiterungen von Winsock kann zu erheblichen Leistungseinbußen führen. Die folgenden Puffer Verwaltungsansätze sollten beim Entwerfen einer Anwendung mit den Winsock-registrierten e/a-Erweiterungen berücksichtigt werden, um die wiederholte Registrierung und Registrierung von Anwendungs Puffern zu minimieren:

-   • Maximieren Sie die Wiederverwendung von Puffern.
-   • Bewahren Sie einen eingeschränkten Pool nicht verwendeter registrierter Puffer für die Verwendung durch die Anwendung auf.
-   • Behalten Sie einen eingeschränkten Pool registrierter Puffer bei, und führen Sie Puffer Kopien zwischen diesen registrierten Puffern und anderen nicht registrierten Puffern aus.

Die typedef " **Rio \_ bufferid** " wird in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist. Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mtausockdef. h (Include mtausock. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rio \_ buf**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**Rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**Rioreceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**Rioreceiveex**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**Rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**Randalisend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**Riosendex**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 

---
description: Gibt einen socketdeskriptor an, der von Sende-und Empfangs Anforderungen mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (mtausockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344739"
---
# <a name="rio_rq"></a>Rio \_ RQ

Die **Rio \_ RQ** -typedef gibt einen socketdeskriptor an, der von Sende-und Empfangs Anforderungen mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**Rio \_ RQ**
</dt> <dd>

Ein Datentyp, der einen von Sende-und Empfangs Anforderungen verwendeten socketdeskriptor angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die registrierten Winsock-e/a-Erweiterungen arbeiten hauptsächlich auf einem **Rio- \_ RQ** -Objekt und nicht auf einem Socket. Eine Anwendung erhält einen **Rio \_ RQ** für einen vorhandenen Socket mithilfe der " [**riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) "-Funktion. Der Eingabe Socket muss durch Aufrufen der [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion erstellt worden sein, wobei das **WSA- \_ Flag " \_ Rio** " im Parameter " *dwFlags* " festgelegt ist.

Nachdem Sie ein **Rio- \_ RQ** -Objekt abgerufen haben, bleibt der zugrunde liegende socketdeskriptor gültig. Eine Anwendung kann den zugrunde liegenden Socket weiterhin verwenden, um Socketoptionen festzulegen und abzufragen, IOCTLs auszugeben und schließlich den Socket zu schließen.

> [!Note]  
> Der Zugriff auf die Vervollständigungs Warteschlangen ([**Rio- \_ CQ**](riocqueue.md) -Strukturen) und Anforderungs Warteschlangen (**Rio \_ RQ** -Strukturen) werden aus Gründen der Effizienz nicht durch Synchronisierungs primitive geschützt. Wenn Sie von mehreren Threads auf eine Vervollständigungs-oder Anforderungs Warteschlange zugreifen müssen, sollte der Zugriff durch einen kritischen Abschnitt, eine schlanke Schreibsperre für Lesevorgänge oder einen ähnlichen Mechanismus koordiniert werden. Diese Sperrung wird nicht für den Zugriff durch einen einzelnen Thread benötigt. Verschiedene Threads können ohne Sperren auf separate Anforderungen/Vervollständigungs Warteschlangen zugreifen. Die Synchronisierung ist nur dann erforderlich, wenn mehrere Threads versuchen, auf dieselbe Warteschlange zuzugreifen. Die Synchronisierung ist auch erforderlich, wenn von mehreren Threads im gleichen Socket gesendet und empfangen wird, da die Sende-und Empfangs Vorgänge die Anforderungs Warteschlange des Sockets verwenden.

 

Die [**Rio \_ RQ**](riocqueue.md) -TypeDef ist in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist. Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mtausockdef. h (Include mtausock. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**Rioreceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**Rioreceiveex**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**Rioresizerequestqueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**Randalisend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**Riosendex**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**Wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 

---
description: Gibt einen Vervollständigungs Warteschlangen Deskriptor an, der für e/a-Abschluss Benachrichtigungen durch Senden und empfangen von Anforderungen mit den Winsock-registrierten e/a-Erweiterungen verwendet wird.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348305"
---
# <a name="rio_cq"></a>Rio, \_ CQ

Die **Rio \_** -Klasse "CQ typedef" gibt einen Vervollständigungs Warteschlangen Deskriptor an, der für e/a-Abschluss Benachrichtigungen verwendet wird, indem Sende-und Empfangs Anforderungen mit den registrierten e/a-Erweiterungen


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**Rio, \_ CQ**
</dt> <dd>

Ein Datentyp, der einen Vervollständigungs Warteschlangen Deskriptor angibt, der von Sende-und Empfangs Anforderungen für die e/a-Abschluss Benachrichtigung verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **Rio \_** -Objekt "CQ" wird für e/a-Abschluss Benachrichtigungen von Sende-und Empfangs Netzwerk Anforderungen von den registrierten e/a-Erweiterungen von Winsock verwendet.

Eine Anwendung kann die [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Funktion verwenden, um eine Benachrichtigung anzufordern, wenn die Abschluss Warteschlange von **Rio \_ CQ** nicht leer ist. Eine Anwendung kann den Status auch jederzeit in einer **Rio- \_ CQ** -Vervollständigungs Warteschlange auf nicht blockierende Weise Abfragen, indem die [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) -Funktion verwendet wird.

Das **Rio \_** -Objekt "CQ" wird mit der Funktion " [**riokreatecompletionqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) " erstellt. Zum Zeitpunkt der Erstellung muss die Anwendung die Größe der Warteschlange angeben, die bestimmt, wie viele Vervollständigungs Einträge enthalten sein können. Wenn eine Anwendung die [**riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) -Funktion aufruft, um ein [**Rio \_ RQ**](riorqueue.md) -Handle abzurufen, muss die Anwendung einen **Rio- \_ CQ** -Handle für Sende Vervollständigungen und einen **Rio- \_ CQ** -Handle für Empfangs Vervollständigungen angeben. Diese Handles können identisch sein, wenn die gleiche Warteschlange für Sende-und Empfangs Vervollständigung verwendet werden soll. Die **riokreaterequestqueue** -Funktion erfordert auch eine maximale Anzahl von ausstehenden Sende-und Empfangs Vorgängen, die mit der Kapazität der zugehörigen Vervollständigungs Warteschlange oder Warteschlangen abgerechnet werden. Wenn die Warteschlangen nicht über genügend Kapazität verfügen, tritt beim Aufrufen von " **riokreaterequestqueue** " ein Fehler mit [WSAENOBUFS](windows-sockets-error-codes-2.md)auf.

Das Benachrichtigungs Verhalten für eine Vervollständigungs Warteschlange wird festgelegt, wenn **Rio \_ CQ** erstellt wird.

Für eine Vervollständigungs Warteschlange, die ein Ereignis verwendet, wird das **typmitglied** der [**Rio- \_ Benachrichtigungs \_ Vervollständigungs**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) Struktur auf die **\_ Ereignis \_ Vervollständigung Rio** festgelegt. Der **Event. EventHandle** -Member sollte das Handle für ein Ereignis enthalten, das von der [**wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) -Funktion oder der-Funktion für die Funktion " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " Um den [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Abschluss zu erhalten, sollte die Anwendung auf das angegebene Ereignis Handle mithilfe von [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) oder einer ähnlichen warte Routine warten. Wenn die Anwendung das Zurücksetzen und wieder verwenden des Ereignisses plant, kann die Anwendung den mehr Aufwand verringern, indem das **Event. notifyreset** -Element auf einen Wert ungleich 0 (null) festgelegt wird. Dies bewirkt, dass das Ereignis automatisch von der **rionotify** -Funktion zurückgesetzt wird, wenn die Benachrichtigung erfolgt. Dadurch wird verhindert, dass die [**wsaresetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) -Funktion aufgerufen werden muss, um das Ereignis zwischen Aufrufen der **rionotify** -Funktion zurückzusetzen.

Für eine Vervollständigungs Warteschlange, die einen e/a-Abschlussport verwendet, wird das **typmitglied** der [**Rio- \_ Benachrichtigungs \_ Vervollständigungs**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) Struktur auf **Rio \_ IOCP \_ completion** festgelegt. Der **IOCP. iocphandle** -Member sollte das Handle für einen e/a-Abschlussport enthalten, der von der Funktion " [**deeiocompletionport**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) " erstellt wurde. Um den [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Abschluss zu erhalten, sollte die Anwendung die Funktion [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) oder [**getqueuedcompletionstatusex**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) aufrufen. Die Anwendung sollte ein dediziertes [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Endes Objekt für die Vervollständigungs Warteschlange bereitstellen, und es kann auch das Element **IOCP. completionkey** verwenden, um **rionotify** -Anforderungen in der Vervollständigungs Warteschlange von anderen e/a-Vervollständigungen zu unterscheiden, einschließlich **rionotifiktionen** für andere Vervollständigungs Warteschlangen

> [!Note]  
> Der Zugriff auf die Vervollständigungs Warteschlangen (**Rio- \_ CQ** -Strukturen) und Anforderungs Warteschlangen ([**Rio \_ RQ**](riorqueue.md) -Strukturen) werden aus Gründen der Effizienz nicht durch Synchronisierungs primitive geschützt. Wenn Sie von mehreren Threads auf eine Vervollständigungs-oder Anforderungs Warteschlange zugreifen müssen, sollte der Zugriff durch einen kritischen Abschnitt, eine schlanke Schreibsperre für Lesevorgänge oder einen ähnlichen Mechanismus koordiniert werden. Diese Sperrung wird nicht für den Zugriff durch einen einzelnen Thread benötigt. Verschiedene Threads können ohne Sperren auf separate Anforderungen/Vervollständigungs Warteschlangen zugreifen. Die Synchronisierung ist nur dann erforderlich, wenn mehrere Threads versuchen, auf dieselbe Warteschlange zuzugreifen. Die Synchronisierung ist auch erforderlich, wenn von mehreren Threads im gleichen Socket gesendet und empfangen wird, da die Sende-und Empfangs Vorgänge die Anforderungs Warteschlange des Sockets verwenden.

 

Wenn mehrere Threads versuchen, mit [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)auf denselben **Rio- \_ CQ** zuzugreifen, muss der Zugriff durch einen kritischen Abschnitt, eine schlanke Lese Schreibsperre oder einen ähnlichen gegenseitigen Ausschlussmechanismus koordiniert werden. Wenn die Vervollständigungs Warteschlangen nicht freigegeben werden, ist kein gegenseitiger Ausschluss erforderlich.

Wenn eine Vervollständigungs Warteschlange nicht mehr benötigt wird, kann Sie von einer Anwendung mithilfe der Funktion " [**rioclosecompletionqueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) " geschlossen werden.

Die **Rio \_** -"CQ typedef" ist in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist. Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.

## <a name="thread-safety"></a>Threadsicherheit

Wenn mehrere Threads versuchen, mit [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)auf denselben **Rio- \_ CQ** zuzugreifen, muss der Zugriff durch einen kritischen Abschnitt, eine schlanke Lese Schreibsperre oder einen ähnlichen gegenseitigen Ausschlussmechanismus koordiniert werden. Wenn die Vervollständigungs Warteschlangen nicht freigegeben werden, ist kein gegenseitiger Ausschluss erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mtausockdef. h (Include mtausock. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatus usex**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**Überlappende**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**Rio- \_ Benachrichtigungs \_ Abschluss**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**Rio \_ - \_ benachrichtigungschlusstyp \_**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**Rio \_ RQ**](riorqueue.md)
</dt> <dt>

[**Rioclosecompletionqueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**Riokreatecompletionqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**Riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**Rioabqueuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**Rionotifizieren**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**Wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**Wsaresetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**Wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 

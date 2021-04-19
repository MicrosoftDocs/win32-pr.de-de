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
# <a name="rio_cq"></a><span data-ttu-id="37b6e-103">Rio, \_ CQ</span><span class="sxs-lookup"><span data-stu-id="37b6e-103">RIO\_CQ</span></span>

<span data-ttu-id="37b6e-104">Die **Rio \_** -Klasse "CQ typedef" gibt einen Vervollständigungs Warteschlangen Deskriptor an, der für e/a-Abschluss Benachrichtigungen verwendet wird, indem Sende-und Empfangs Anforderungen mit den registrierten e/a-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="37b6e-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="37b6e-105">**Rio, \_ CQ**</span><span class="sxs-lookup"><span data-stu-id="37b6e-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-106">Ein Datentyp, der einen Vervollständigungs Warteschlangen Deskriptor angibt, der von Sende-und Empfangs Anforderungen für die e/a-Abschluss Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37b6e-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37b6e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37b6e-107">Remarks</span></span>

<span data-ttu-id="37b6e-108">Das **Rio \_** -Objekt "CQ" wird für e/a-Abschluss Benachrichtigungen von Sende-und Empfangs Netzwerk Anforderungen von den registrierten e/a-Erweiterungen von Winsock verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b6e-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="37b6e-109">Eine Anwendung kann die [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Funktion verwenden, um eine Benachrichtigung anzufordern, wenn die Abschluss Warteschlange von **Rio \_ CQ** nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="37b6e-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="37b6e-110">Eine Anwendung kann den Status auch jederzeit in einer **Rio- \_ CQ** -Vervollständigungs Warteschlange auf nicht blockierende Weise Abfragen, indem die [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37b6e-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="37b6e-111">Das **Rio \_** -Objekt "CQ" wird mit der Funktion " [**riokreatecompletionqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) " erstellt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="37b6e-112">Zum Zeitpunkt der Erstellung muss die Anwendung die Größe der Warteschlange angeben, die bestimmt, wie viele Vervollständigungs Einträge enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="37b6e-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="37b6e-113">Wenn eine Anwendung die [**riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) -Funktion aufruft, um ein [**Rio \_ RQ**](riorqueue.md) -Handle abzurufen, muss die Anwendung einen **Rio- \_ CQ** -Handle für Sende Vervollständigungen und einen **Rio- \_ CQ** -Handle für Empfangs Vervollständigungen angeben.</span><span class="sxs-lookup"><span data-stu-id="37b6e-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="37b6e-114">Diese Handles können identisch sein, wenn die gleiche Warteschlange für Sende-und Empfangs Vervollständigung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b6e-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="37b6e-115">Die **riokreaterequestqueue** -Funktion erfordert auch eine maximale Anzahl von ausstehenden Sende-und Empfangs Vorgängen, die mit der Kapazität der zugehörigen Vervollständigungs Warteschlange oder Warteschlangen abgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="37b6e-116">Wenn die Warteschlangen nicht über genügend Kapazität verfügen, tritt beim Aufrufen von " **riokreaterequestqueue** " ein Fehler mit [WSAENOBUFS](windows-sockets-error-codes-2.md)auf.</span><span class="sxs-lookup"><span data-stu-id="37b6e-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="37b6e-117">Das Benachrichtigungs Verhalten für eine Vervollständigungs Warteschlange wird festgelegt, wenn **Rio \_ CQ** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="37b6e-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="37b6e-118">Für eine Vervollständigungs Warteschlange, die ein Ereignis verwendet, wird das **typmitglied** der [**Rio- \_ Benachrichtigungs \_ Vervollständigungs**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) Struktur auf die **\_ Ereignis \_ Vervollständigung Rio** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="37b6e-119">Der **Event. EventHandle** -Member sollte das Handle für ein Ereignis enthalten, das von der [**wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) -Funktion oder der-Funktion für die Funktion " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) "</span><span class="sxs-lookup"><span data-stu-id="37b6e-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="37b6e-120">Um den [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Abschluss zu erhalten, sollte die Anwendung auf das angegebene Ereignis Handle mithilfe von [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) oder einer ähnlichen warte Routine warten.</span><span class="sxs-lookup"><span data-stu-id="37b6e-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="37b6e-121">Wenn die Anwendung das Zurücksetzen und wieder verwenden des Ereignisses plant, kann die Anwendung den mehr Aufwand verringern, indem das **Event. notifyreset** -Element auf einen Wert ungleich 0 (null) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="37b6e-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="37b6e-122">Dies bewirkt, dass das Ereignis automatisch von der **rionotify** -Funktion zurückgesetzt wird, wenn die Benachrichtigung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="37b6e-123">Dadurch wird verhindert, dass die [**wsaresetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) -Funktion aufgerufen werden muss, um das Ereignis zwischen Aufrufen der **rionotify** -Funktion zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="37b6e-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="37b6e-124">Für eine Vervollständigungs Warteschlange, die einen e/a-Abschlussport verwendet, wird das **typmitglied** der [**Rio- \_ Benachrichtigungs \_ Vervollständigungs**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) Struktur auf **Rio \_ IOCP \_ completion** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="37b6e-125">Der **IOCP. iocphandle** -Member sollte das Handle für einen e/a-Abschlussport enthalten, der von der Funktion " [**deeiocompletionport**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) " erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="37b6e-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="37b6e-126">Um den [**rionotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) -Abschluss zu erhalten, sollte die Anwendung die Funktion [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) oder [**getqueuedcompletionstatusex**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37b6e-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="37b6e-127">Die Anwendung sollte ein dediziertes [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Endes Objekt für die Vervollständigungs Warteschlange bereitstellen, und es kann auch das Element **IOCP. completionkey** verwenden, um **rionotify** -Anforderungen in der Vervollständigungs Warteschlange von anderen e/a-Vervollständigungen zu unterscheiden, einschließlich **rionotifiktionen** für andere Vervollständigungs Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="37b6e-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="37b6e-128">Der Zugriff auf die Vervollständigungs Warteschlangen (**Rio- \_ CQ** -Strukturen) und Anforderungs Warteschlangen ([**Rio \_ RQ**](riorqueue.md) -Strukturen) werden aus Gründen der Effizienz nicht durch Synchronisierungs primitive geschützt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="37b6e-129">Wenn Sie von mehreren Threads auf eine Vervollständigungs-oder Anforderungs Warteschlange zugreifen müssen, sollte der Zugriff durch einen kritischen Abschnitt, eine schlanke Schreibsperre für Lesevorgänge oder einen ähnlichen Mechanismus koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="37b6e-130">Diese Sperrung wird nicht für den Zugriff durch einen einzelnen Thread benötigt.</span><span class="sxs-lookup"><span data-stu-id="37b6e-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="37b6e-131">Verschiedene Threads können ohne Sperren auf separate Anforderungen/Vervollständigungs Warteschlangen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="37b6e-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="37b6e-132">Die Synchronisierung ist nur dann erforderlich, wenn mehrere Threads versuchen, auf dieselbe Warteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="37b6e-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="37b6e-133">Die Synchronisierung ist auch erforderlich, wenn von mehreren Threads im gleichen Socket gesendet und empfangen wird, da die Sende-und Empfangs Vorgänge die Anforderungs Warteschlange des Sockets verwenden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="37b6e-134">Wenn mehrere Threads versuchen, mit [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)auf denselben **Rio- \_ CQ** zuzugreifen, muss der Zugriff durch einen kritischen Abschnitt, eine schlanke Lese Schreibsperre oder einen ähnlichen gegenseitigen Ausschlussmechanismus koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="37b6e-135">Wenn die Vervollständigungs Warteschlangen nicht freigegeben werden, ist kein gegenseitiger Ausschluss erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37b6e-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="37b6e-136">Wenn eine Vervollständigungs Warteschlange nicht mehr benötigt wird, kann Sie von einer Anwendung mithilfe der Funktion " [**rioclosecompletionqueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) " geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="37b6e-137">Die **Rio \_** -"CQ typedef" ist in der Header Datei " *mgosockdef. h* " definiert, die automatisch in der Header Datei " *mgosock. h* " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="37b6e-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="37b6e-138">Die Header Datei " *mtausockdef. h* " sollte niemals direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="37b6e-139">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="37b6e-139">Thread Safety</span></span>

<span data-ttu-id="37b6e-140">Wenn mehrere Threads versuchen, mit [**riodequeuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)auf denselben **Rio- \_ CQ** zuzugreifen, muss der Zugriff durch einen kritischen Abschnitt, eine schlanke Lese Schreibsperre oder einen ähnlichen gegenseitigen Ausschlussmechanismus koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="37b6e-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="37b6e-141">Wenn die Vervollständigungs Warteschlangen nicht freigegeben werden, ist kein gegenseitiger Ausschluss erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37b6e-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b6e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37b6e-142">Requirements</span></span>



| <span data-ttu-id="37b6e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37b6e-143">Requirement</span></span> | <span data-ttu-id="37b6e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="37b6e-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b6e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37b6e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="37b6e-146">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37b6e-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="37b6e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37b6e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="37b6e-148">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37b6e-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="37b6e-149">Header</span><span class="sxs-lookup"><span data-stu-id="37b6e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b6e-150"><dt>Mtausockdef. h (Include mtausock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37b6e-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b6e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37b6e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b6e-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="37b6e-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="37b6e-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="37b6e-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="37b6e-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="37b6e-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="37b6e-155">**GetQueuedCompletionStatus usex**</span><span class="sxs-lookup"><span data-stu-id="37b6e-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="37b6e-156">**Überlappende**</span><span class="sxs-lookup"><span data-stu-id="37b6e-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="37b6e-157">**Rio- \_ Benachrichtigungs \_ Abschluss**</span><span class="sxs-lookup"><span data-stu-id="37b6e-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="37b6e-158">**Rio \_ - \_ benachrichtigungschlusstyp \_**</span><span class="sxs-lookup"><span data-stu-id="37b6e-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="37b6e-159">**Rio \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="37b6e-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="37b6e-160">[**Rioclosecompletionqueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37b6e-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37b6e-161">**Riokreatecompletionqueue**</span><span class="sxs-lookup"><span data-stu-id="37b6e-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="37b6e-162">**Riokreaterequestqueue**</span><span class="sxs-lookup"><span data-stu-id="37b6e-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="37b6e-163">**Rioabqueuecompletion**</span><span class="sxs-lookup"><span data-stu-id="37b6e-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="37b6e-164">**Rionotifizieren**</span><span class="sxs-lookup"><span data-stu-id="37b6e-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="37b6e-165">**Wsacreateevent**</span><span class="sxs-lookup"><span data-stu-id="37b6e-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="37b6e-166">**Wsaresetevent**</span><span class="sxs-lookup"><span data-stu-id="37b6e-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="37b6e-167">**Wsawaitformultipleevents**</span><span class="sxs-lookup"><span data-stu-id="37b6e-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 

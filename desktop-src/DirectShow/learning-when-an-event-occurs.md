---
description: Lernen, wenn ein Ereignis eintritt
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Lernen, wenn ein Ereignis eintritt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522067"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="25a57-103">Lernen, wenn ein Ereignis eintritt</span><span class="sxs-lookup"><span data-stu-id="25a57-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="25a57-104">Um DirectShow-Ereignisse zu verarbeiten, benötigt eine Anwendung eine Methode, um herauszufinden, wann Ereignisse in der Warteschlange warten.</span><span class="sxs-lookup"><span data-stu-id="25a57-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="25a57-105">Der Filter Graph-Manager bietet zwei Möglichkeiten, dies zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="25a57-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="25a57-106">**Fenster Benachrichtigung:** Der Filter Graph-Manager sendet eine benutzerdefinierte Windows-Meldung an ein Anwendungsfenster, wenn ein neues Ereignis vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="25a57-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="25a57-107">**Ereignis Signalisierung:** Der Filter Graph-Manager signalisiert einem Windows-Ereignis, wenn sich DirectShow-Ereignisse in der Warteschlange befinden, und setzt das Ereignis zurück, wenn die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="25a57-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="25a57-108">Eine Anwendung kann beide Techniken verwenden.</span><span class="sxs-lookup"><span data-stu-id="25a57-108">An application can use either technique.</span></span> <span data-ttu-id="25a57-109">Die Fenster Benachrichtigung ist in der Regel einfacher.</span><span class="sxs-lookup"><span data-stu-id="25a57-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="25a57-110">**Fenster Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="25a57-110">**Window Notification**</span></span>

<span data-ttu-id="25a57-111">Um eine Fenster Benachrichtigung einzurichten, müssen Sie die [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) -Methode aufrufen und eine private Meldung angeben.</span><span class="sxs-lookup"><span data-stu-id="25a57-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="25a57-112">Anwendungen können Nachrichtennummern im Bereich von WM- \_ app bis 0xbfff als private Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="25a57-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="25a57-113">Jedes Mal, wenn der Filter Diagramm-Manager eine neue Ereignis Benachrichtigung in der Warteschlange eingibt, wird diese Nachricht an das angegebene Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="25a57-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="25a57-114">Die Anwendung antwortet innerhalb der Nachrichten Schleife des Fensters auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="25a57-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="25a57-115">Im folgenden Codebeispiel wird gezeigt, wie das Benachrichtigungsfenster festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="25a57-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="25a57-116">Die Meldung ist eine normale Windows-Meldung und wird separat von der DirectShow-Ereignis Benachrichtigungs Warteschlange gepostet.</span><span class="sxs-lookup"><span data-stu-id="25a57-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="25a57-117">Der Vorteil dieses Ansatzes besteht darin, dass die meisten Anwendungen bereits eine Nachrichten Schleife implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="25a57-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="25a57-118">Daher können Sie die DirectShow-Ereignis Behandlung ohne viel zusätzliche Arbeit integrieren.</span><span class="sxs-lookup"><span data-stu-id="25a57-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="25a57-119">Im folgenden Codebeispiel wird gezeigt, wie auf die Benachrichtigungs Meldung reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="25a57-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="25a57-120">Ein umfassendes Beispiel finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="25a57-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="25a57-121">Da Ereignis Benachrichtigung und Nachrichten Schleife asynchron sind, kann die Warteschlange mehr als ein Ereignis enthalten, wenn die Anwendung auf die Nachricht antwortet.</span><span class="sxs-lookup"><span data-stu-id="25a57-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="25a57-122">Außerdem können Ereignisse manchmal aus der Warteschlange gelöscht werden, wenn Sie ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="25a57-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="25a57-123">Daher wird in Ihrem Ereignis Behandlungs Code [**iammediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) aufgerufen, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="25a57-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="25a57-124">Bevor Sie den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger freigeben, brechen Sie die Ereignis Benachrichtigung ab, indem Sie [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **null** -Zeiger aufrufen.</span><span class="sxs-lookup"><span data-stu-id="25a57-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="25a57-125">Überprüfen Sie im Ereignis Verarbeitungs Code, ob der **imediaeventex** -Zeiger gültig ist, bevor Sie [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="25a57-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="25a57-126">Diese Schritte verhindern einen möglichen Fehler, bei dem die Anwendung die Ereignis Benachrichtigung empfängt, nachdem Sie den **imediaeventex** -Zeiger freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="25a57-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="25a57-127">**Ereignissignal**</span><span class="sxs-lookup"><span data-stu-id="25a57-127">**Event Signaling**</span></span>

<span data-ttu-id="25a57-128">Der Filter Graph-Manager speichert ein manuelles Zurücksetzungs Ereignis, das den Status der Ereignis Warteschlange widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="25a57-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="25a57-129">Wenn die Warteschlange ausstehende Ereignis Benachrichtigungen enthält, signalisiert der Filter Graph-Manager das Ereignis für manuelles Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="25a57-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="25a57-130">Wenn die Warteschlange leer ist, wird das Ereignis durch einen Aufrufe der [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="25a57-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="25a57-131">Eine Anwendung kann dieses Ereignis verwenden, um den Status der Warteschlange zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="25a57-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="25a57-132">Die Terminologie kann hier verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="25a57-132">The terminology can be confusing here.</span></span> <span data-ttu-id="25a57-133">Das Ereignis für manuelles Zurücksetzen ist der Typ des Ereignisses, das von der Windows-Funktion " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " erstellt wurde. Dies hat nichts mit den Ereignissen zu tun, die von DirectShow definiert werden.</span><span class="sxs-lookup"><span data-stu-id="25a57-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="25a57-134">Ruft die [**imediaevent:: geteventhandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) -Methode auf, um ein Handle für das manuelle Zurücksetzungs Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25a57-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="25a57-135">Warten Sie, bis das Ereignis signalisiert wird, indem Sie eine Funktion wie [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="25a57-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="25a57-136">Nachdem das Ereignis signalisiert wurde, wenden Sie [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) an, um das DirectShow-Ereignis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25a57-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="25a57-137">Das folgende Codebeispiel veranschaulicht diese Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="25a57-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="25a57-138">Er ruft das Ereignis Handle ab und wartet dann in Intervallen von 100 Millisekunden, bis das Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="25a57-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="25a57-139">Wenn das Ereignis signalisiert wird, ruft es **GetEvent** auf und druckt den Ereignis Code und die Ereignis Parameter im Konsolenfenster.</span><span class="sxs-lookup"><span data-stu-id="25a57-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="25a57-140">Die Schleife wird beendet, wenn das [**EC \_ Complete**](ec-complete.md) -Ereignis auftritt, das angibt, dass die Wiedergabe abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="25a57-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="25a57-141">Da das Filter Diagramm das Ereignis nach Bedarf automatisch festlegt oder zurücksetzt, sollte Ihre Anwendung dies nicht tun.</span><span class="sxs-lookup"><span data-stu-id="25a57-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="25a57-142">Beim Freigeben des Filter Diagramms schließt das Filter Diagramm auch das Ereignis handle. verwenden Sie daher nach diesem Punkt nicht das Ereignis handle.</span><span class="sxs-lookup"><span data-stu-id="25a57-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 

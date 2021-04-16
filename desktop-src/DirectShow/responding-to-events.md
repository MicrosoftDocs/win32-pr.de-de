---
description: In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filter Diagramm auftreten.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Reagieren auf Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521400"
---
# <a name="responding-to-events"></a><span data-ttu-id="7303f-103">Reagieren auf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7303f-103">Responding to Events</span></span>

<span data-ttu-id="7303f-104">In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filter Diagramm auftreten.</span><span class="sxs-lookup"><span data-stu-id="7303f-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="7303f-105">Funktionsweise der Ereignis Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7303f-105">How Event Notification Works</span></span>

<span data-ttu-id="7303f-106">Während eine DirectShow-Anwendung ausgeführt wird, können Ereignisse innerhalb des Filter Diagramms auftreten.</span><span class="sxs-lookup"><span data-stu-id="7303f-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="7303f-107">Ein Filter kann z. b. auf einen Streamingfehler stoßen.</span><span class="sxs-lookup"><span data-stu-id="7303f-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="7303f-108">Filter benachrichtigen den Filter Graph-Manager durch das Senden von Ereignissen, die aus einem Ereignis Code und zwei Ereignis Parametern bestehen.</span><span class="sxs-lookup"><span data-stu-id="7303f-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="7303f-109">Der Ereignis Code gibt den Typ des Ereignisses an, und die Ereignis Parameter stellen zusätzliche Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="7303f-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="7303f-110">Die Bedeutung der Parameter hängt vom Ereignis Code ab.</span><span class="sxs-lookup"><span data-stu-id="7303f-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="7303f-111">Eine umfassende Liste der Ereignis Codes finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7303f-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="7303f-112">Einige Ereignisse werden vom Filter Graph-Manager automatisch verarbeitet, ohne dass die Anwendung benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="7303f-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="7303f-113">Andere Ereignisse werden in eine Warteschlange für die Anwendung eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7303f-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="7303f-114">Abhängig von der Anwendung gibt es verschiedene Ereignisse, die Sie möglicherweise behandeln müssen.</span><span class="sxs-lookup"><span data-stu-id="7303f-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="7303f-115">Dieser Artikel konzentriert sich auf drei häufige Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="7303f-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="7303f-116">Das Ereignis [**EC \_ Complete**](ec-complete.md) gibt an, dass die Wiedergabe normal abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7303f-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="7303f-117">Das Ereignis " [**EC \_ userabort**](ec-userabort.md) " gibt an, dass der Benutzer die Wiedergabe unterbrochen hat.</span><span class="sxs-lookup"><span data-stu-id="7303f-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="7303f-118">Videorenderer Senden dieses Ereignis, wenn der Benutzer das Videofenster schließt.</span><span class="sxs-lookup"><span data-stu-id="7303f-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="7303f-119">Das [**EC \_ errorabort**](ec-errorabort.md) -Ereignis gibt an, dass die Wiedergabe aufgrund eines Fehlers angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="7303f-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="7303f-120">Verwenden der Ereignis Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7303f-120">Using Event Notification</span></span>

<span data-ttu-id="7303f-121">Eine Anwendung kann den Filter Graph-Manager anweisen, eine Windows-Meldung an ein bestimmtes Fenster zu senden, wenn ein neues Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="7303f-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="7303f-122">Dadurch kann die Anwendung innerhalb der Nachrichten Schleife des Fensters Antworten.</span><span class="sxs-lookup"><span data-stu-id="7303f-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="7303f-123">Definieren Sie zuerst die Nachricht, die an das Anwendungsfenster gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7303f-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="7303f-124">Anwendungen können Nachrichtennummern im Bereich von WM- \_ app bis 0xbfff als private Nachrichten verwenden:</span><span class="sxs-lookup"><span data-stu-id="7303f-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="7303f-125">Fragen Sie als nächstes den Filter Graph-Manager nach der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle ab, und nennen Sie die [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) -Methode:</span><span class="sxs-lookup"><span data-stu-id="7303f-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="7303f-126">Diese Methode legt das angegebene Fenster (g \_ HWND) als Empfänger der Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="7303f-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="7303f-127">Rufen Sie die-Methode auf, nachdem Sie das Filter Diagramm erstellt haben, aber bevor Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="7303f-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="7303f-128">WM \_ graphnotify ist eine gewöhnliche Windows-Meldung.</span><span class="sxs-lookup"><span data-stu-id="7303f-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="7303f-129">Jedes Mal, wenn der Filter Graph-Manager ein neues Ereignis in der Ereignis Warteschlange einfügt, sendet er eine WM- \_ graphnotify-Meldung an das angegebene Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="7303f-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="7303f-130">Der *LPARAM* -Parameter der Nachricht ist gleich dem dritten Parameter in [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="7303f-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="7303f-131">Dieser Parameter ermöglicht es Ihnen, Instanzdaten mit der Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="7303f-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="7303f-132">Der *wParam* -Parameter der Fenster Meldung ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7303f-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="7303f-133">Fügen Sie in der **WindowProc** -Funktion Ihrer Anwendung eine Case-Anweisung für die WM- \_ graphnotify-Nachricht hinzu:</span><span class="sxs-lookup"><span data-stu-id="7303f-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="7303f-134">Rufen Sie in der Ereignishandlerfunktion die [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode auf, um Ereignisse aus der Warteschlange abzurufen:</span><span class="sxs-lookup"><span data-stu-id="7303f-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="7303f-135">Die [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode ruft den Ereignis Code und die beiden Ereignis Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="7303f-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="7303f-136">Der vierte **GetEvent** -Parameter gibt die Zeitdauer an, die auf ein Ereignis gewartet wird (in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="7303f-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="7303f-137">Da die Anwendung diese Methode als Reaktion auf eine WM- \_ graphnotify-Nachricht aufruft, wird das Ereignis bereits in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="7303f-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="7303f-138">Daher legen wir den Timeout Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="7303f-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="7303f-139">Die Ereignis Benachrichtigung und die Nachrichten Schleife sind asynchron, sodass die Warteschlange möglicherweise mehr als ein Ereignis enthält, wenn Ihre Anwendung auf die Nachricht antwortet.</span><span class="sxs-lookup"><span data-stu-id="7303f-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="7303f-140">Der Filter Graph-Manager kann auch bestimmte Ereignisse aus der Warteschlange entfernen, wenn Sie ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="7303f-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="7303f-141">Daher sollten Sie [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) so lange aufzurufen, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="7303f-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="7303f-142">In diesem Beispiel reagiert die Anwendung auf [**EC \_ Complete**](ec-complete.md), [**EC \_ userabort**](ec-userabort.md)und [**EC \_ errorabort**](ec-errorabort.md) , indem Sie die Anwendungs definierte Bereinigungs Funktion aufruft, die bewirkt, dass die Anwendung ordnungsgemäß beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7303f-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="7303f-143">Im Beispiel werden die beiden Ereignis Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7303f-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="7303f-144">Nachdem Sie ein Ereignis abgerufen haben, rufen Sie [**imediaevent:: freeeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) für alle freien Ressourcen auf, die den Ereignis Parametern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7303f-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="7303f-145">Beachten Sie, dass ein [**EC \_ Complete**](ec-complete.md) -Ereignis nicht dazu führt, dass das Filter Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7303f-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="7303f-146">Die Anwendung kann das Diagramm entweder anhalten oder anhalten.</span><span class="sxs-lookup"><span data-stu-id="7303f-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="7303f-147">Wenn Sie das Diagramm abbrechen, gibt Filter alle Ressourcen frei, die Sie halten.</span><span class="sxs-lookup"><span data-stu-id="7303f-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="7303f-148">Wenn Sie das Diagramm anhalten, enthalten Filter weiterhin Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7303f-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="7303f-149">Wenn ein Videorenderer anhält, wird auch ein statisches Bild des letzten Frames angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7303f-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="7303f-150">Bevor Sie den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger freigeben, brechen Sie die Ereignis Benachrichtigung ab, indem Sie [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **null** -Fenster Handle aufrufen:</span><span class="sxs-lookup"><span data-stu-id="7303f-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="7303f-151">\_Überprüfen Sie im "WM graphnotify"-Nachrichten Handler den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger, bevor Sie " [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)" aufrufen:</span><span class="sxs-lookup"><span data-stu-id="7303f-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="7303f-152">Dadurch wird ein möglicher Fehler verhindert, der auftreten kann, wenn die Anwendung die Ereignis Benachrichtigung empfängt, nachdem der Zeiger losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="7303f-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7303f-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7303f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7303f-154">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="7303f-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="7303f-155">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7303f-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




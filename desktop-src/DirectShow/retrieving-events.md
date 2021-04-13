---
description: Abrufen von Ereignissen
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Abrufen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392335"
---
# <a name="retrieving-events"></a><span data-ttu-id="d222d-103">Abrufen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d222d-103">Retrieving Events</span></span>

<span data-ttu-id="d222d-104">Der Filter Graph-Manager macht drei Schnittstellen verfügbar, die die Ereignis Benachrichtigung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d222d-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="d222d-105">[**Imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) enthält die-Methode für Filter zum Veröffentlichen von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="d222d-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="d222d-106">[**Imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) enthält Methoden, mit denen Anwendungen Ereignisse abrufen können.</span><span class="sxs-lookup"><span data-stu-id="d222d-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="d222d-107">[**Imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) erbt von und erweitert die [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d222d-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="d222d-108">Filtert nach Ereignis Benachrichtigungen, indem die [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) -Methode für den Filter Graph-Manager aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d222d-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="d222d-109">Eine Ereignis Benachrichtigung besteht aus einem Ereignis Code, der den Ereignistyp definiert, und zwei Parametern, die zusätzliche Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d222d-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="d222d-110">Abhängig vom Ereignis Code können die Parameter Zeiger, Rückgabecodes, Verweis Zeiten oder andere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d222d-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="d222d-111">Eine umfassende Liste von Ereignis Codes und Parametern finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d222d-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="d222d-112">Um ein Ereignis aus der Warteschlange abzurufen, ruft die Anwendung die [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode für den Filter Graph-Manager auf.</span><span class="sxs-lookup"><span data-stu-id="d222d-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="d222d-113">Diese Methode wird blockiert, bis ein Ereignis zurückgegeben werden kann oder bis eine angegebene Zeit verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="d222d-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="d222d-114">Wenn ein Ereignis in der Warteschlange vorhanden ist, gibt die Methode mit dem Ereignis Code und den beiden Ereignis Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="d222d-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="d222d-115">Nach dem Aufruf von **GetEvent** sollte eine Anwendung immer die Methode [**imediaevent:: freeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) aufrufen, um alle Ressourcen freizugeben, die den Ereignis Parametern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d222d-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="d222d-116">Ein Parameter kann z. b. ein **BSTR** -Wert sein, der vom Filter Diagramm zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d222d-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="d222d-117">Im folgenden Codebeispiel wird erläutert, wie Ereignisse aus der Warteschlange abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d222d-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="d222d-118">Um die Standardbehandlung des Filter Graph-Managers für ein Ereignis zu überschreiben, rufen Sie die [**imediaevent:: canceldefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) -Methode mit dem Ereignis Code als Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="d222d-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="d222d-119">Sie können die Standardbehandlung wiederherstellen, indem Sie die [**imediaevent:: restoredefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d222d-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="d222d-120">Wenn das Filter Diagramm keine Standardbehandlung für den angegebenen Ereignis Code ausführt, hat das Aufrufen dieser Methoden keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="d222d-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d222d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d222d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d222d-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d222d-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




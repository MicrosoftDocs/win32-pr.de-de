---
description: Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für den Fall, dass Component Object Model (com) und die Automatisierung verwendet werden.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Überlegungen zu com-und Automatisierungs Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344648"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="28a41-103">Überlegungen zu com-und Automatisierungs Threading</span><span class="sxs-lookup"><span data-stu-id="28a41-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="28a41-104">Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für den Fall, dass Component Object Model (com) und die Automatisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28a41-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="28a41-105">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="28a41-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="28a41-106">STA-und MTA-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28a41-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="28a41-107">InkCollector und InkOverlay</span><span class="sxs-lookup"><span data-stu-id="28a41-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="28a41-108">Ereignis senken</span><span class="sxs-lookup"><span data-stu-id="28a41-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="28a41-109">Ausnahmen innerhalb von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="28a41-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="28a41-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28a41-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="28a41-111">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="28a41-111">Thread Safety</span></span>

<span data-ttu-id="28a41-112">Mit Ausnahme der [InkPicture](inkpicture-control.md) -und [InkEdit](inkedit-control.md) -Steuerelemente sind Tablet PC-Objekte Thread sicher und als beides gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="28a41-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="28a41-113">Wenn Sie als beides gekennzeichnet sind, können Sie entweder in einem Single Thread-Apartment (STA) oder einem Multithread-Apartment (MTA) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="28a41-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="28a41-114">Windows Forms verwenden das STA-Modell, da Windows Forms auf nativen Win32-Fenstern basiert, die von Natur aus Apartment Thread sind.</span><span class="sxs-lookup"><span data-stu-id="28a41-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="28a41-115">STA-und MTA-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28a41-115">STA and MTA Applications</span></span>

<span data-ttu-id="28a41-116">Wenn Ihre Anwendung in einem MTA ausgeführt wird oder den Free Threaded Mars Haller (FTM) verwendet, müssen Sie Thread sicheren Code schreiben. auf diese Weise können Sie jedoch bestimmte Leistungsprobleme bei der Ereignis Behandlung verbessern.</span><span class="sxs-lookup"><span data-stu-id="28a41-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="28a41-117">InkCollector und InkOverlay</span><span class="sxs-lookup"><span data-stu-id="28a41-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="28a41-118">Ihre Anwendung sollte nicht ihren endgültigen Verweis auf das [**InkCollector**](inkcollector-class.md) -Objekt oder das [**InkOverlay**](inkoverlay-class.md) -Objekt freigeben und somit das Objekt direkt aus dem frei Hand Thread zerstören.</span><span class="sxs-lookup"><span data-stu-id="28a41-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="28a41-119">Stattdessen sollte die Anwendung das **InkCollector** -Objekt oder das **InkOverlay** -Objekt aus einem Anwendungs Thread freigeben.</span><span class="sxs-lookup"><span data-stu-id="28a41-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="28a41-120">**Vorsicht:** Eine Anwendung, die als MTA gekennzeichnet ist oder das FTM verwendet, das direkte Aufrufe aus dem frei Hand Thread in das Apartment der Anwendung zulässt, kann den endgültigen Verweis auf das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt direkt aus dem frei Hand Thread freigeben. Dies verursacht jedoch einen nicht BEHEB baren Anwendungsfehler.</span><span class="sxs-lookup"><span data-stu-id="28a41-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="28a41-121">Ereignis senken</span><span class="sxs-lookup"><span data-stu-id="28a41-121">Event Sinks</span></span>

<span data-ttu-id="28a41-122">Wenn Ihre Anwendung nicht FTM und ein Objekt verwendet und die zugehörige Ereignis Senke in verschiedenen Apartments erstellt wird, wird das Ereignis auf dem Thread ausgeführt, der die Ereignis Senke bedient.</span><span class="sxs-lookup"><span data-stu-id="28a41-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="28a41-123">Ausnahmen innerhalb von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="28a41-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="28a41-124">Aus Tablet PC-Ereignis Handlern ausgelöste Ausnahmen werden verbraucht und sind für den Rest oder Ihre Anwendung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="28a41-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="28a41-125">Ebenso werden HRESULT-Werte nicht von Tablet PC-Ereignis Handlern weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="28a41-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="28a41-126">Wenn eine Anwendung, die die com-Ebene verwendet, eine Ausnahme auslöst, wird der Hintergrund Thread beendet, und die Ausnahme geht verloren.</span><span class="sxs-lookup"><span data-stu-id="28a41-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="28a41-127">Es werden keine weiteren Ereignishandler aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="28a41-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28a41-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28a41-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a41-129">C++ Event senken-Beispiel</span><span class="sxs-lookup"><span data-stu-id="28a41-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="28a41-130">Allgemeine Überlegungen zum Threading</span><span class="sxs-lookup"><span data-stu-id="28a41-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="28a41-131">Überlegungen zum Threading verwalteter Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="28a41-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 




---
description: Informationen zum Filter Graph-Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informationen zum Filter Graph-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522240"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="6d8fd-103">Informationen zum Filter Graph-Manager</span><span class="sxs-lookup"><span data-stu-id="6d8fd-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="6d8fd-104">Der [Filter Graph-Manager](filter-graph-manager.md) ist ein COM-Objekt, mit dem die Filter in einem Filter Diagramm gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="6d8fd-105">Sie führt viele Funktionen aus, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="6d8fd-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="6d8fd-106">Koordinieren von Zustandsänderungen zwischen den Filtern.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="6d8fd-107">Einrichten einer verweisuhr.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="6d8fd-108">Ereignisse werden zurück an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="6d8fd-109">Bereitstellen von Methoden für Anwendungen zum Erstellen des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="6d8fd-110">Jede dieser Funktionen wird hier kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="6d8fd-111">Details finden Sie an anderer Stelle in der Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="6d8fd-112">**Statusänderungen**.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-112">**State changes**.</span></span> <span data-ttu-id="6d8fd-113">Zustandsänderungen innerhalb von Filtern müssen in einer bestimmten Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="6d8fd-114">Daher gibt die Anwendung keine Status Änderungs Befehle direkt an die Filter aus.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="6d8fd-115">Stattdessen wird dem Filter Graph-Manager ein einziger Befehl erteilt, der den Befehl an jeden Filter verteilt.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="6d8fd-116">Die Suche funktioniert auf ähnliche Weise: die Anwendung gibt dem Filter Graph-Manager einen Suchbefehl, der Sie an die Filter verteilt.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="6d8fd-117">Die **Referenzuhr**.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-117">**Reference clock**.</span></span> <span data-ttu-id="6d8fd-118">Alle Filter im Diagramm verwenden dieselbe Uhr, die als *Referenzuhr* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="6d8fd-119">Die Referenzuhr stellt sicher, dass alle Streams synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="6d8fd-120">Die Uhrzeit, zu der ein Video Frame oder ein Audiobeispiel gerendert werden soll, wird als *Präsentationszeit* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="6d8fd-121">Die Präsentationszeit wird relativ zur Referenzuhr gemessen.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="6d8fd-122">Der Filter Graph-Manager wählt eine Referenzuhr aus, normalerweise entweder die Uhr auf der Soundkarte oder die Systemuhr.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="6d8fd-123">**Graph-Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-123">**Graph events**.</span></span> <span data-ttu-id="6d8fd-124">Der Filter Graph-Manager verwendet eine Ereignis Warteschlange, um die Anwendung über Ereignisse zu informieren, die im Filter Diagramm auftreten.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="6d8fd-125">Dieser Mechanismus ähnelt einer Windows-Nachrichten Schleife.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="6d8fd-126">**Graph-erbauungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-126">**Graph-building methods**.</span></span> <span data-ttu-id="6d8fd-127">Der Filter Graph-Manager bietet Methoden für die Anwendung zum Hinzufügen von Filtern zum Diagramm, zum Verbinden von Filtern mit anderen Filtern und zum Trennen von Filtern.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="6d8fd-128">Eine Funktion, die der Filter Graph-Manager nicht verarbeitet, ist das Verschieben von Daten von einem Filter zum nächsten.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="6d8fd-129">Dies erfolgt durch die Filter selbst über die PIN-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="6d8fd-130">Die Verarbeitung erfolgt immer in einem separaten Thread.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="6d8fd-131">Filter sind immer frei, wenn Sie sich im gleichen Prozess wie der Filter Graph-Manager befinden und aus Prozess internen Servern geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="6d8fd-132">Daher werden Methodenaufrufe nicht zwischen Filtern oder zwischen Filtern und dem Filter Diagramm-Manager gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="6d8fd-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6d8fd-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d8fd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d8fd-134">Datenfluss im Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="6d8fd-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="6d8fd-135">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6d8fd-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6d8fd-136">Festlegen der diagrammuhr</span><span class="sxs-lookup"><span data-stu-id="6d8fd-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="6d8fd-137">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6d8fd-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 




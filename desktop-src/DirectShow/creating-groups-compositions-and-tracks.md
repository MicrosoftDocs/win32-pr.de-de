---
description: Erstellen von Gruppenkompositionen und-Spuren
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Erstellen von Gruppenkompositionen und-Spuren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860506"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="f5ce5-103">Erstellen von Gruppenkompositionen und-Spuren</span><span class="sxs-lookup"><span data-stu-id="f5ce5-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="f5ce5-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="f5ce5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f5ce5-105">Gruppen, Kompositionen und Spuren sind die zwischen Ebenen zwischen der Zeitachse und den Quell Clips.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="f5ce5-106">Sie unterscheiden sich durch den Objekttyp, den Sie enthalten können.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="f5ce5-107">Spuren enthalten Quell Objekte.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="f5ce5-108">Die Komposition enthält Spuren und andere Kompositionen, aber keine Quell Objekte.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="f5ce5-109">Gruppen sind Kompositionen der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-109">Groups are top-level compositions.</span></span> <span data-ttu-id="f5ce5-110">Gruppen enthalten Kompositionen und Spuren, aber die Komposition darf keine Gruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="f5ce5-111">Ein *virtueller Titel* ist ein beliebiges Objekt, das sich in einer Komposition oder einer Gruppe befinden kann.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="f5ce5-112">Dies schließt Titel und Kompositionen ein.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="f5ce5-113">Diese Objekte machen die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f5ce5-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="f5ce5-114">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f5ce5-114">Interface</span></span>                                                  | <span data-ttu-id="f5ce5-115">Verfügbar von</span><span class="sxs-lookup"><span data-stu-id="f5ce5-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="f5ce5-116">**Iamtimelinetrack**</span><span class="sxs-lookup"><span data-stu-id="f5ce5-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="f5ce5-117">Spuren</span><span class="sxs-lookup"><span data-stu-id="f5ce5-117">Tracks</span></span>               |
| [<span data-ttu-id="f5ce5-118">**Iamtimelinevirtualtrack**</span><span class="sxs-lookup"><span data-stu-id="f5ce5-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="f5ce5-119">Spuren, Kompositionen</span><span class="sxs-lookup"><span data-stu-id="f5ce5-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="f5ce5-120">**Iamtimelinecomp**</span><span class="sxs-lookup"><span data-stu-id="f5ce5-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="f5ce5-121">Komposition, Gruppen</span><span class="sxs-lookup"><span data-stu-id="f5ce5-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="f5ce5-122">**Iamtimelinegroup**</span><span class="sxs-lookup"><span data-stu-id="f5ce5-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="f5ce5-123">Gruppen</span><span class="sxs-lookup"><span data-stu-id="f5ce5-123">Groups</span></span>               |



 

<span data-ttu-id="f5ce5-124">Diese Schnittstellen enthalten die Methoden zum Hinzufügen von Objekten zur Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="f5ce5-125">[**Iamtimeline:: addgroup**](iamtimeline-addgroup.md): Fügt eine Gruppe in die Zeitachse ein.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="f5ce5-126">[**Iamtimelinecomp:: vtrackinsbefore**](iamtimelinecomp-vtrackinsbefore.md): Fügt einen virtuellen Track in eine Komposition oder eine Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="f5ce5-127">[**Iamtimelinetrack:: srcadd**](iamtimelinetrack-srcadd.md): Fügt eine Quelle in eine Spur ein.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="f5ce5-128">Der folgende Code fügt z. b. einen neuen Track in eine Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="f5ce5-129">Wie in der obigen Tabelle gezeigt, wird eine Gruppe als eine Art Komposition betrachtet, und eine Spur ist eine Art virtueller Nachverfolgung. Wenn Sie also den Track in die Gruppe einfügen möchten, müssen Sie die Gruppe nach ihrer **iamtimelinecomp** -Schnittstelle Abfragen und die **iamtimelinecomp:: vtrackinsbefore** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="f5ce5-130">Der zweite Parameter für **vtrackinsbefore** gibt die Priorität des virtuellen Titels an. Prioritätsstufen beginnen bei Null.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="f5ce5-131">Wenn Sie den Wert – 1 angeben, wird die virtuelle Spur am Ende der Prioritäts Liste eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="f5ce5-132">Wenn Sie einen Wert angeben, bei dem bereits eine virtuelle Spur vorhanden ist, wird von diesem Punkt aus die Liste um eine Prioritäts Ebene nach unten verschoben.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="f5ce5-133">Fügen Sie eine virtuelle Spur nicht mit einer Priorität ein, die größer als die Anzahl der virtuellen Spuren ist, da dies zu undefiniertem Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="f5ce5-134">Um ein Objekt dauerhaft aus der Zeitachse zu löschen, nennen Sie [**iamtimelineobj:: RemoveAll**](iamtimelineobj-removeall.md) für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="f5ce5-135">Diese Methode entfernt das-Objekt und alle zugehörigen untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-135">This method removes the object and all its children.</span></span> <span data-ttu-id="f5ce5-136">Um ein Objekt zu entfernen, um es an anderer Stelle in der Zeitachse wiederherzustellen, müssen Sie stattdessen [**iamtimelineobj:: Remove**](iamtimelineobj-remove.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="f5ce5-137">Anders als **RemoveAll** löscht diese Methode nicht die untergeordneten Elemente des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f5ce5-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="f5ce5-138">Um alles aus der Zeitachse zu entfernen, nennen Sie [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="f5ce5-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5ce5-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5ce5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5ce5-140">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="f5ce5-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




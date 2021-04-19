---
description: Timeline-Objekte
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Timeline-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350178"
---
# <a name="timeline-objects"></a><span data-ttu-id="4186a-103">Timeline-Objekte</span><span class="sxs-lookup"><span data-stu-id="4186a-103">Timeline Objects</span></span>

<span data-ttu-id="4186a-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="4186a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4186a-105">Jeder Objekttyp in der Zeitachse – Quelle, Track, Effect usw. – ist ein eindeutiges com-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4186a-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="4186a-106">Eine Anwendung erstellt Sie jedoch nicht mithilfe der **cokreatanstance** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4186a-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="4186a-107">Stattdessen wird die [**iamtimeline:: erkreateemptynode**](iamtimeline-createemptynode.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4186a-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="4186a-108">Diese Methode erstellt ein Objekt des angeforderten Typs, initialisiert es und gibt einen Zeiger auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4186a-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="4186a-109">Weitere Informationen finden Sie unter [Erstellen einer Zeitachse](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="4186a-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="4186a-110">Jedes Zeitachsen Objekt macht die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4186a-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="4186a-111">Außerdem unterstützen die verschiedenen Objekttypen ihre eigenen spezialisierten Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="4186a-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="4186a-112">Quelle: [ **iamtimelinesrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="4186a-113">Nachverfolgung: [ **iamtimelinetrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="4186a-114">Komposition: [ **iamtimelinecomp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="4186a-115">Gruppe: [**iamtimelinecomp**](iamtimelinecomp.md), [**iamtimelinegroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="4186a-116">Auswirkung: [ **iamtimelineeffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="4186a-117">Übergang: [ **iamtimelinetrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="4186a-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="4186a-118">Beachten Sie, dass Gruppen eine Art der Komposition sind, sodass Sie [**iamtimelinecomp**](iamtimelinecomp.md)und ihre eigene [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4186a-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="4186a-119">Zusätzlich zu den zuvor aufgelisteten Schnittstellen stellen Zeitachsen Objekte andere sekundäre Schnittstellen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4186a-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="4186a-120">Diese Schnittstellen bestimmen die Beziehungen zwischen den Objekttypen.</span><span class="sxs-lookup"><span data-stu-id="4186a-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="4186a-121">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4186a-121">Interface</span></span>                                                  | <span data-ttu-id="4186a-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4186a-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="4186a-123">Verfügbar von</span><span class="sxs-lookup"><span data-stu-id="4186a-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="4186a-124">**Iamtimelinevirtualtrack**</span><span class="sxs-lookup"><span data-stu-id="4186a-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="4186a-125">Das-Objekt ist ein virtueller Titel. Virtuelle Spuren können sich innerhalb von Kompositionen befinden und andere Zeitachsen Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="4186a-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="4186a-126">Komposition, Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="4186a-126">Composition, Track</span></span>                |
| [<span data-ttu-id="4186a-127">**Iamtimelineeffectable**</span><span class="sxs-lookup"><span data-stu-id="4186a-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="4186a-128">Das-Objekt kann Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="4186a-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="4186a-129">Komposition, Nachverfolgung, Quelle</span><span class="sxs-lookup"><span data-stu-id="4186a-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="4186a-130">**Iamtimelinetransable**</span><span class="sxs-lookup"><span data-stu-id="4186a-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="4186a-131">Das-Objekt kann über Übergänge verfügen.</span><span class="sxs-lookup"><span data-stu-id="4186a-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="4186a-132">Komposition, Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="4186a-132">Composition, Track</span></span>                |
| [<span data-ttu-id="4186a-133">**Iamtimelinesplicustom**</span><span class="sxs-lookup"><span data-stu-id="4186a-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="4186a-134">Das-Objekt kann in zwei-Objekte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4186a-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="4186a-135">Track, Source, Effect, Transition</span><span class="sxs-lookup"><span data-stu-id="4186a-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4186a-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4186a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4186a-137">Übersicht über die Zeitachsen Komponenten</span><span class="sxs-lookup"><span data-stu-id="4186a-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 




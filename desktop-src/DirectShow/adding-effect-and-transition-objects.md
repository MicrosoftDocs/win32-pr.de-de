---
description: Hinzufügen von Effekt-und Übergangs Objekten
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Hinzufügen von Effekt-und Übergangs Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041192"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="c8901-103">Hinzufügen von Effekt-und Übergangs Objekten</span><span class="sxs-lookup"><span data-stu-id="c8901-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="c8901-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="c8901-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c8901-105">In des wird ein Effekt oder Übergang mit zwei Objekten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="c8901-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="c8901-106">Ein *Zeitachsen Objekt* stellt den Effekt oder Übergang innerhalb der Zeitachse dar.</span><span class="sxs-lookup"><span data-stu-id="c8901-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="c8901-107">Für Effekte unterstützt das Timeline-Objekt die [**iamtimelineeffect**](iamtimelineeffect.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c8901-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="c8901-108">Bei Übergängen wird die [**iamtimelinetrans**](iamtimelinetrans.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8901-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="c8901-109">Beide Typen unterstützen die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c8901-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="c8901-110">Das unter *geordnete* Objekt ist ein Objekt, das die Datenverarbeitung für den Effekt oder Übergang implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8901-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="c8901-111">Das Timeline-Objekt enthält einen Zeiger auf das unter Objekt.</span><span class="sxs-lookup"><span data-stu-id="c8901-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="c8901-112">Führen Sie die folgenden Schritte aus, um einen Effekt oder Übergang hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8901-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="c8901-113">**1. Erstellen des Zeitachsen Objekts**</span><span class="sxs-lookup"><span data-stu-id="c8901-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="c8901-114">Um das Timeline-Objekt zu erstellen, rufen Sie die [**iamtimeline::**](iamtimeline-createemptynode.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c8901-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="c8901-115">Legen Sie den Typ auf die **Zeitachse des \_ Haupt \_ Typs \_** für einen Effekt oder einen **Zeitachsen \_ \_ \_ haupttypübergang** für einen Übergang fest.</span><span class="sxs-lookup"><span data-stu-id="c8901-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="c8901-116">Im folgenden Beispiel wird ein Übergangs Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="c8901-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="c8901-117">**2. Geben Sie das untergeordnete Objekt an.**</span><span class="sxs-lookup"><span data-stu-id="c8901-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="c8901-118">Das Zeitachsen Objekt fungiert als Wrapper für ein anderes Objekt, das *als untergeordnetes* Element bezeichnet wird, das die eigentliche Arbeit übernimmt.</span><span class="sxs-lookup"><span data-stu-id="c8901-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="c8901-119">Das untergeordnete Objekt implementiert eine Datentransformation, die den gewünschten Effekt oder Übergang erzeugt.</span><span class="sxs-lookup"><span data-stu-id="c8901-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="c8901-120">Eine Liste der Übergänge und Effekte, die mit des bereitgestellt werden, finden Sie unter [Übergänge und Effekte](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="c8901-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="c8901-121">Um das untergeordnete Objekt festzulegen, wenden Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode für das Timeline-Objekt an, und übergeben Sie dabei den Klassen Bezeichner (CLSID) des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8901-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="c8901-122">DirectShow bietet einen Enumerator für Video Effekte und Video Übergänge, die Sie zum Abrufen der CLSID verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c8901-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="c8901-123">Weitere Informationen finden Sie unter [Enumerieren von Effekten und Übergängen](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="c8901-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="c8901-124">Im folgenden Beispiel wird der [SMPTE](smpte-wipe-transition.md) -zurücksetzen-Übergang als untergeordnetes Objekt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c8901-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="c8901-125">**3. Festlegen der Start-und Endzeiten**</span><span class="sxs-lookup"><span data-stu-id="c8901-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="c8901-126">Um die Start-und Endzeit Zeiten festzulegen, müssen Sie die [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8901-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="c8901-127">Diese Zeiten sind relativ zur Startzeit des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8901-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="c8901-128">Die Auswirkungen können sich innerhalb desselben Objekts überlappen, aber Übergänge sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="c8901-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="c8901-129">Im folgenden Beispiel wird die Startzeit auf 5 Sekunden und die Endzeit auf 10 Sekunden festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c8901-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="c8901-130">Wenn ein Übergang gerendert wird, wird der Fortschritt des Übergangs bei jedem Frame basierend auf einer **Fortschritts** Eigenschaft berechnet, die zu einem Bereich von 0,0 bis 1,0 normalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8901-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="c8901-131">Des verwendet die Startzeit der einzelnen Frames, um den Fortschritts Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c8901-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="c8901-132">Dies bedeutet, **dass der Statuswert,** wenn die Übergangs Endzeit gleich der Quell Endzeit ist, nie genau 1,0 erreicht, da die Startzeit des letzten Frames etwas länger als die Endzeit ist.</span><span class="sxs-lookup"><span data-stu-id="c8901-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="c8901-133">Legen Sie die Übergangs Endzeit auf mindestens einen Frame vor der Quell Endzeit fest, damit der Übergang 1,0 erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="c8901-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="c8901-134">**4. Fügen Sie das Objekt in die Zeitachse ein**</span><span class="sxs-lookup"><span data-stu-id="c8901-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="c8901-135">Um das Objekt in die Zeitachse einzufügen, müssen Sie je nach Objekttyp eine der folgenden Methoden für das übergeordnete Element abrufen:</span><span class="sxs-lookup"><span data-stu-id="c8901-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="c8901-136">Effekte: [ **iamtimelineeffectable:: effectinsbefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="c8901-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="c8901-137">Übergänge: [ **iamtimelinetransable:: transadd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="c8901-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="c8901-138">In der [**iamtimelineeffectable:: effectinsbefore**](iamtimelineeffectable-effectinsbefore.md) -Methode müssen Sie die Priorität des Effekts angeben.</span><span class="sxs-lookup"><span data-stu-id="c8901-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="c8901-139">Wenn sich die Auswirkungen auf das gleiche Objekt überlappen, werden Sie in der Reihenfolge ihrer Priorität angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8901-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="c8901-140">Der volumeumschlag-Audioeffekt ist eine Ausnahme. Weitere Informationen finden Sie in der Referenz zu [volumeumschlags Effekten](volume-envelope-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="c8901-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="c8901-141">Innerhalb einer Komposition werden alle Audiospuren gemischt, bevor die Audioeffekte für diese Komposition angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8901-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="c8901-142">Da Übergänge sich nicht im selben Objekt überlappen können, haben Sie keinen Prioritätswert.</span><span class="sxs-lookup"><span data-stu-id="c8901-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="c8901-143">Im folgenden Beispiel wird das Übergangs Objekt zu einer Spur hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="c8901-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="c8901-144">Im Beispiel wird das Track-Objekt für die [**iamtimelinetransable**](iamtimelinetransable.md) -Schnittstelle abgefragt, bevor addTrans aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c8901-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="c8901-145">**5. Festlegen von Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="c8901-145">**5. Set Properties**</span></span>

<span data-ttu-id="c8901-146">Viele Effekte und Übergänge unterstützen benutzerdefinierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8901-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="c8901-147">Weitere Informationen finden Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="c8901-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="c8901-148">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c8901-148">Example</span></span>

<span data-ttu-id="c8901-149">Im folgenden Codebeispiel wird ein [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang zu einer Spur hinzugefügt. Es wird davon ausgegangen, dass das Track-Objekt bereits in der Zeitachse vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="c8901-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="c8901-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8901-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8901-151">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="c8901-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungs Filter Ausgabedaten generieren soll.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Erstellen von Daten in einem Erfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957969"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="d1607-103">Erstellen von Daten in einem Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="d1607-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="d1607-104">In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungs Filter Ausgabedaten generieren soll.</span><span class="sxs-lookup"><span data-stu-id="d1607-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="d1607-105">Filter Zustandsänderungen</span><span class="sxs-lookup"><span data-stu-id="d1607-105">Filter State Changes</span></span>

<span data-ttu-id="d1607-106">Ein Erfassungs Filter sollte nur dann Daten erstellen, wenn der Filter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1607-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="d1607-107">Senden Sie keine Daten von ihren Pins, wenn der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d1607-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="d1607-108">Geben Sie außerdem einen **VFW \_ S \_ \_** -Fehler von der [**cbasefilter:: GetState**](cbasefilter-getstate.md) -Methode zurück, wenn der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d1607-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="d1607-109">Mit diesem Rückgabewert wird dem Filter Diagramm-Manager mitgeteilt, dass er nicht auf Daten aus dem Filter warten soll, während der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d1607-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="d1607-110">Weitere Informationen finden Sie unter [Filter Zustände](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="d1607-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="d1607-111">Der folgende Code zeigt, wie die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="d1607-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="d1607-112">Steuern einzelner Streams</span><span class="sxs-lookup"><span data-stu-id="d1607-112">Controlling Individual Streams</span></span>

<span data-ttu-id="d1607-113">Die Ausgabe Pins eines Erfassungs Filters sollten die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle unterstützen, sodass eine Anwendung jede Pin einzeln aktivieren oder deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="d1607-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="d1607-114">Beispielsweise kann eine Anwendung ohne Erfassung eine Vorschau anzeigen und dann in den Aufzeichnungsmodus wechseln, ohne das Filter Diagramm neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1607-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="d1607-115">Sie können die [**cbasestreamcontrol**](cbasestreamcontrol.md) -Klasse verwenden, um diese Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d1607-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="d1607-116">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="d1607-116">Time Stamps</span></span>

<span data-ttu-id="d1607-117">Wenn der Filter eine Stichprobe erfasst, wird das Beispiel mit der aktuellen streamzeit versehen.</span><span class="sxs-lookup"><span data-stu-id="d1607-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="d1607-118">Die Endzeit ist die Startzeit und die Dauer.</span><span class="sxs-lookup"><span data-stu-id="d1607-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="d1607-119">Wenn der Filter beispielsweise bei zehn Samplings pro Sekunde erfasst und die streamzeit 200 Millionen Einheiten beträgt, wenn der Filter das Beispiel erfasst, sollten die Zeitstempel 200 Millionen und 201 Millionen lauten.</span><span class="sxs-lookup"><span data-stu-id="d1607-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="d1607-120">(Es sind 10 Millionen Einheiten pro Sekunde vorhanden.)</span><span class="sxs-lookup"><span data-stu-id="d1607-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="d1607-121">Um die streamzeit zu berechnen, müssen Sie die [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode aufrufen, um die aktuelle Verweis Zeit abzurufen. Anschließend wird die ursprüngliche Startzeit subtrahit.</span><span class="sxs-lookup"><span data-stu-id="d1607-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="d1607-122">Rufen Sie alternativ die [**cbasefilter:: streamtime**](cbasefilter-streamtime.md) -Methode auf, die dieselbe Berechnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="d1607-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="d1607-123">Um den Zeitstempel für ein Beispiel festzulegen, müssen Sie die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d1607-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="d1607-124">Wenn der Filter jedoch über eine Vorschau-Pin verfügt, sollten Beispiele aus der Vorschau-Pin keine Zeitstempel enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1607-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="d1607-125">Der Grund hierfür ist, dass die Beispiele den Renderer nach dem Zeitpunkt der Erfassung immer etwas erreichen.</span><span class="sxs-lookup"><span data-stu-id="d1607-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="d1607-126">Wenn die Beispiele Zeitstempel sind, behandelt der Renderer Sie als spät, und es kann versucht werden, Beispiele zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="d1607-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="d1607-127">(Weitere Informationen finden Sie unter [DirectShow-Video Erfassungs Filter](directshow-video-capture-filters.md).) Beachten Sie, dass die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle erfordert, dass die PIN die Stichproben Zeiten nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="d1607-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="d1607-128">Für eine Vorschau-PIN müssen Sie möglicherweise die Implementierung ändern, damit Sie nicht auf Zeitstempel angewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d1607-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="d1607-129">Zeitstempel müssen immer von einem Beispiel auf das nächste erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="d1607-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="d1607-130">Dies gilt auch, wenn der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d1607-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="d1607-131">Wenn der Filter ausgeführt wird, angehalten und dann erneut ausgeführt wird, muss das erste Beispiel nach der Pause einen größeren Zeitstempel aufweisen als das letzte Beispiel vor der Pause.</span><span class="sxs-lookup"><span data-stu-id="d1607-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="d1607-132">Abhängig von den Daten, die Sie erfassen, kann es sinnvoll sein, die Medien Zeit für die Beispiele festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d1607-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="d1607-133">Weitere Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d1607-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1607-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1607-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1607-135">DirectShow-Video Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="d1607-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="d1607-136">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1607-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d1607-137">Schreiben von Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="d1607-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 




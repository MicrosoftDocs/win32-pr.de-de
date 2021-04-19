---
description: Diese Klasse implementiert die iamstreamcontrol-Schnittstelle für Eingabe-und Ausgabe Pins.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Cbasestreamcontrol-Klasse ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370646"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="396c6-103">Cbasestreamcontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="396c6-103">CBaseStreamControl class</span></span>

![cbasestreamcontrol-Klassenhierarchie](images/strmctl1.png)

<span data-ttu-id="396c6-105">Diese Klasse implementiert die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle für Eingabe-und Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="396c6-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="396c6-106">Er bietet Kontrolle über das Starten und Beenden einer einzelnen PIN für den Filter.</span><span class="sxs-lookup"><span data-stu-id="396c6-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="396c6-107">Eine PIN, die **iamstreamcontrol** unterstützt, sollte von dieser Basisklasse erben.</span><span class="sxs-lookup"><span data-stu-id="396c6-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="396c6-108">Im folgenden finden Sie eine typische Deklaration für eine Eingabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="396c6-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="396c6-109">Stellen Sie sicher, dass **nondelegatingqueryinteface** überschrieben wird, um **iamstreamcontrol** verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="396c6-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="396c6-110">Weitere Informationen finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="396c6-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="396c6-111">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="396c6-111">Public Methods</span></span>                                                        | <span data-ttu-id="396c6-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="396c6-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="396c6-113">**Cbasestreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="396c6-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="396c6-114">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="396c6-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="396c6-115">**~ Cbasestreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="396c6-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="396c6-116">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="396c6-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="396c6-117">**Checkstreamstate**</span><span class="sxs-lookup"><span data-stu-id="396c6-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="396c6-118">Bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.</span><span class="sxs-lookup"><span data-stu-id="396c6-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="396c6-119">**Lak**</span><span class="sxs-lookup"><span data-stu-id="396c6-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="396c6-120">Benachrichtigt die Basisklasse, dass die PIN gestartet oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="396c6-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="396c6-121">**Notifyfilterstate**</span><span class="sxs-lookup"><span data-stu-id="396c6-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="396c6-122">Benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="396c6-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="396c6-123">**Setfiltergraph**</span><span class="sxs-lookup"><span data-stu-id="396c6-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="396c6-124">Gibt die Ereignis Senke für streamsteuerungsereignisse an.</span><span class="sxs-lookup"><span data-stu-id="396c6-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="396c6-125">**Setsyncsource**</span><span class="sxs-lookup"><span data-stu-id="396c6-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="396c6-126">Benachrichtigt die Basisklasse der aktuellen verweisuhr.</span><span class="sxs-lookup"><span data-stu-id="396c6-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="396c6-127">Iamstreamcontrol-Methoden</span><span class="sxs-lookup"><span data-stu-id="396c6-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="396c6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="396c6-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="396c6-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="396c6-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="396c6-130">Ruft Informationen zu den aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="396c6-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="396c6-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="396c6-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="396c6-132">Informiert die PIN, wann mit der Übermittlung von Daten begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="396c6-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="396c6-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="396c6-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="396c6-134">Informiert den PIN, wann die Übermittlung von Daten beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="396c6-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="396c6-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="396c6-135">Remarks</span></span>

<span data-ttu-id="396c6-136">Diese Klasse erfordert, dass die PIN und der besitzende Filter die Klasse Benachrichtigen, wenn verschiedene Ereignisse auftreten, z. b. der Filter, der dem Diagramm Beitritt oder eine neue verweisuhr empfängt.</span><span class="sxs-lookup"><span data-stu-id="396c6-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="396c6-137">Sie sollten die folgenden Klassen Methoden aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="396c6-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="396c6-138">In der [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode des Filters aufrufen Sie die [**cbasestreamcontrol:: setsyncsource**](cbasestreamcontrol-setsyncsource.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="396c6-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="396c6-139">Diese Methode benachrichtigt die-Klasse über die aktuelle verweisuhr.</span><span class="sxs-lookup"><span data-stu-id="396c6-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="396c6-140">In der [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Methode des Filters aufrufen Sie die [**cbasestreamcontrol:: setfiltergraph**](cbasestreamcontrol-setfiltergraph.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="396c6-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="396c6-141">Diese Methode gibt der Klasse einen Zeiger auf den Filter Graph-Manager, sodass die Klasse die richtigen streamsteuerungsereignisse senden kann.</span><span class="sxs-lookup"><span data-stu-id="396c6-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="396c6-142">Wenn der Filter den Zustand ändert (in "wird ausgeführt", "angehalten" oder "beendet"), wird die Methode [**cbasestreamcontrol:: notifyfilterstate**](cbasestreamcontrol-notifyfilterstate.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="396c6-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="396c6-143">In den [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden der PIN wird die [**cbasestreamcontrol::**](cbasestreamcontrol-flushing.md) Flush-Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="396c6-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="396c6-144">Die `CBaseStreamControl` -Klasse verwendet die Referenzuhr des Filter Diagramms, um zu bestimmen, welche Beispiele der Filter liefern soll und welche verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="396c6-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="396c6-145">Aufrufen Sie in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der PIN die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode mit einem Zeiger auf das Beispiel für eingehende Medien.</span><span class="sxs-lookup"><span data-stu-id="396c6-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="396c6-146">Wenn die Methode den Wert für den wertstream zurückgibt, übermitteln Sie \_ das Beispiel Downstream.</span><span class="sxs-lookup"><span data-stu-id="396c6-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="396c6-147">Verwerfen Sie diese andernfalls.</span><span class="sxs-lookup"><span data-stu-id="396c6-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="396c6-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="396c6-148">Requirements</span></span>



| <span data-ttu-id="396c6-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="396c6-149">Requirement</span></span> | <span data-ttu-id="396c6-150">Wert</span><span class="sxs-lookup"><span data-stu-id="396c6-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="396c6-151">Header</span><span class="sxs-lookup"><span data-stu-id="396c6-151">Header</span></span><br/>  | <dl> <span data-ttu-id="396c6-152"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="396c6-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="396c6-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="396c6-153">Library</span></span><br/> | <dl> <span data-ttu-id="396c6-154">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="396c6-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





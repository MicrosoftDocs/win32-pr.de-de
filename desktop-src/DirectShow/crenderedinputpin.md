---
description: Die crenderedinputpin-Klasse ist eine Basisklasse zum Implementieren einer Eingabe-PIN für einen Renderer.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Crenderedinputpin-Klasse (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370146"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="ca12b-103">Crenderedinputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca12b-103">CRenderedInputPin class</span></span>

![crenderedinputpin-Klassenhierarchie](images/rbase04.png)

<span data-ttu-id="ca12b-105">Die **crenderedinputpin** -Klasse ist eine Basisklasse zum Implementieren einer Eingabe-PIN für einen Renderer.</span><span class="sxs-lookup"><span data-stu-id="ca12b-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="ca12b-106">Diese Klasse wurde für Renderer-Filter entwickelt, die nicht von der [**cbaserenderer**](cbaserenderer.md) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ca12b-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="ca12b-107">(Filter, die von **cbaserenderer** abgeleitet werden, sollten die [**crendererinputpin**](crendererinputpin.md) -Klasse für die Eingabe-PIN verwenden.)</span><span class="sxs-lookup"><span data-stu-id="ca12b-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="ca12b-108">Um diese Klasse verwenden zu können, müssen Sie mindestens die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="ca12b-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="ca12b-109">Deklarieren Sie eine neue PIN-Klasse, die **crenderedinputpin** erbt.</span><span class="sxs-lookup"><span data-stu-id="ca12b-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="ca12b-110">Deklarieren Sie in der PIN-Klasse ein kritisches Abschnitts Objekt, das die streamingsperre enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="ca12b-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="ca12b-111">Zu diesem Zweck können Sie die [**ccritsec**](ccritsec.md) -Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca12b-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="ca12b-112">Weitere Informationen finden Sie unter [Threads und wichtige Abschnitte](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="ca12b-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="ca12b-113">Überschreiben Sie [**crenderedinputpin:: EndOfStream**](crenderedinputpin-endofstream.md) , um die streamingsperre aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ca12b-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="ca12b-114">Implementieren Sie die Methoden [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md)und [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="ca12b-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="ca12b-115">Implementieren Sie in Ihrem Filter [**cbasefilter:: getpin**](cbasefilter-getpin.md) , um eine Instanz der PIN-Klasse zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca12b-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="ca12b-116">Sie können diese Klasse in einem Renderer verwenden, der über mehr als eine Eingabe-PIN verfügt.</span><span class="sxs-lookup"><span data-stu-id="ca12b-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="ca12b-117">Diese Klasse erbt die [**cbasinput Pin**](cbaseinputpin.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ca12b-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="ca12b-118">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="ca12b-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="ca12b-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca12b-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca12b-120">**m \_ batendofistream**</span><span class="sxs-lookup"><span data-stu-id="ca12b-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="ca12b-121">Gibt an, ob das Ende des Streams erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="ca12b-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="ca12b-122">**m \_ bcompletenotifiziert**</span><span class="sxs-lookup"><span data-stu-id="ca12b-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="ca12b-123">Gibt an, ob die PIN ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Diagramm-Manager gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="ca12b-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="ca12b-124">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="ca12b-124">Public Methods</span></span>                                                        | <span data-ttu-id="ca12b-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca12b-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="ca12b-126">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="ca12b-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="ca12b-127">Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ca12b-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="ca12b-128">**Crenderedinputpin**</span><span class="sxs-lookup"><span data-stu-id="ca12b-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="ca12b-129">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ca12b-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="ca12b-130">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="ca12b-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="ca12b-131">Benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca12b-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="ca12b-132">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="ca12b-132">IPin Methods</span></span>                                                          | <span data-ttu-id="ca12b-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca12b-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="ca12b-134">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="ca12b-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="ca12b-135">Beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="ca12b-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="ca12b-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ca12b-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="ca12b-137">Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis der Filter einen neuen Befehl zum Ausführen erhält.</span><span class="sxs-lookup"><span data-stu-id="ca12b-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="ca12b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca12b-138">Requirements</span></span>



| <span data-ttu-id="ca12b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca12b-139">Requirement</span></span> | <span data-ttu-id="ca12b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ca12b-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca12b-141">Header</span><span class="sxs-lookup"><span data-stu-id="ca12b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ca12b-142"><dt>Amextra. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca12b-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca12b-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca12b-143">Library</span></span><br/> | <dl> <span data-ttu-id="ca12b-144">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca12b-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





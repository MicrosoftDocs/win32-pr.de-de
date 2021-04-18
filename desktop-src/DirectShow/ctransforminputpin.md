---
description: Die ctransforminputpin-Klasse implementiert eine Eingabe-PIN, die von der ctransformfilter-Klasse verwendet wird.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Ctransforminputpin-Klasse (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354820"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="c7ba4-103">Ctransforminputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7ba4-103">CTransformInputPin class</span></span>

![ctransforminputpin-Klassenhierarchie](images/tfrm01.png)

<span data-ttu-id="c7ba4-105">Die- `CTransformInputPin` Klasse implementiert eine Eingabe-PIN, die von der [**ctransformfilter**](ctransformfilter.md) -Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="c7ba4-106">In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="c7ba4-107">Die meisten Methoden in dieser Klasse können die entsprechenden Methoden der **ctransformfilter** -Klasse aufzurufen, die Sie überschreiben können.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="c7ba4-108">Wenn Sie von dieser Klasse ableiten, müssen Sie die [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="c7ba4-109">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="c7ba4-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="c7ba4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7ba4-111">**m \_ ptransformfilter**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="c7ba4-112">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="c7ba4-113">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="c7ba4-113">Public Methods</span></span>                                                       | <span data-ttu-id="c7ba4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-114">Description</span></span>                                                                            |
| [<span data-ttu-id="c7ba4-115">**Ctransforminputpin**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="c7ba4-116">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="c7ba4-117">**Check Connect**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="c7ba4-118">Bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="c7ba4-119">**Breakconnect**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="c7ba4-120">Gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="c7ba4-121">**Completeconnect**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="c7ba4-122">Schließt eine Verbindung mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="c7ba4-123">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="c7ba4-124">Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="c7ba4-125">**Setmediatype**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="c7ba4-126">Legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="c7ba4-127">**Checkstreaming**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="c7ba4-128">Bestimmt, ob die PIN Beispiele annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="c7ba4-129">Virtu.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-129">Virtual.</span></span>                                |
| [<span data-ttu-id="c7ba4-130">**Currentmediatype**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="c7ba4-131">Ruft den Medientyp für die aktuelle PIN-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="c7ba4-132">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="c7ba4-132">IPin Methods</span></span>                                                         | <span data-ttu-id="c7ba4-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-133">Description</span></span>                                                                            |
| [<span data-ttu-id="c7ba4-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="c7ba4-135">Ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="c7ba4-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="c7ba4-137">Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="c7ba4-138">**Beginflush**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="c7ba4-139">Startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="c7ba4-140">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="c7ba4-141">Beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="c7ba4-142">**Newsegment**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="c7ba4-143">Benachrichtigt die PIN, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="c7ba4-144">IMemInputPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="c7ba4-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="c7ba4-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7ba4-145">Description</span></span>                                                                            |
| [<span data-ttu-id="c7ba4-146">**Medizinisch**</span><span class="sxs-lookup"><span data-stu-id="c7ba4-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="c7ba4-147">Empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="c7ba4-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="c7ba4-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7ba4-148">Requirements</span></span>



| <span data-ttu-id="c7ba4-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7ba4-149">Requirement</span></span> | <span data-ttu-id="c7ba4-150">Wert</span><span class="sxs-lookup"><span data-stu-id="c7ba4-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ba4-151">Header</span><span class="sxs-lookup"><span data-stu-id="c7ba4-151">Header</span></span><br/>  | <dl> <span data-ttu-id="c7ba4-152"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7ba4-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c7ba4-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7ba4-153">Library</span></span><br/> | <dl> <span data-ttu-id="c7ba4-154">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c7ba4-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





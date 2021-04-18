---
description: Die ctransformoutputpin-Klasse implementiert eine Ausgabe-PIN, die von der ctransformfilter-Klasse verwendet wird.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Ctransformoutputpin-Klasse (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371771"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="26431-103">Ctransformoutputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="26431-103">CTransformOutputPin class</span></span>

![ctransformoutputpin-Klassenhierarchie](images/tfrm02.png)

<span data-ttu-id="26431-105">Die- `CTransformOutputPin` Klasse implementiert eine Ausgabe-PIN, die von der [**ctransformfilter**](ctransformfilter.md) -Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26431-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="26431-106">In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen.</span><span class="sxs-lookup"><span data-stu-id="26431-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="26431-107">Die meisten Methoden in dieser Klasse können die entsprechenden Methoden der **ctransformfilter** -Klasse aufzurufen, die Sie überschreiben können.</span><span class="sxs-lookup"><span data-stu-id="26431-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="26431-108">Wenn Sie von dieser Klasse ableiten, müssen Sie die [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="26431-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="26431-109">Diese Klasse macht die Schnittstellen **imediaseeking** und **imediaposition** über das [**cpospassthru**](cpospassthru.md) -Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26431-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="26431-110">Alle Suchanforderungen werden an den nächsten Filter Upstream weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="26431-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="26431-111">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="26431-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="26431-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26431-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="26431-113">**m \_ ptransformfilter**</span><span class="sxs-lookup"><span data-stu-id="26431-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="26431-114">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="26431-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="26431-115">Öffentliche Element Variablen</span><span class="sxs-lookup"><span data-stu-id="26431-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="26431-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26431-116">Description</span></span>                                              |
| [<span data-ttu-id="26431-117">**m \_ pposition**</span><span class="sxs-lookup"><span data-stu-id="26431-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="26431-118">Hilfsobjekt, um Seek-Befehle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="26431-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="26431-119">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="26431-119">Public Methods</span></span>                                                           | <span data-ttu-id="26431-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26431-120">Description</span></span>                                              |
| [<span data-ttu-id="26431-121">**Ctransformoutputpin**</span><span class="sxs-lookup"><span data-stu-id="26431-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="26431-122">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="26431-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="26431-123">**~ Ctransformoutputpin**</span><span class="sxs-lookup"><span data-stu-id="26431-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="26431-124">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="26431-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="26431-125">**Check Connect**</span><span class="sxs-lookup"><span data-stu-id="26431-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="26431-126">Bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="26431-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="26431-127">**Breakconnect**</span><span class="sxs-lookup"><span data-stu-id="26431-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="26431-128">Gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="26431-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="26431-129">**Completeconnect**</span><span class="sxs-lookup"><span data-stu-id="26431-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="26431-130">Schließt eine Verbindung mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="26431-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="26431-131">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="26431-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="26431-132">Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="26431-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="26431-133">**Setmediatype**</span><span class="sxs-lookup"><span data-stu-id="26431-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="26431-134">Legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="26431-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="26431-135">**Decidebuffersize**</span><span class="sxs-lookup"><span data-stu-id="26431-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="26431-136">Legt die Puffer Anforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="26431-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="26431-137">**Getmediatype**</span><span class="sxs-lookup"><span data-stu-id="26431-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="26431-138">Ruft einen bevorzugten Medientyp nach Indexwert ab.</span><span class="sxs-lookup"><span data-stu-id="26431-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="26431-139">**Currentmediatype**</span><span class="sxs-lookup"><span data-stu-id="26431-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="26431-140">Ruft den Medientyp für die aktuelle PIN-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="26431-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="26431-141">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="26431-141">IPin Methods</span></span>                                                             | <span data-ttu-id="26431-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26431-142">Description</span></span>                                              |
| [<span data-ttu-id="26431-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="26431-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="26431-144">Ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="26431-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="26431-145">Iqualitycontrol-Methoden</span><span class="sxs-lookup"><span data-stu-id="26431-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="26431-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26431-146">Description</span></span>                                              |
| [<span data-ttu-id="26431-147">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="26431-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="26431-148">Benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="26431-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="26431-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26431-149">Requirements</span></span>



| <span data-ttu-id="26431-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26431-150">Requirement</span></span> | <span data-ttu-id="26431-151">Wert</span><span class="sxs-lookup"><span data-stu-id="26431-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26431-152">Header</span><span class="sxs-lookup"><span data-stu-id="26431-152">Header</span></span><br/>  | <dl> <span data-ttu-id="26431-153"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26431-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26431-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26431-154">Library</span></span><br/> | <dl> <span data-ttu-id="26431-155">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="26431-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





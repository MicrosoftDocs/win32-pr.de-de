---
description: Die ctransinplaceinputpin-Klasse implementiert eine Eingabe-PIN, die von der ctransinplacefilter-Klasse verwendet wird.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Ctransinplaceinputpin-Klasse (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371026"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="50676-103">Ctransinplaceinputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="50676-103">CTransInPlaceInputPin class</span></span>

![ctransinplaceinputpin-Klassenhierarchie](images/tsip01.png)

<span data-ttu-id="50676-105">Die- `CTransInPlaceInputPin` Klasse implementiert eine Eingabe-PIN, die von der [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50676-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="50676-106">In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen.</span><span class="sxs-lookup"><span data-stu-id="50676-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="50676-107">Wenn Sie dies tun, müssen Sie die [**ctransinplacefilter:: getpin**](ctransinplacefilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50676-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="50676-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="50676-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="50676-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50676-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="50676-110">**\_nur m Brot**</span><span class="sxs-lookup"><span data-stu-id="50676-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="50676-111">Flag, das angibt, ob der Eingabestream schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="50676-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="50676-112">**m \_ ptipfilter**</span><span class="sxs-lookup"><span data-stu-id="50676-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="50676-113">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="50676-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="50676-114">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="50676-114">Public Methods</span></span>                                                                      | <span data-ttu-id="50676-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50676-115">Description</span></span>                                                |
| [<span data-ttu-id="50676-116">**Ctransinplaceinputpin**</span><span class="sxs-lookup"><span data-stu-id="50676-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="50676-117">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="50676-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="50676-118">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="50676-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="50676-119">Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="50676-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="50676-120">**Peer Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="50676-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="50676-121">Ruft einen Zeiger auf die Zuweisung der PIN ab.</span><span class="sxs-lookup"><span data-stu-id="50676-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="50676-122">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="50676-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="50676-123">Gibt an, ob der Eingabestream schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="50676-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="50676-124">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="50676-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="50676-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50676-125">Description</span></span>                                                |
| [<span data-ttu-id="50676-126">**Enummediatypes**</span><span class="sxs-lookup"><span data-stu-id="50676-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="50676-127">Listet die bevorzugten Medientypen der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="50676-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="50676-128">IMemInputPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="50676-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="50676-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50676-129">Description</span></span>                                                |
| [<span data-ttu-id="50676-130">**Getallocator**</span><span class="sxs-lookup"><span data-stu-id="50676-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="50676-131">Ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="50676-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="50676-132">**Notifyzukator**</span><span class="sxs-lookup"><span data-stu-id="50676-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="50676-133">Gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="50676-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="50676-134">**Getalloserorrequirements**</span><span class="sxs-lookup"><span data-stu-id="50676-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="50676-135">Ruft die von der PIN angeforderten zuordnereigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="50676-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="50676-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50676-136">Requirements</span></span>



| <span data-ttu-id="50676-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50676-137">Requirement</span></span> | <span data-ttu-id="50676-138">Wert</span><span class="sxs-lookup"><span data-stu-id="50676-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50676-139">Header</span><span class="sxs-lookup"><span data-stu-id="50676-139">Header</span></span><br/>  | <dl> <span data-ttu-id="50676-140"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50676-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50676-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50676-141">Library</span></span><br/> | <dl> <span data-ttu-id="50676-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="50676-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





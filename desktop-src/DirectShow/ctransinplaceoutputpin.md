---
description: Die ctransinplaceoutputpin-Klasse implementiert eine Ausgabe-PIN, die von der ctransinplacefilter-Klasse verwendet wird.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Ctransinplaceoutputpin-Klasse (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359289"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="4e66a-103">Ctransinplaceoutputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e66a-103">CTransInPlaceOutputPin class</span></span>

![ctransinplaceoutputpin-Klassenhierarchie](images/tsip02.png)

<span data-ttu-id="4e66a-105">Die- `CTransInPlaceOutputPin` Klasse implementiert eine Ausgabe-PIN, die von der [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e66a-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="4e66a-106">In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen.</span><span class="sxs-lookup"><span data-stu-id="4e66a-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="4e66a-107">Wenn Sie dies tun, müssen Sie die [**ctransinplacefilter:: getpin**](ctransinplacefilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e66a-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="4e66a-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="4e66a-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="4e66a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e66a-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="4e66a-110">**m \_ ptipfilter**</span><span class="sxs-lookup"><span data-stu-id="4e66a-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="4e66a-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="4e66a-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="4e66a-112">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="4e66a-112">Public Methods</span></span>                                                                  | <span data-ttu-id="4e66a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e66a-113">Description</span></span>                                          |
| [<span data-ttu-id="4e66a-114">**Ctransinplaceoutputpin**</span><span class="sxs-lookup"><span data-stu-id="4e66a-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="4e66a-115">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4e66a-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="4e66a-116">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="4e66a-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="4e66a-117">Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4e66a-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="4e66a-118">**"Stallocator"**</span><span class="sxs-lookup"><span data-stu-id="4e66a-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="4e66a-119">Gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="4e66a-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="4e66a-120">**Connectedimeminputpin**</span><span class="sxs-lookup"><span data-stu-id="4e66a-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="4e66a-121">Ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="4e66a-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="4e66a-122">**Peer Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="4e66a-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="4e66a-123">Ruft einen Zeiger auf die Zuweisung der PIN ab.</span><span class="sxs-lookup"><span data-stu-id="4e66a-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="4e66a-124">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="4e66a-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="4e66a-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e66a-125">Description</span></span>                                          |
| [<span data-ttu-id="4e66a-126">**Enummediatypes**</span><span class="sxs-lookup"><span data-stu-id="4e66a-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="4e66a-127">Listet die bevorzugten Medientypen der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="4e66a-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="4e66a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e66a-128">Requirements</span></span>



| <span data-ttu-id="4e66a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e66a-129">Requirement</span></span> | <span data-ttu-id="4e66a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4e66a-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e66a-131">Header</span><span class="sxs-lookup"><span data-stu-id="4e66a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4e66a-132"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e66a-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e66a-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e66a-133">Library</span></span><br/> | <dl> <span data-ttu-id="4e66a-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4e66a-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: Die cenumpins-Klasse implementiert einen Enumerator für Pins.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Cenumpins-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365509"
---
# <a name="cenumpins-class"></a><span data-ttu-id="ce129-103">Cenumpins-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce129-103">CEnumPins class</span></span>

![cenumpins-Klassenhierarchie](images/filter03.png)

<span data-ttu-id="ce129-105">Die- `CEnumPins` Klasse implementiert einen Enumerator für Pins.</span><span class="sxs-lookup"><span data-stu-id="ce129-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="ce129-106">Diese Klasse implementiert die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ce129-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="ce129-107">Die folgenden [**cbasefilter**](cbasefilter.md) -Methoden werden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="ce129-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="ce129-108">[**Cbasefilter:: getpin**](cbasefilter-getpin.md): Ruft eine PIN für den Filter ab, auf die durch einen NULL basierten Index verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce129-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="ce129-109">[**Cbasefilter:: getpincount**](cbasefilter-getpincount.md): Ruft die Gesamtanzahl der Pins für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="ce129-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="ce129-110">[**Cbasefilter:: getpinversion**](cbasefilter-getpinversion.md): bestimmt, ob die Pins geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ce129-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="ce129-111">Wenn der Filter Pins dynamisch erstellt oder zerstört, erhöht er die PIN-Version, wenn die Pins geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ce129-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="ce129-112">Wenn die Versionsnummer geändert wird, wird das Enumeratorobjekt nicht mehr mit dem Filter synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ce129-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="ce129-113">Sobald der Enumerator nicht mehr synchronisiert ist, geben die Methoden in `CEnumPins` VFW \_ E \_ Enum \_ nicht \_ \_ synchron zurück.</span><span class="sxs-lookup"><span data-stu-id="ce129-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="ce129-114">Zum erneuten Synchronisieren des Enumerators wird die [**cenumpins:: Reset**](cenumpins-reset.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce129-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="ce129-115">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="ce129-115">Public Methods</span></span>                             | <span data-ttu-id="ce129-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce129-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="ce129-117">**Cenumpins**</span><span class="sxs-lookup"><span data-stu-id="ce129-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="ce129-118">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ce129-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="ce129-119">**~ Cenumpins**</span><span class="sxs-lookup"><span data-stu-id="ce129-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="ce129-120">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ce129-120">Destructor method.</span></span> <span data-ttu-id="ce129-121">Virtu.</span><span class="sxs-lookup"><span data-stu-id="ce129-121">Virtual.</span></span>                                     |
| <span data-ttu-id="ce129-122">Ienumins-Methoden</span><span class="sxs-lookup"><span data-stu-id="ce129-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="ce129-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce129-123">Description</span></span>                                                     |
| [<span data-ttu-id="ce129-124">**Klon**</span><span class="sxs-lookup"><span data-stu-id="ce129-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="ce129-125">Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand.</span><span class="sxs-lookup"><span data-stu-id="ce129-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="ce129-126">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="ce129-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="ce129-127">Ruft eine angegebene Anzahl von Pins ab.</span><span class="sxs-lookup"><span data-stu-id="ce129-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="ce129-128">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ce129-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="ce129-129">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="ce129-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="ce129-130">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="ce129-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="ce129-131">Überspringt eine angegebene Anzahl von Pins.</span><span class="sxs-lookup"><span data-stu-id="ce129-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="ce129-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce129-132">Requirements</span></span>



| <span data-ttu-id="ce129-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce129-133">Requirement</span></span> | <span data-ttu-id="ce129-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ce129-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce129-135">Header</span><span class="sxs-lookup"><span data-stu-id="ce129-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ce129-136"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce129-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce129-137">Library</span></span><br/> | <dl> <span data-ttu-id="ce129-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





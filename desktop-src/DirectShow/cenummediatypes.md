---
description: Die cenummediatypes-Klasse implementiert einen Enumerator für bevorzugte Medientypen.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Cenumschlag mediatypes-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354664"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="ff726-103">Cenum mediatypes-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff726-103">CEnumMediaTypes class</span></span>

![cenenmediatypes-Klassenhierarchie](images/filter04.png)

<span data-ttu-id="ff726-105">Die- `CEnumMediaTypes` Klasse implementiert einen Enumerator für bevorzugte Medientypen.</span><span class="sxs-lookup"><span data-stu-id="ff726-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="ff726-106">Diese Klasse implementiert die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ff726-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="ff726-107">Die folgenden [**cbasepin**](cbasepin.md) -Methoden werden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="ff726-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="ff726-108">[**Cbasepin:: getmediatype**](cbasepin-getmediatype.md): Ruft einen Medientyp ab, auf den von einem NULL basierten Index verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ff726-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="ff726-109">[**Cbasepin:: getmediatyetversion**](cbasepin-getmediatypeversion.md): bestimmt, ob sich der Satz bevorzugter Typen geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ff726-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="ff726-110">Wenn eine PIN die Liste der bevorzugten Medientypen ändert, erhöht die PIN die Medientyp-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="ff726-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="ff726-111">In diesem Fall wird das Enumeratorobjekt nicht mehr mit der PIN synchronisiert, und die Klassen Methoden geben die Vfw E-Enumeration nicht \_ \_ synchron zurück \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ff726-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="ff726-112">Aufrufen der Methode [**cenummediatypes:: Reset**](cenummediatypes-reset.md) zum erneuten Synchronisieren des Enumerators.</span><span class="sxs-lookup"><span data-stu-id="ff726-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="ff726-113">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="ff726-113">Public Methods</span></span>                                               | <span data-ttu-id="ff726-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff726-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="ff726-115">**Cenum mediatypes**</span><span class="sxs-lookup"><span data-stu-id="ff726-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="ff726-116">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ff726-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="ff726-117">**~ Cenum mediatypes**</span><span class="sxs-lookup"><span data-stu-id="ff726-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="ff726-118">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ff726-118">Destructor method.</span></span> <span data-ttu-id="ff726-119">Virtu.</span><span class="sxs-lookup"><span data-stu-id="ff726-119">Virtual.</span></span>                                     |
| <span data-ttu-id="ff726-120">Ienummediatypes-Methoden</span><span class="sxs-lookup"><span data-stu-id="ff726-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="ff726-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff726-121">Description</span></span>                                                     |
| [<span data-ttu-id="ff726-122">**Klon**</span><span class="sxs-lookup"><span data-stu-id="ff726-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="ff726-123">Erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand.</span><span class="sxs-lookup"><span data-stu-id="ff726-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="ff726-124">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="ff726-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="ff726-125">Ruft eine angegebene Anzahl von Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="ff726-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="ff726-126">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ff726-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="ff726-127">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="ff726-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="ff726-128">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="ff726-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="ff726-129">Überspringt eine angegebene Anzahl von Medientypen.</span><span class="sxs-lookup"><span data-stu-id="ff726-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="ff726-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff726-130">Requirements</span></span>



| <span data-ttu-id="ff726-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff726-131">Requirement</span></span> | <span data-ttu-id="ff726-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ff726-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff726-133">Header</span><span class="sxs-lookup"><span data-stu-id="ff726-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ff726-134"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff726-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff726-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff726-135">Library</span></span><br/> | <dl> <span data-ttu-id="ff726-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff726-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





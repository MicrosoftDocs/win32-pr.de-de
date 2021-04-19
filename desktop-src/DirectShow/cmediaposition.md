---
description: Die cmediaposition-Klasse verarbeitet die IDispatch-Methoden der Dual-Schnittstelle imediaposition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Cmediaposition-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369623"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="65b78-103">Cmediaposition-Klasse</span><span class="sxs-lookup"><span data-stu-id="65b78-103">CMediaPosition class</span></span>

![cmediaposition-Klassenhierarchie](images/cutil14.png)

<span data-ttu-id="65b78-105">Die **cmediaposition** -Klasse verarbeitet die **IDispatch** -Methoden der Dual-Schnittstelle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="65b78-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="65b78-106">Diese Klasse erbt die Schnittstelle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) , implementiert Sie jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="65b78-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="65b78-107">**IDispatch** wird durch die [**cbasedispatch**](cbasedispatch.md) -Klasse und die DirectShow-Typbibliothek implementiert.</span><span class="sxs-lookup"><span data-stu-id="65b78-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="65b78-108">Verwenden Sie diese Klasse nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="65b78-108">Do not use this class directly.</span></span> <span data-ttu-id="65b78-109">Verwenden Sie stattdessen eine der folgenden Klassen:</span><span class="sxs-lookup"><span data-stu-id="65b78-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="65b78-110">Quell Filter: Verwenden Sie die [**csourceseeking**](csourceseeking.md) -Basisklasse, um Suchvorgänge zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="65b78-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="65b78-111">Transformations Filter: Verwenden Sie die [**cpospassthru**](cpospassthru.md) -Klasse, um Such Befehle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="65b78-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="65b78-112">Renderer: Verwenden Sie die [**crendererpospassthru**](crendererpospassthru.md) -Klasse, um Such Befehle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="65b78-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="65b78-113">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="65b78-113">Public Methods</span></span>                                              | <span data-ttu-id="65b78-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65b78-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65b78-115">**Cmediaposition**</span><span class="sxs-lookup"><span data-stu-id="65b78-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="65b78-116">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="65b78-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="65b78-117">IDispatch-Methoden</span><span class="sxs-lookup"><span data-stu-id="65b78-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="65b78-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65b78-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="65b78-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="65b78-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="65b78-120">Ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.</span><span class="sxs-lookup"><span data-stu-id="65b78-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="65b78-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="65b78-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="65b78-122">Ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="65b78-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="65b78-123">**Gettypeingefocount**</span><span class="sxs-lookup"><span data-stu-id="65b78-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="65b78-124">Ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="65b78-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="65b78-125">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="65b78-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="65b78-126">Bietet Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="65b78-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="65b78-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65b78-127">Requirements</span></span>



| <span data-ttu-id="65b78-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65b78-128">Requirement</span></span> | <span data-ttu-id="65b78-129">Wert</span><span class="sxs-lookup"><span data-stu-id="65b78-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b78-130">Header</span><span class="sxs-lookup"><span data-stu-id="65b78-130">Header</span></span><br/>  | <dl> <span data-ttu-id="65b78-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65b78-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65b78-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65b78-132">Library</span></span><br/> | <dl> <span data-ttu-id="65b78-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="65b78-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b78-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65b78-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b78-135">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="65b78-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 





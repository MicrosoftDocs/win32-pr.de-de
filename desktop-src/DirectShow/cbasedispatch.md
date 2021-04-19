---
description: Die cbasedispatch-Klasse ist eine Basisklasse zum Implementieren der IDispatch-Schnittstelle in einem DirectShow-Filter.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Cbasedispatch-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361910"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="9d624-103">Cbasedispatch-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d624-103">CBaseDispatch class</span></span>

![cbasedispatch-Klassenhierarchie](images/cutil01.png)

<span data-ttu-id="9d624-105">Die **cbasedispatch** -Klasse ist eine Basisklasse zum Implementieren der **IDispatch** -Schnittstelle in einem DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="9d624-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="9d624-106">Diese Klasse ist auf die Unterstützung der Automatisierungs kompatiblen Schnittstellen beschränkt, die von der DirectShow-Typbibliothek, QuartzTypeLib, exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d624-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="9d624-107">Beispielsweise verwenden die Klassen [**cmediacontrol**](cmediacontrol.md) und [**cmediaposition**](cmediaposition.md) **cbasedispatch** zum Implementieren von [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) bzw. [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition).</span><span class="sxs-lookup"><span data-stu-id="9d624-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="9d624-108">Aufgrund dieser Einschränkung gibt es wahrscheinlich keinen Grund, **cbasedispatch** direkt in ihren eigenen Filtern zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d624-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="9d624-109">Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="9d624-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="9d624-110">Deklarieren Sie eine neue Klasse, die **IDispatch** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d624-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="9d624-111">Geben Sie der neuen Klasse eine private Member-Variable vom Typ **cbasedispatch**.</span><span class="sxs-lookup"><span data-stu-id="9d624-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="9d624-112">Implementieren Sie die **IDispatch** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d624-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="9d624-113">Nennen Sie in Ihren **IDispatch** -Methoden die **cbasedispatch** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d624-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="9d624-114">Weitere Informationen finden Sie im Quellcode für eine der in ctlutil. h deklarierten Beispiel Klassen.</span><span class="sxs-lookup"><span data-stu-id="9d624-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="9d624-115">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="9d624-115">Public Methods</span></span>                                             | <span data-ttu-id="9d624-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d624-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d624-117">**Cbasedispatch**</span><span class="sxs-lookup"><span data-stu-id="9d624-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="9d624-118">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="9d624-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="9d624-119">**~ Cbasedispatch**</span><span class="sxs-lookup"><span data-stu-id="9d624-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="9d624-120">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="9d624-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="9d624-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="9d624-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="9d624-122">Ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.</span><span class="sxs-lookup"><span data-stu-id="9d624-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="9d624-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="9d624-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="9d624-124">Ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9d624-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="9d624-125">**Gettypeingefocount**</span><span class="sxs-lookup"><span data-stu-id="9d624-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="9d624-126">Ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9d624-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="9d624-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d624-127">Requirements</span></span>



| <span data-ttu-id="9d624-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d624-128">Requirement</span></span> | <span data-ttu-id="9d624-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9d624-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d624-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d624-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9d624-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d624-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d624-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d624-132">Library</span></span><br/> | <dl> <span data-ttu-id="9d624-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d624-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d624-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d624-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d624-135">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="9d624-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 





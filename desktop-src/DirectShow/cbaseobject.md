---
description: Die cbaseobject-Klasse ist eine abstrakte Klasse für die Implementierung von DirectShow-Objekten. Um Component Object Model (com)-Objekte zu implementieren, verwenden Sie die cunknown-Klasse, die von cbaseobject abgeleitet wird.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Cbaseobject-Klasse (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358324"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="4a296-104">Cbaseobject-Klasse</span><span class="sxs-lookup"><span data-stu-id="4a296-104">CBaseObject class</span></span>

<span data-ttu-id="4a296-105">Die **cbaseobject** -Klasse ist eine abstrakte Klasse für die Implementierung von DirectShow-Objekten.</span><span class="sxs-lookup"><span data-stu-id="4a296-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="4a296-106">Um Component Object Model (com)-Objekte zu implementieren, verwenden Sie die [**cunknown**](cunknown.md) -Klasse, die von **cbaseobject** abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4a296-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="4a296-107">Klassen Methoden</span><span class="sxs-lookup"><span data-stu-id="4a296-107">Class Methods</span></span>                                      | <span data-ttu-id="4a296-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a296-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="4a296-109">**Cbaseobject**</span><span class="sxs-lookup"><span data-stu-id="4a296-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="4a296-110">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4a296-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="4a296-111">**~ Cbaseobject**</span><span class="sxs-lookup"><span data-stu-id="4a296-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="4a296-112">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4a296-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="4a296-113">**Objectatactive**</span><span class="sxs-lookup"><span data-stu-id="4a296-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="4a296-114">Ruft die Anzahl der aktiven-Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="4a296-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4a296-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a296-115">Remarks</span></span>

<span data-ttu-id="4a296-116">Die meisten DirectShow-Basisklassen werden von **cbaseobject** abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4a296-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="4a296-117">Diese Klasse stellt Debuggingunterstützung bereit, indem die Anzahl der während der Laufzeit aktiven DirectShow-Objekte beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4a296-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="4a296-118">Die Objekt Anzahl wird in einer klassenstatischen Element Variablen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="4a296-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="4a296-119">In Debugbuilds bestätigt die dll, dass Sie entladen wird, während die Objekt Anzahl größer als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="4a296-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="4a296-120">Dies erleichtert das Ermitteln von Verlusten aufgrund von Problemen bei der Verweis Zählung.</span><span class="sxs-lookup"><span data-stu-id="4a296-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="4a296-121">Der **cbaseobject** -Konstruktor benötigt ein Argument, einen debugnamen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a296-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="4a296-122">Dieser Name wird in einer globalen Tabelle in der dll gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a296-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="4a296-123">Die Funktion [**dbgdumpobjectregiester**](dbgdumpobjectregister.md) formatiert eine Liste der in der dll aktiven Objekte und sendet Sie an die Debugausgabe.</span><span class="sxs-lookup"><span data-stu-id="4a296-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a296-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a296-124">Requirements</span></span>



| <span data-ttu-id="4a296-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a296-125">Requirement</span></span> | <span data-ttu-id="4a296-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4a296-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a296-127">Header</span><span class="sxs-lookup"><span data-stu-id="4a296-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4a296-128"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a296-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a296-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a296-129">Library</span></span><br/> | <dl> <span data-ttu-id="4a296-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4a296-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a296-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a296-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a296-132">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="4a296-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 





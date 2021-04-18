---
description: Die cunknown-Klasse implementiert die IUnknown-Schnittstelle. Die meisten Component Object Model (com)-Objekte in DirectShow werden von cunknown abgeleitet.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Cunknown-Klasse (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354720"
---
# <a name="cunknown-class"></a><span data-ttu-id="e72f9-104">Cunknown-Klasse</span><span class="sxs-lookup"><span data-stu-id="e72f9-104">CUnknown class</span></span>

![cunknown-Klassenhierarchie](images/cbase01.png)

<span data-ttu-id="e72f9-106">Die **cunknown** -Klasse implementiert die **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e72f9-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="e72f9-107">Die meisten Component Object Model (com)-Objekte in DirectShow werden von **cunknown** abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e72f9-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="e72f9-108">Wenn Sie ein COM-Objekt implementieren, sollten Sie es ggf. von **cunknown** ableiten.</span><span class="sxs-lookup"><span data-stu-id="e72f9-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="e72f9-109">Die Ableitung von **cunknown** bietet eine Thread sichere Implementierung und erspart Ihnen das Implementieren von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e72f9-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="e72f9-110">Ausführliche Informationen zur Verwendung dieser Basisklasse finden Sie unter Gewusst wie: [Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e72f9-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="e72f9-111">Im folgenden finden Sie eine kurze Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="e72f9-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="e72f9-112">Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt Public der Klassendefinition ein.</span><span class="sxs-lookup"><span data-stu-id="e72f9-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="e72f9-113">Dieses Makro deklariert die drei Methoden der **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e72f9-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="e72f9-114">Überschreiben Sie die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode, um andere Schnittstellen als **IUnknown** zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e72f9-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="e72f9-115">Rufen Sie in dieser Methode die [**GetInterface**](getinterface.md) -Funktion zum Abrufen von Schnittstellen Zeigern auf.</span><span class="sxs-lookup"><span data-stu-id="e72f9-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="e72f9-116">Rufen Sie in Ihrem Klassenkonstruktor die **cunknown** -Konstruktormethode auf.</span><span class="sxs-lookup"><span data-stu-id="e72f9-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="e72f9-117">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="e72f9-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="e72f9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e72f9-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="e72f9-119">**m- \_ kref**</span><span class="sxs-lookup"><span data-stu-id="e72f9-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="e72f9-120">Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e72f9-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="e72f9-121">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="e72f9-121">Public Methods</span></span>                                                              | <span data-ttu-id="e72f9-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e72f9-122">Description</span></span>                                                        |
| [<span data-ttu-id="e72f9-123">**Cunknown**</span><span class="sxs-lookup"><span data-stu-id="e72f9-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="e72f9-124">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e72f9-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="e72f9-125">**~ Cunknown**</span><span class="sxs-lookup"><span data-stu-id="e72f9-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="e72f9-126">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e72f9-126">Destructor method.</span></span> <span data-ttu-id="e72f9-127">Virtu.</span><span class="sxs-lookup"><span data-stu-id="e72f9-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="e72f9-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="e72f9-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="e72f9-129">Ruft einen Zeiger auf das steuernde **IUnknown**-Element ab.</span><span class="sxs-lookup"><span data-stu-id="e72f9-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="e72f9-130">Inondelegatingunknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="e72f9-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="e72f9-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e72f9-131">Description</span></span>                                                        |
| [<span data-ttu-id="e72f9-132">**Nondelegatingadressf**</span><span class="sxs-lookup"><span data-stu-id="e72f9-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="e72f9-133">Erhöht den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e72f9-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="e72f9-134">**Nondelegatingqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="e72f9-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="e72f9-135">Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e72f9-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="e72f9-136">**Nondelegatingrelease**</span><span class="sxs-lookup"><span data-stu-id="e72f9-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="e72f9-137">Verringert den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e72f9-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="e72f9-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e72f9-138">Requirements</span></span>



| <span data-ttu-id="e72f9-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e72f9-139">Requirement</span></span> | <span data-ttu-id="e72f9-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e72f9-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e72f9-141">Header</span><span class="sxs-lookup"><span data-stu-id="e72f9-141">Header</span></span><br/>  | <dl> <span data-ttu-id="e72f9-142"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e72f9-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e72f9-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e72f9-143">Library</span></span><br/> | <dl> <span data-ttu-id="e72f9-144">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e72f9-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e72f9-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e72f9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72f9-146">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="e72f9-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 





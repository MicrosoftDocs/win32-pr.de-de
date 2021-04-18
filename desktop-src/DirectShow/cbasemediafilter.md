---
description: Die cbasemediafilter-Klasse implementiert die imediafilter-Schnittstelle.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Cbasemediafilter-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357611"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="8b92a-103">Cbasemediafilter-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b92a-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="8b92a-105">Die- `CBaseMediaFilter` Klasse implementiert die [**imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8b92a-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="8b92a-106">Verwenden Sie diese Klasse für Plug-in-Verteiler oder andere Objekte, die **imediafilter** unterstützen müssen, ohne die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b92a-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="8b92a-107">Verwenden Sie diese Klasse nicht für Filter.</span><span class="sxs-lookup"><span data-stu-id="8b92a-107">Do not use this class for filters.</span></span> <span data-ttu-id="8b92a-108">Verwenden Sie stattdessen die [**cbasefilter**](cbasefilter.md) -Klasse oder eine Basisklasse, die von **cbasefilter** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="8b92a-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="8b92a-109">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="8b92a-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="8b92a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b92a-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="8b92a-111">**m- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="8b92a-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="8b92a-112">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b92a-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="8b92a-113">**m \_ pclock**</span><span class="sxs-lookup"><span data-stu-id="8b92a-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="8b92a-114">Zeiger auf die verweisuhr des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b92a-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="8b92a-115">**m \_ tSTART**</span><span class="sxs-lookup"><span data-stu-id="8b92a-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="8b92a-116">Die Verweis Zeit, die der streamzeit 0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b92a-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="8b92a-117">**m \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="8b92a-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="8b92a-118">Klassen Bezeichner (CLSID) des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b92a-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="8b92a-119">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="8b92a-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="8b92a-120">Zeiger auf einen kritischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="8b92a-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="8b92a-121">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="8b92a-121">Public Methods</span></span>                                                   | <span data-ttu-id="8b92a-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b92a-122">Description</span></span>                                                  |
| [<span data-ttu-id="8b92a-123">**Cbasemediafilter**</span><span class="sxs-lookup"><span data-stu-id="8b92a-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="8b92a-124">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8b92a-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="8b92a-125">**~ Cbasemediafilter**</span><span class="sxs-lookup"><span data-stu-id="8b92a-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="8b92a-126">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8b92a-126">Destructor method.</span></span> <span data-ttu-id="8b92a-127">Virtu.</span><span class="sxs-lookup"><span data-stu-id="8b92a-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="8b92a-128">**Streamtime**</span><span class="sxs-lookup"><span data-stu-id="8b92a-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="8b92a-129">Ruft die aktuelle streamzeit ab.</span><span class="sxs-lookup"><span data-stu-id="8b92a-129">Retrieves the current stream time.</span></span> <span data-ttu-id="8b92a-130">Virtu.</span><span class="sxs-lookup"><span data-stu-id="8b92a-130">Virtual.</span></span>                  |
| [<span data-ttu-id="8b92a-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="8b92a-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="8b92a-132">Bestimmt, ob das Objekt aktiv ist (wird ausgeführt oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="8b92a-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="8b92a-133">Ipersistent-Methoden</span><span class="sxs-lookup"><span data-stu-id="8b92a-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="8b92a-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b92a-134">Description</span></span>                                                  |
| [<span data-ttu-id="8b92a-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="8b92a-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="8b92a-136">Ruft den Klassen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="8b92a-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="8b92a-137">Imediafilter-Methoden</span><span class="sxs-lookup"><span data-stu-id="8b92a-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="8b92a-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b92a-138">Description</span></span>                                                  |
| [<span data-ttu-id="8b92a-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="8b92a-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="8b92a-140">Ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="8b92a-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="8b92a-141">**Setsyncsource**</span><span class="sxs-lookup"><span data-stu-id="8b92a-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="8b92a-142">Legt eine Referenzuhr für das-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="8b92a-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="8b92a-143">**Getsyncsource**</span><span class="sxs-lookup"><span data-stu-id="8b92a-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="8b92a-144">Ruft die vom-Objekt verwendete Referenzuhr ab.</span><span class="sxs-lookup"><span data-stu-id="8b92a-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="8b92a-145">**Stop**</span><span class="sxs-lookup"><span data-stu-id="8b92a-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="8b92a-146">Beendet das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b92a-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="8b92a-147">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="8b92a-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="8b92a-148">Hält das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8b92a-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="8b92a-149">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="8b92a-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="8b92a-150">Führt das-Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="8b92a-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="8b92a-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b92a-151">Requirements</span></span>



| <span data-ttu-id="8b92a-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b92a-152">Requirement</span></span> | <span data-ttu-id="8b92a-153">Wert</span><span class="sxs-lookup"><span data-stu-id="8b92a-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b92a-154">Header</span><span class="sxs-lookup"><span data-stu-id="8b92a-154">Header</span></span><br/>  | <dl> <span data-ttu-id="8b92a-155"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b92a-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8b92a-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b92a-156">Library</span></span><br/> | <dl> <span data-ttu-id="8b92a-157">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8b92a-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





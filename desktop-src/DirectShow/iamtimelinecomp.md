---
description: Die iamtimelinecomp-Schnittstelle fügt virtuelle Spuren in einer Komposition in DirectShow-Bearbeitungs Diensten ein bzw. ruft Sie ab. Eine Komposition ist eine Auflistung von Ebenen, die als einzelner, zusammengesetzter Track fungiert.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Iamtimelinecomp-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365843"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="8b227-103">Iamtimelinecomp-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8b227-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="8b227-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8b227-104">\[Deprecated.</span></span> <span data-ttu-id="8b227-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8b227-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8b227-106">Die **iamtimelinecomp** -Schnittstelle fügt virtuelle Spuren in einer Komposition in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) ein bzw. ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="8b227-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="8b227-107">Eine Komposition ist eine Auflistung von Ebenen, die als einzelner, zusammengesetzter *Track* fungiert. Beispielsweise fungiert eine Komposition, die zwei Spuren mit einem Übergang zwischen Ihnen enthält, als einzelner Track mit dem vorab zusammengesetzten Übergang.</span><span class="sxs-lookup"><span data-stu-id="8b227-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="8b227-108">Eine Komposition sollte nur Medien mit einem Typ enthalten (z. b. Audiodaten oder Videos), aber diese Einschränkung wird nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="8b227-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="8b227-109">Ein *virtueller Titel* ist ein beliebiges Objekt, das sich in einer Komposition befinden kann, einschließlich Spuren und anderen Kompositionen.</span><span class="sxs-lookup"><span data-stu-id="8b227-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="8b227-110">Die obersten Knoten in der Zeitachse sind *Gruppen*.</span><span class="sxs-lookup"><span data-stu-id="8b227-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="8b227-111">Gruppen implementieren sowohl die `IAMTimelineComp` -Schnittstelle als auch die [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8b227-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="8b227-112">Um ein Kompositions Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline- \_ \_ Haupttyp \_ Composite auf.</span><span class="sxs-lookup"><span data-stu-id="8b227-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="8b227-113">Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineComp` Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8b227-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="8b227-114">Weitere Informationen finden Sie [unter Zeitachsen Modell](the-timeline-model.md) und [Erstellen einer Zeitachse](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="8b227-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="8b227-115">Member</span><span class="sxs-lookup"><span data-stu-id="8b227-115">Members</span></span>

<span data-ttu-id="8b227-116">Die **iamtimelinecomp** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8b227-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b227-117">**Iamtimelinecomp** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b227-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="8b227-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b227-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b227-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b227-119">Methods</span></span>

<span data-ttu-id="8b227-120">Die **iamtimelinecomp** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8b227-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="8b227-121">Methode</span><span class="sxs-lookup"><span data-stu-id="8b227-121">Method</span></span>                                                                       | <span data-ttu-id="8b227-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b227-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b227-123">**Getgräfin Service Type**</span><span class="sxs-lookup"><span data-stu-id="8b227-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="8b227-124">Ruft rekursiv die Anzahl der Objekte eines angegebenen Typs ab, der in dieser Komposition und allen virtuellen Spuren enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8b227-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="8b227-125">**Getnextvtrack**</span><span class="sxs-lookup"><span data-stu-id="8b227-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="8b227-126">Ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.</span><span class="sxs-lookup"><span data-stu-id="8b227-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="8b227-127">**Getrecursivelayeroftype**</span><span class="sxs-lookup"><span data-stu-id="8b227-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="8b227-128">Führt eine tiefen erste Reihenfolge der virtuellen Spuren in dieser Komposition aus und ruft die *n*-te virtuelle Spur aus dieser Reihenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="8b227-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="8b227-129">**Getrecursivelayeroftypei**</span><span class="sxs-lookup"><span data-stu-id="8b227-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="8b227-130">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b227-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="8b227-131">**Getvtrack**</span><span class="sxs-lookup"><span data-stu-id="8b227-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="8b227-132">Ruft den virtuellen Track mit der angegebenen Priorität ab.</span><span class="sxs-lookup"><span data-stu-id="8b227-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8b227-133">**Vtrackgetcount**</span><span class="sxs-lookup"><span data-stu-id="8b227-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="8b227-134">Ruft die Anzahl der in der Komposition enthaltenen virtuellen Spuren ab.</span><span class="sxs-lookup"><span data-stu-id="8b227-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="8b227-135">**Vtrackinsbefore**</span><span class="sxs-lookup"><span data-stu-id="8b227-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="8b227-136">Fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.</span><span class="sxs-lookup"><span data-stu-id="8b227-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="8b227-137">**Vtracktauapprioritäten**</span><span class="sxs-lookup"><span data-stu-id="8b227-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="8b227-138">Schaltet die Prioritäts Ebenen von zwei Spuren um.</span><span class="sxs-lookup"><span data-stu-id="8b227-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8b227-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b227-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b227-140">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8b227-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8b227-141">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8b227-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8b227-142">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b227-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b227-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b227-143">Requirements</span></span>



| <span data-ttu-id="8b227-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b227-144">Requirement</span></span> | <span data-ttu-id="8b227-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8b227-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b227-146">Header</span><span class="sxs-lookup"><span data-stu-id="8b227-146">Header</span></span><br/>  | <dl> <span data-ttu-id="8b227-147"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8b227-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8b227-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b227-148">Library</span></span><br/> | <dl> <span data-ttu-id="8b227-149"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="8b227-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 

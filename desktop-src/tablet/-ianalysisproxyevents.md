---
description: Gibt Ereignisse an, die den Daten Proxy Schritten eines iinkanalyzer-Objekts zugeordnet sind.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: _IAnalysisProxyEvents-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350598"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="9ef37-103">\_Ianalysisproxyevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ef37-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="9ef37-104">Gibt Ereignisse an, die den Daten Proxy Schritten eines [**iinkanalyzer**](iinkanalyzer.md) -Objekts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ef37-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="9ef37-105">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9ef37-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="9ef37-106">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9ef37-106">Events</span></span>

<span data-ttu-id="9ef37-107">Die **\_ ianalysisproxyevents** -Schnittstelle enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9ef37-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="9ef37-108">Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ef37-108">Event</span></span>                                                                                      | <span data-ttu-id="9ef37-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ef37-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ef37-110">**ContextNode created**</span><span class="sxs-lookup"><span data-stu-id="9ef37-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="9ef37-111">Tritt auf, nachdem [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextnode**](icontextnode.md) -Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="9ef37-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="9ef37-112">**Contextnodebug**</span><span class="sxs-lookup"><span data-stu-id="9ef37-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="9ef37-113">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt löscht.</span><span class="sxs-lookup"><span data-stu-id="9ef37-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="9ef37-114">**Contextnodelta inkadditions**</span><span class="sxs-lookup"><span data-stu-id="9ef37-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="9ef37-115">Tritt auf, bevor [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9ef37-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="9ef37-116">**Contextnodelinklösch**</span><span class="sxs-lookup"><span data-stu-id="9ef37-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="9ef37-117">Tritt auf, bevor [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten löscht.</span><span class="sxs-lookup"><span data-stu-id="9ef37-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="9ef37-118">**ContextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="9ef37-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="9ef37-119">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.</span><span class="sxs-lookup"><span data-stu-id="9ef37-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="9ef37-120">**Contextnodebug propertiesaktualisierten**</span><span class="sxs-lookup"><span data-stu-id="9ef37-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="9ef37-121">Tritt auf, nachdem der [**iinkanalyzer**](iinkanalyzer.md) eine oder mehrere Eigenschaften eines [**icontextnode**](icontextnode.md) -Objekts aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="9ef37-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="9ef37-122">**Contextnodereenting**</span><span class="sxs-lookup"><span data-stu-id="9ef37-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="9ef37-123">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) [**-Objekt durch**](icontextnode.md) Ändern des übergeordneten Knotens verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="9ef37-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="9ef37-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="9ef37-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="9ef37-125">Tritt auf, bevor die Analyseergebnisse von [**iinkanalyzer**](iinkanalyzer.md) so synchronisiert werden, dass eine Anwendung Daten mit dem **iinkanalyzer** synchronisieren kann.</span><span class="sxs-lookup"><span data-stu-id="9ef37-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="9ef37-126">**PopulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="9ef37-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="9ef37-127">Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) innerhalb des Bereichs eines teilweise aufgefüllten [**icontextnode**](icontextnode.md) -Objekts eine Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="9ef37-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="9ef37-128">**Strokereüber geordnet**</span><span class="sxs-lookup"><span data-stu-id="9ef37-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="9ef37-129">Tritt auf, wenn der [**iinkanalyzer**](iinkanalyzer.md) einen Strich von einem [**icontextnode**](icontextnode.md) -Objekt zu einem anderen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="9ef37-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="9ef37-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ef37-130">Remarks</span></span>

<span data-ttu-id="9ef37-131">Verwenden Sie diese Ereignisse, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ef37-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="9ef37-132">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit **iinkanalyzer** finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9ef37-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef37-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ef37-133">Requirements</span></span>



| <span data-ttu-id="9ef37-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ef37-134">Requirement</span></span> | <span data-ttu-id="9ef37-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9ef37-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef37-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ef37-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef37-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ef37-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9ef37-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ef37-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef37-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ef37-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9ef37-140">Header</span><span class="sxs-lookup"><span data-stu-id="9ef37-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef37-141"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef37-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9ef37-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9ef37-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ef37-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ef37-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9ef37-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ef37-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef37-145">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="9ef37-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9ef37-146">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="9ef37-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9ef37-147">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="9ef37-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="9ef37-148">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="9ef37-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="9ef37-149">\_Ianalysil Vents</span><span class="sxs-lookup"><span data-stu-id="9ef37-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="9ef37-150">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="9ef37-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


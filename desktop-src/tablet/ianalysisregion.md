---
description: Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Ianalysisregion-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751857"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="1790d-103">Ianalysisregion-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1790d-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="1790d-104">Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="1790d-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="1790d-105">Member</span><span class="sxs-lookup"><span data-stu-id="1790d-105">Members</span></span>

<span data-ttu-id="1790d-106">Die **ianalysisregion** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1790d-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1790d-107">**Ianalysisregion** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1790d-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="1790d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1790d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1790d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1790d-109">Methods</span></span>

<span data-ttu-id="1790d-110">Die **ianalysisregion** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1790d-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="1790d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1790d-111">Method</span></span>                                                           | <span data-ttu-id="1790d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1790d-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1790d-113">**Klon**</span><span class="sxs-lookup"><span data-stu-id="1790d-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="1790d-114">Erstellt eine Kopie von **ianalysisregion**.</span><span class="sxs-lookup"><span data-stu-id="1790d-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="1790d-115">**Excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="1790d-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="1790d-116">Schränkt den Bereich von **ianalysisregion** auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.</span><span class="sxs-lookup"><span data-stu-id="1790d-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="1790d-117">**Excluderegion**</span><span class="sxs-lookup"><span data-stu-id="1790d-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="1790d-118">Schränkt den Bereich von **ianalysisregion** auf den Teil des Bereichs ein, der den angegebenen **ianalysisregion** nicht überschneidet.</span><span class="sxs-lookup"><span data-stu-id="1790d-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="1790d-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="1790d-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="1790d-120">Ruft das umgebende Rechteck von **ianalysisregion** ab.</span><span class="sxs-lookup"><span data-stu-id="1790d-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="1790d-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="1790d-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="1790d-122">Ruft ein Array von Rechtecke ab, das den Bereich von **ianalysisregion** definiert.</span><span class="sxs-lookup"><span data-stu-id="1790d-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="1790d-123">**Intersectrechteck**</span><span class="sxs-lookup"><span data-stu-id="1790d-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="1790d-124">Schränkt den Bereich dieses **ianalysisregion** auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1790d-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="1790d-125">**Intersectregion**</span><span class="sxs-lookup"><span data-stu-id="1790d-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="1790d-126">Schränkt den Bereich von **ianalysisregion** auf den Bereich ein, der durch die Schnittmenge mit der angegebenen **ianalysisregion** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1790d-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="1790d-127">**Intersecin**</span><span class="sxs-lookup"><span data-stu-id="1790d-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="1790d-128">Bestimmt, ob sich der Bereich des **ianalysisregion** mit dem angegebenen Rechteck überschneidet.</span><span class="sxs-lookup"><span data-stu-id="1790d-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="1790d-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="1790d-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="1790d-130">Ruft einen Wert ab, der angibt, ob **ianalysisregion** einen leeren Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="1790d-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="1790d-131">**IsInfinite**</span><span class="sxs-lookup"><span data-stu-id="1790d-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="1790d-132">Ruft einen Wert ab, der angibt, ob **ianalysisregion** einen unendlichen Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="1790d-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="1790d-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="1790d-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="1790d-134">Reduziert den **ianalysisregion** -Element, um einen leeren Bereich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="1790d-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="1790d-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="1790d-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="1790d-136">Erweitert **ianalysisregion** , um einen unendlichen Bereich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="1790d-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="1790d-137">**Unionrechteck**</span><span class="sxs-lookup"><span data-stu-id="1790d-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="1790d-138">Erweitert den Bereich dieses **ianalysisregion** auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1790d-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="1790d-139">**Unionregion**</span><span class="sxs-lookup"><span data-stu-id="1790d-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="1790d-140">Erweitert den Bereich dieses **ianalysisregion** auf den Bereich, der von seiner Union mit dem angegebenen **ianalysisregion** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1790d-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="1790d-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1790d-141">Remarks</span></span>

<span data-ttu-id="1790d-142">Diese Schnittstelle stellt einen Bereich dar, der aus rechteckigen Bereichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1790d-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="1790d-143">Der [**iinkanalyzer**](iinkanalyzer.md) gibt die Koordinaten eines Bereichs innerhalb des Koordinaten Bereichs zurück, in dem er Strich Daten empfängt, oder interpretiert ihn.</span><span class="sxs-lookup"><span data-stu-id="1790d-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="1790d-144">Verwenden Sie die [**ianalysisregion:: GetBounds-Methode**](ianalysisregion-getbounds.md) oder die [**ianalysisregion:: GetRegionScans-Methode**](ianalysisregion-getregionscans.md), um die aktuellen Begrenzungen von **ianalysisregion** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1790d-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="1790d-145">Verwenden Sie die folgenden Methoden, um den Bereich einer vorhandenen **ianalysisregion** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1790d-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="1790d-146">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="1790d-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="1790d-147">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="1790d-148">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="1790d-149">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="1790d-150">**Ianalysisregion:: MakeEmpty-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="1790d-151">**Ianalysisregion:: MakeInfinite-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="1790d-152">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="1790d-153">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="1790d-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="1790d-154">Diese Schnittstelle entspricht der Klasse System. Windows. Ink. AnalysisCore. AnalysisRegionBase in der .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1790d-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="1790d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1790d-155">Requirements</span></span>



| <span data-ttu-id="1790d-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1790d-156">Requirement</span></span> | <span data-ttu-id="1790d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="1790d-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1790d-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1790d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="1790d-159">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1790d-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1790d-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1790d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="1790d-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1790d-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1790d-162">Header</span><span class="sxs-lookup"><span data-stu-id="1790d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="1790d-163"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1790d-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1790d-164">DLL</span><span class="sxs-lookup"><span data-stu-id="1790d-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1790d-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1790d-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1790d-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1790d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1790d-167">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="1790d-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1790d-168">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="1790d-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


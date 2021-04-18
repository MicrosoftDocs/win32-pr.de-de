---
description: Ändert den Typ der angegebenen Striche.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Iinkanalyzer:: SetStrokesType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344457"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="64027-103">Iinkanalyzer:: SetStrokesType-Methode</span><span class="sxs-lookup"><span data-stu-id="64027-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="64027-104">Ändert den Typ der angegebenen Striche.</span><span class="sxs-lookup"><span data-stu-id="64027-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="64027-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64027-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="64027-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64027-107">*strokeidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64027-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64027-108">Die Anzahl der Stroke-IDs in *plstrokes*.</span><span class="sxs-lookup"><span data-stu-id="64027-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="64027-109">*pltakte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64027-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64027-110">Ein Array, das die Strich Bezeichner der Striche enthält, denen *StrokeType* zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64027-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="64027-111">*StrokeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64027-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64027-112">Der [**StrokeType**](stroketype.md) -Wert, der den Strichen zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64027-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64027-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64027-113">Return value</span></span>

<span data-ttu-id="64027-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="64027-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64027-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64027-115">Remarks</span></span>

<span data-ttu-id="64027-116">Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert **\_ nicht klassifiziert** ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse.</span><span class="sxs-lookup"><span data-stu-id="64027-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="64027-117">Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64027-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="64027-118">Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64027-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="64027-119">Verwenden Sie die [**iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die **iinkanalyzer:: SetStrokesType-Methode**, um den strichentyp anzugeben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="64027-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="64027-120">Wenn ein Strich einem [**icontextnode**](icontextnode.md) zugeordnet ist, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), verschiebt diese Methode den Strich auf einen nicht klassifizierten Ink-Knoten, der Striche derselben Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="64027-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="64027-121">Wenn kein solcher Kontext Knoten vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und fügt diesen dem Strich hinzu.</span><span class="sxs-lookup"><span data-stu-id="64027-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="64027-122">Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** , der vom Typ unclassimeedink ist.</span><span class="sxs-lookup"><span data-stu-id="64027-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="64027-123">Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="64027-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="64027-124">Diese Methode verschiebt keinen Strich, wenn der *StrokeType* -Parameter mit dem aktuellen Typ des Strichs übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="64027-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="64027-125">Wenn ein in *strokeIds* identifizierter Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="64027-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="64027-126">Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="64027-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="64027-127">Beim Festlegen des Strich Typs für Striche, die einem ContextNode zugeordnet sind, für das NodeTypeAndProperties bestätigt ist, wird eine InvalidOperationException ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="64027-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="64027-128">Diese Methode gibt einen Fehlercode zurück, wenn *plstrokes* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="64027-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="64027-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64027-129">Requirements</span></span>



| <span data-ttu-id="64027-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64027-130">Requirement</span></span> | <span data-ttu-id="64027-131">Wert</span><span class="sxs-lookup"><span data-stu-id="64027-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64027-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64027-132">Minimum supported client</span></span><br/> | <span data-ttu-id="64027-133">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64027-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64027-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64027-134">Minimum supported server</span></span><br/> | <span data-ttu-id="64027-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="64027-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="64027-136">Header</span><span class="sxs-lookup"><span data-stu-id="64027-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="64027-137"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64027-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64027-138">DLL</span><span class="sxs-lookup"><span data-stu-id="64027-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64027-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64027-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="64027-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64027-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64027-141">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="64027-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="64027-142">**Iinkanalyzer:: GetStrokeType-Methode**</span><span class="sxs-lookup"><span data-stu-id="64027-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="64027-143">**Iinkanalyzer:: SetStrokeType-Methode**</span><span class="sxs-lookup"><span data-stu-id="64027-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="64027-144">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="64027-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





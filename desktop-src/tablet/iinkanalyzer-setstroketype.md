---
description: Ändert den Typ des angegebenen Strichs.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'Iinkanalyzer:: SetStrokeType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129436"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="cf031-103">Iinkanalyzer:: SetStrokeType-Methode</span><span class="sxs-lookup"><span data-stu-id="cf031-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="cf031-104">Ändert den Typ des angegebenen Strichs.</span><span class="sxs-lookup"><span data-stu-id="cf031-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf031-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf031-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="cf031-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf031-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf031-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf031-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf031-108">Der Strich Bezeichner des Strichs, dem *StrokeType* zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf031-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="cf031-109">*StrokeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf031-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf031-110">Der [**StrokeType**](stroketype.md) -Wert, der dem Strich zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf031-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf031-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf031-111">Return value</span></span>

<span data-ttu-id="cf031-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf031-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf031-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf031-113">Remarks</span></span>

<span data-ttu-id="cf031-114">Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert **\_ nicht klassifiziert** ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse.</span><span class="sxs-lookup"><span data-stu-id="cf031-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="cf031-115">Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cf031-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="cf031-116">Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf031-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="cf031-117">Verwenden Sie die **iinkanalyzer:: SetStrokeType-Methode** oder die [**iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md), um den strichentyp anzugeben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cf031-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="cf031-118">Wenn ein Strich einem [**icontextnode**](icontextnode.md) zugeordnet ist, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), verschiebt diese Methode den Strich auf einen nicht klassifizierten Ink-Knoten, der Striche derselben Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="cf031-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="cf031-119">Wenn kein solcher Kontext Knoten vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und fügt diesen dem Strich hinzu.</span><span class="sxs-lookup"><span data-stu-id="cf031-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="cf031-120">Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** , der vom Typ unclassimeedink ist.</span><span class="sxs-lookup"><span data-stu-id="cf031-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="cf031-121">Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="cf031-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="cf031-122">Diese Methode verschiebt keinen Strich, wenn der *StrokeType* -Parameter mit dem aktuellen Typ des Strichs übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cf031-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="cf031-123">Beim Festlegen des Strich Typs für Striche, die einem ContextNode zugeordnet sind, für das NodeTypeAndProperties bestätigt ist, wird eine InvalidOperationException ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cf031-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="cf031-124">Wenn der angegebene Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cf031-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf031-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf031-125">Requirements</span></span>



| <span data-ttu-id="cf031-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf031-126">Requirement</span></span> | <span data-ttu-id="cf031-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cf031-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf031-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf031-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf031-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf031-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf031-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf031-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf031-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cf031-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cf031-132">Header</span><span class="sxs-lookup"><span data-stu-id="cf031-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf031-133"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cf031-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf031-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cf031-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf031-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf031-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cf031-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf031-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf031-137">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="cf031-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cf031-138">**Iinkanalyzer:: GetStrokeType-Methode**</span><span class="sxs-lookup"><span data-stu-id="cf031-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="cf031-139">**Iinkanalyzer:: SetStrokesType-Methode**</span><span class="sxs-lookup"><span data-stu-id="cf031-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="cf031-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="cf031-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





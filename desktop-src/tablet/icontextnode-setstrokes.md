---
description: Ordnet diesem icontextnode die angegebenen Striche zu.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Icontextnode:: setstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347197"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="4ed66-103">Icontextnode:: setstrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="4ed66-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="4ed66-104">Ordnet diesem [**icontextnode**](icontextnode.md)die angegebenen Striche zu.</span><span class="sxs-lookup"><span data-stu-id="4ed66-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ed66-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="4ed66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ed66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed66-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ed66-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed66-108">Die Anzahl der Stroke-IDs in *plstrokeids*.</span><span class="sxs-lookup"><span data-stu-id="4ed66-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="4ed66-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ed66-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed66-110">Die Bezeichner der Striche, die diesem [**icontextnode**](icontextnode.md)zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ed66-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ed66-111">Return value</span></span>

<span data-ttu-id="4ed66-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4ed66-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed66-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ed66-113">Remarks</span></span>

<span data-ttu-id="4ed66-114">Mit dieser Methode wird der geänderte Bereich der Ink Analyzer nicht aktualisiert (Weitere Informationen finden Sie unter [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="4ed66-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="4ed66-115">Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4ed66-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="4ed66-116">Verwenden Sie diese Methode, um einem bestimmten Kontext Knoten hubdaten zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="4ed66-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="4ed66-117">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit **iinkanalyzer** finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4ed66-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="4ed66-118">Wenn einer der angegebenen Striche bereits mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ed66-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed66-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ed66-119">Requirements</span></span>



| <span data-ttu-id="4ed66-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ed66-120">Requirement</span></span> | <span data-ttu-id="4ed66-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4ed66-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed66-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ed66-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed66-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ed66-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ed66-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ed66-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed66-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4ed66-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4ed66-126">Header</span><span class="sxs-lookup"><span data-stu-id="4ed66-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed66-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed66-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4ed66-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed66-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ed66-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ed66-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4ed66-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ed66-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed66-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4ed66-132">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="4ed66-133">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="4ed66-134">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="4ed66-135">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="4ed66-136">**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4ed66-137">**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4ed66-138">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="4ed66-139">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="4ed66-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="4ed66-140">**Icontextnode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="4ed66-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="4ed66-141">**Icontextnode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="4ed66-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="4ed66-142">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4ed66-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





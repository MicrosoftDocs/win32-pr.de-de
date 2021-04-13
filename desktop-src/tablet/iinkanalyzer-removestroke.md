---
description: Entfernt den angegebenen Strich aus iinkanalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Iinkanalyzer:: RemoveStroke-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526486"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="53c11-103">Iinkanalyzer:: RemoveStroke-Methode</span><span class="sxs-lookup"><span data-stu-id="53c11-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="53c11-104">Entfernt den angegebenen Strich aus [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="53c11-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="53c11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c11-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="53c11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c11-107">*plstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53c11-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53c11-108">Der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="53c11-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c11-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53c11-109">Return value</span></span>

<span data-ttu-id="53c11-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="53c11-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="53c11-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53c11-111">Remarks</span></span>

<span data-ttu-id="53c11-112">Diese Methode entfernt die Paketdaten für den angegebenen Strich und verweist auf den angegebenen Strich aus dem [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="53c11-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="53c11-113">Mit dieser Methode wird der Strich aus dem Blatt Kontext Knoten entfernt, der auf den Strich verweist.</span><span class="sxs-lookup"><span data-stu-id="53c11-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="53c11-114">Wenn der [**icontextnode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode den **icontextnode** -und alle Vorgänger- **icontextnode** -Objekte, die keine untergeordneten Knoten mehr aufweisen.</span><span class="sxs-lookup"><span data-stu-id="53c11-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="53c11-115">Nachdem diese Methode den Strich aus dem [**icontextnode**](icontextnode.md)entfernt hat, aktualisiert Sie den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), um das umgebende Feld des entfernten Strichs einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="53c11-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="53c11-116">Wenn *plstrokeid* keinen dem [**iinkanalyzer**](iinkanalyzer.md)zugeordneten Strich identifiziert, gibt diese Methode zurück, ohne den Ink Analyzer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="53c11-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c11-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53c11-117">Requirements</span></span>



| <span data-ttu-id="53c11-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53c11-118">Requirement</span></span> | <span data-ttu-id="53c11-119">Wert</span><span class="sxs-lookup"><span data-stu-id="53c11-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c11-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53c11-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53c11-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53c11-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53c11-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53c11-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53c11-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="53c11-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="53c11-124">Header</span><span class="sxs-lookup"><span data-stu-id="53c11-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c11-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="53c11-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="53c11-126">DLL</span><span class="sxs-lookup"><span data-stu-id="53c11-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53c11-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c11-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="53c11-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53c11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c11-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="53c11-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="53c11-130">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="53c11-131">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="53c11-132">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="53c11-133">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="53c11-134">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="53c11-135">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="53c11-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="53c11-136">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="53c11-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





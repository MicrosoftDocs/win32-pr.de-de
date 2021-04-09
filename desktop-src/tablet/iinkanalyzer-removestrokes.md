---
description: Entfernt die angegebenen Striche aus iinkanalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Iinkanalyzer:: RemoveStrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129449"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="78fd5-103">Iinkanalyzer:: RemoveStrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="78fd5-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="78fd5-104">Entfernt die angegebenen Striche aus [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="78fd5-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78fd5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fd5-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="78fd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fd5-107">*ulstrokeidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fd5-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fd5-108">Die Anzahl der Stroke-IDs in *plstrokes*.</span><span class="sxs-lookup"><span data-stu-id="78fd5-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="78fd5-109">*pltakte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fd5-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fd5-110">Die Bezeichner für die Striche, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="78fd5-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fd5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78fd5-111">Return value</span></span>

<span data-ttu-id="78fd5-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="78fd5-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78fd5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78fd5-113">Remarks</span></span>

<span data-ttu-id="78fd5-114">Diese Methode entfernt die Paketdaten für-und-Verweise auf die angegebenen Striche aus [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="78fd5-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="78fd5-115">Diese Methode entfernt die Striche aus dem Blatt Kontext Knoten, der auf die Striche verweist.</span><span class="sxs-lookup"><span data-stu-id="78fd5-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="78fd5-116">Wenn ein [**icontextnode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode den **icontextnode** -und alle Vorgänger- **icontextnode** -Objekte, die keine untergeordneten Knoten mehr aufweisen.</span><span class="sxs-lookup"><span data-stu-id="78fd5-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="78fd5-117">Nachdem diese Methode die Striche aus dem [**icontextnode**](icontextnode.md)entfernt hat, aktualisiert Sie den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), um das umgebende Feld der entfernten Striche einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="78fd5-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="78fd5-118">Wenn ein in *plstrokes* identifizierter Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="78fd5-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="78fd5-119">Wenn keiner der in *plstrokes* identifizierten Striche mit der Ink Analyzer verknüpft ist, gibt diese Methode zurück, ohne [**iinkanalyzer**](iinkanalyzer.md)zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="78fd5-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="78fd5-120">Diese Methode gibt den Fehlercode zurück, wenn *plstrokes* NULL ist.</span><span class="sxs-lookup"><span data-stu-id="78fd5-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="78fd5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78fd5-121">Requirements</span></span>



| <span data-ttu-id="78fd5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78fd5-122">Requirement</span></span> | <span data-ttu-id="78fd5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="78fd5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fd5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78fd5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78fd5-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78fd5-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78fd5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78fd5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78fd5-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="78fd5-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="78fd5-128">Header</span><span class="sxs-lookup"><span data-stu-id="78fd5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="78fd5-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78fd5-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78fd5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="78fd5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78fd5-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78fd5-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="78fd5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78fd5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fd5-133">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="78fd5-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="78fd5-134">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="78fd5-135">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="78fd5-136">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="78fd5-137">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="78fd5-138">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="78fd5-139">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="78fd5-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="78fd5-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="78fd5-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





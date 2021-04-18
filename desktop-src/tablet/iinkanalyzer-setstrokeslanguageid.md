---
description: Ändert den Gebiets Schema Bezeichner für die angegebenen Striche.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Iinkanalyzer:: SetStrokesLanguageId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345121"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="1862e-103">Iinkanalyzer:: SetStrokesLanguageId-Methode</span><span class="sxs-lookup"><span data-stu-id="1862e-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="1862e-104">Ändert den Gebiets Schema Bezeichner für die angegebenen Striche.</span><span class="sxs-lookup"><span data-stu-id="1862e-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1862e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1862e-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="1862e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1862e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1862e-107">*ulstrokeidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1862e-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1862e-108">Die Anzahl der Stroke-IDs in *plstrokes*.</span><span class="sxs-lookup"><span data-stu-id="1862e-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="1862e-109">*pltakte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1862e-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1862e-110">Das Array von Bezeichnern für die Striche, denen der Gebiets Schema Bezeichner zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1862e-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1862e-111">*lstrokeslcid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1862e-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1862e-112">Der Gebiets Schema Bezeichner, der den Strichen zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1862e-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1862e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1862e-113">Return value</span></span>

<span data-ttu-id="1862e-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1862e-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1862e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1862e-115">Remarks</span></span>

<span data-ttu-id="1862e-116">Das Gebiets Schema eines Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1862e-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="1862e-117">Um das Gebiets Schema abzurufen, das momentan einem Strich zugewiesen ist, müssen Sie die [**iinkanalyzer:: GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1862e-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="1862e-118">Die angegebenen Striche werden auf einen nicht klassifizierten frei Hand Knoten verschoben (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), der Striche derselben Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="1862e-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="1862e-119">Wenn kein solcher [**icontextnode**](icontextnode.md) vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und verschiebt die Striche darauf.</span><span class="sxs-lookup"><span data-stu-id="1862e-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="1862e-120">Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** mit dem Typ unclassimeedink.</span><span class="sxs-lookup"><span data-stu-id="1862e-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="1862e-121">Wenn diese Methode Striche von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch die Begrenzungs Felder der Striche in den geänderten Bereich der Ink Analyzer ein (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="1862e-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="1862e-122">Diese Methode verschiebt keinen Strich, wenn der *lstrokelcid* -Parameter mit dem aktuellen sprach Bezeichner des Strichs übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="1862e-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="1862e-123">Wenn ein angegebener Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1862e-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="1862e-124">Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1862e-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="1862e-125">Diese Methode gibt einen Fehlercode zurück, wenn strokeIds **null** ist.</span><span class="sxs-lookup"><span data-stu-id="1862e-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="1862e-126">Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="1862e-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="1862e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1862e-127">Requirements</span></span>



| <span data-ttu-id="1862e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1862e-128">Requirement</span></span> | <span data-ttu-id="1862e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1862e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1862e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1862e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1862e-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1862e-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1862e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1862e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1862e-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1862e-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1862e-134">Header</span><span class="sxs-lookup"><span data-stu-id="1862e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1862e-135"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1862e-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1862e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1862e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1862e-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1862e-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1862e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1862e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1862e-139">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="1862e-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1862e-140">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="1862e-141">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="1862e-142">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="1862e-143">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="1862e-144">**Iinkanalyzer:: GetStrokeLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="1862e-145">**Iinkanalyzer:: SetStrokeLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="1862e-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="1862e-146">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="1862e-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


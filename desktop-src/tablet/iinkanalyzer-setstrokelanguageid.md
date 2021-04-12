---
description: Ändert den Gebiets Schema Bezeichner für den angegebenen Strich.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Iinkanalyzer:: SetStrokeLanguageId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526474"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="8cf21-103">Iinkanalyzer:: SetStrokeLanguageId-Methode</span><span class="sxs-lookup"><span data-stu-id="8cf21-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="8cf21-104">Ändert den Gebiets Schema Bezeichner für den angegebenen Strich.</span><span class="sxs-lookup"><span data-stu-id="8cf21-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cf21-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="8cf21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cf21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf21-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cf21-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf21-108">Der Bezeichner des Strichs, dem der Gebiets Schema Bezeichner zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cf21-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8cf21-109">*lstrokelcid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cf21-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf21-110">Der Gebiets Schema Bezeichner, der dem Strich zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cf21-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf21-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cf21-111">Return value</span></span>

<span data-ttu-id="8cf21-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8cf21-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf21-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cf21-113">Remarks</span></span>

<span data-ttu-id="8cf21-114">Das Gebiets Schema eines Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8cf21-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="8cf21-115">Um das Gebiets Schema abzurufen, das momentan einem Strich zugewiesen ist, müssen Sie die [**iinkanalyzer:: GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cf21-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="8cf21-116">Der angegebene Strich wird in einen nicht klassifizierten frei Hand Knoten verschoben (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), der Striche derselben Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="8cf21-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="8cf21-117">Wenn kein solcher [**icontextnode**](icontextnode.md) vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und verschiebt den Strich darauf.</span><span class="sxs-lookup"><span data-stu-id="8cf21-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="8cf21-118">Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** mit dem Typ unclassimeedink.</span><span class="sxs-lookup"><span data-stu-id="8cf21-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="8cf21-119">Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="8cf21-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="8cf21-120">Diese Methode verschiebt keinen Strich, wenn der *lstrokelcid* -Parameter mit dem aktuellen sprach Bezeichner des Strichs übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8cf21-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="8cf21-121">Wenn der angegebene Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8cf21-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="8cf21-122">Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="8cf21-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf21-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf21-123">Requirements</span></span>



| <span data-ttu-id="8cf21-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cf21-124">Requirement</span></span> | <span data-ttu-id="8cf21-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf21-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf21-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cf21-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf21-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf21-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cf21-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cf21-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf21-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8cf21-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cf21-130">Header</span><span class="sxs-lookup"><span data-stu-id="8cf21-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf21-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8cf21-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cf21-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf21-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf21-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf21-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cf21-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cf21-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf21-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="8cf21-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8cf21-136">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="8cf21-137">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="8cf21-138">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="8cf21-139">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="8cf21-140">**Iinkanalyzer:: GetStrokeLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="8cf21-141">**Iinkanalyzer:: SetStrokesLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="8cf21-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="8cf21-142">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8cf21-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


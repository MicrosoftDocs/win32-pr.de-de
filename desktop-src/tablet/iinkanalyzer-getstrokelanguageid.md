---
description: Gibt den Gebiets Schema Bezeichner des angegebenen Strichs zurück.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Iinkanalyzer:: GetStrokeLanguageId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751801"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="4aee1-103">Iinkanalyzer:: GetStrokeLanguageId-Methode</span><span class="sxs-lookup"><span data-stu-id="4aee1-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="4aee1-104">Gibt den Gebiets Schema Bezeichner des angegebenen Strichs zurück.</span><span class="sxs-lookup"><span data-stu-id="4aee1-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aee1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aee1-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="4aee1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aee1-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4aee1-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aee1-108">Der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4aee1-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4aee1-109">*lstrokelcid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4aee1-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aee1-110">Der Gebiets Schema Bezeichner für den angegebenen Strich.</span><span class="sxs-lookup"><span data-stu-id="4aee1-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aee1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4aee1-111">Return value</span></span>

<span data-ttu-id="4aee1-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4aee1-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4aee1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aee1-113">Remarks</span></span>

<span data-ttu-id="4aee1-114">Das Gebiets Schema des Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4aee1-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="4aee1-115">Um das Gebiets Schema des Strichs zu ändern, verwenden Sie die [**iinkanalyzer:: SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md) oder die [**iinkanalyzer:: SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="4aee1-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aee1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aee1-116">Requirements</span></span>



| <span data-ttu-id="4aee1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aee1-117">Requirement</span></span> | <span data-ttu-id="4aee1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4aee1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aee1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aee1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4aee1-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aee1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4aee1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aee1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4aee1-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4aee1-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4aee1-123">Header</span><span class="sxs-lookup"><span data-stu-id="4aee1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aee1-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4aee1-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4aee1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4aee1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aee1-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aee1-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4aee1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aee1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aee1-128">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="4aee1-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4aee1-129">**Iinkanalyzer:: SetStrokeLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="4aee1-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="4aee1-130">**Iinkanalyzer:: SetStrokesLanguageId-Methode**</span><span class="sxs-lookup"><span data-stu-id="4aee1-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="4aee1-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4aee1-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





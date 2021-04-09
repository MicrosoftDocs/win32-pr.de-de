---
description: Ruft Analyse Alternativen für die Striche mit den angegebenen Strich bezeichaten ab.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Iinkanalyzer:: getalternatesforstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129457"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="e3406-103">Iinkanalyzer:: getalternatesforstrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="e3406-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="e3406-104">Ruft Analyse Alternativen für die Striche mit den angegebenen Strich bezeichaten ab.</span><span class="sxs-lookup"><span data-stu-id="e3406-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3406-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="e3406-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3406-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3406-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3406-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3406-108">Die Anzahl der Stroke-IDs in *plstrokes*.</span><span class="sxs-lookup"><span data-stu-id="e3406-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="e3406-109">*pltakte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3406-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3406-110">Das Array von Strich bezeichlern.</span><span class="sxs-lookup"><span data-stu-id="e3406-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="e3406-111">*ulmaximumalteraten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3406-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3406-112">Die maximale Anzahl der zurückgegebenen Analyse Alternativen.</span><span class="sxs-lookup"><span data-stu-id="e3406-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="e3406-113">*ppalternativen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e3406-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3406-114">Das [**ianalysisalterniert**](ianalysisalternates.md) -Objekt, das die Analyse Alternativen enthält.</span><span class="sxs-lookup"><span data-stu-id="e3406-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3406-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3406-115">Return value</span></span>

<span data-ttu-id="e3406-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e3406-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3406-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3406-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e3406-118">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e3406-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="e3406-119">Der oberste [**ianalysisalternate**](ianalysisalternate.md) wird als erste Alternative der Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3406-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="e3406-120">Die angegebenen Striche müssen keine angrenzenden Bereiche des Dokuments darstellen.</span><span class="sxs-lookup"><span data-stu-id="e3406-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3406-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3406-121">Requirements</span></span>



| <span data-ttu-id="e3406-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3406-122">Requirement</span></span> | <span data-ttu-id="e3406-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e3406-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3406-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3406-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3406-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3406-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e3406-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3406-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3406-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e3406-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e3406-128">Header</span><span class="sxs-lookup"><span data-stu-id="e3406-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3406-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e3406-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e3406-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e3406-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3406-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3406-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e3406-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3406-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3406-133">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="e3406-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e3406-134">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="e3406-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="e3406-135">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="e3406-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="e3406-136">**Iinkanalyzer:: getalteraten-Methode**</span><span class="sxs-lookup"><span data-stu-id="e3406-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="e3406-137">**Iinkanalyzer:: getalternatesforcontextnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="e3406-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e3406-138">**Iinkanalyzer:: ModifyTopAlternate-Methode**</span><span class="sxs-lookup"><span data-stu-id="e3406-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="e3406-139">**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**</span><span class="sxs-lookup"><span data-stu-id="e3406-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="e3406-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e3406-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Ruft Flags ab, die Steuern, wie iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'Iinkanalyzer:: getanalysismodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368097"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="0063c-103">Iinkanalyzer:: getanalysismodes-Methode</span><span class="sxs-lookup"><span data-stu-id="0063c-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="0063c-104">Ruft Flags ab, die Steuern, wie [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="0063c-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0063c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0063c-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="0063c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0063c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0063c-107">*panalysismode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0063c-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0063c-108">Eine bitweise Kombination der [**AnalysisModes**](analysismodes.md) -Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="0063c-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0063c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0063c-109">Return value</span></span>

<span data-ttu-id="0063c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0063c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0063c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0063c-111">Requirements</span></span>



| <span data-ttu-id="0063c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0063c-112">Requirement</span></span> | <span data-ttu-id="0063c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0063c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0063c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0063c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0063c-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0063c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0063c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0063c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0063c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0063c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0063c-118">Header</span><span class="sxs-lookup"><span data-stu-id="0063c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0063c-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0063c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0063c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0063c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0063c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0063c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0063c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0063c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0063c-123">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="0063c-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0063c-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="0063c-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="0063c-125">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="0063c-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="0063c-126">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="0063c-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="0063c-127">**Iinkanalyzer:: abtanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="0063c-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="0063c-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="0063c-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





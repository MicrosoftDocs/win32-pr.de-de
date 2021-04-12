---
description: Ändert Flags, die Steuern, wie iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'Iinkanalyzer:: abtanalysismodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526477"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="c147f-103">Iinkanalyzer:: abtanalysismodes-Methode</span><span class="sxs-lookup"><span data-stu-id="c147f-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="c147f-104">Ändert Flags, die Steuern, wie [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="c147f-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c147f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c147f-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="c147f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c147f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c147f-107">*analysismode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c147f-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c147f-108">Eine bitweise Kombination der [**AnalysisModes**](analysismodes.md) -Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="c147f-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c147f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c147f-109">Return value</span></span>

<span data-ttu-id="c147f-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c147f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c147f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c147f-111">Requirements</span></span>



| <span data-ttu-id="c147f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c147f-112">Requirement</span></span> | <span data-ttu-id="c147f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c147f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c147f-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c147f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c147f-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c147f-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c147f-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c147f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c147f-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c147f-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c147f-118">Header</span><span class="sxs-lookup"><span data-stu-id="c147f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c147f-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c147f-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c147f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c147f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c147f-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c147f-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c147f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c147f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c147f-123">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="c147f-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c147f-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="c147f-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="c147f-125">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="c147f-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c147f-126">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="c147f-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c147f-127">**Iinkanalyzer:: getanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="c147f-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="c147f-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="c147f-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





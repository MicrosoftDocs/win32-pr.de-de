---
description: Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Ianalysiswarning:: GetHint-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346959"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="e0f94-103">Ianalysiswarning:: GetHint-Methode</span><span class="sxs-lookup"><span data-stu-id="e0f94-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="e0f94-104">Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="e0f94-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0f94-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="e0f94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0f94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f94-107">*panalysishint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0f94-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f94-108">Der Kontext Knoten des Analyse Hinweises, der diese Warnung verursacht hat, oder **null** , wenn ein Analyse Hinweis Diese Warnung nicht verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="e0f94-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f94-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0f94-109">Return value</span></span>

<span data-ttu-id="e0f94-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e0f94-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f94-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0f94-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e0f94-112">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *panalysishint* aufrufen, wenn Sie den Kontext Knoten des Analyse Hinweises nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e0f94-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="e0f94-113">Ein Beispiel für einen Analyse Hinweis, der eine [**ianalysiswarning**](ianalysiswarning.md) generiert, ist ein Analyse Hinweis, der eine falsch geschriebene Faktoid enthält.</span><span class="sxs-lookup"><span data-stu-id="e0f94-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="e0f94-114">In diesem Fall gibt die frei Hand Analyse einen [**ianalysisstatus**](ianalysisstatus.md) zurück, der ein **ianalysiswarning** -Element enthält, das auf den Kontext Knoten des Analyse Hinweises mit der falsch geschriebenen Faktoid verweist.</span><span class="sxs-lookup"><span data-stu-id="e0f94-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="e0f94-115">In diesem Fall gibt die [**ianalysiswarning:: getwarningcode**](ianalysiswarning-getwarningcode.md) -Methode der Analyse Warnung außerdem einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ FactoidNotSupported** zurück.</span><span class="sxs-lookup"><span data-stu-id="e0f94-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f94-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0f94-116">Requirements</span></span>



| <span data-ttu-id="e0f94-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0f94-117">Requirement</span></span> | <span data-ttu-id="e0f94-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e0f94-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f94-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0f94-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f94-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0f94-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0f94-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0f94-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f94-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0f94-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e0f94-123">Header</span><span class="sxs-lookup"><span data-stu-id="e0f94-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f94-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e0f94-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e0f94-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f94-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0f94-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f94-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e0f94-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0f94-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f94-128">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="e0f94-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="e0f94-129">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="e0f94-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="e0f94-130">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="e0f94-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e0f94-131">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="e0f94-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e0f94-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="e0f94-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="e0f94-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e0f94-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


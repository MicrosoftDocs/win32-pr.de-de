---
description: Ruft 10 Analyse Alternativen für alle dem iinkanalyzer zugeordneten frei Hand Eingaben ab.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'Iinkanalyzer:: getalteraten-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357350"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="97046-103">Iinkanalyzer:: getalteraten-Methode</span><span class="sxs-lookup"><span data-stu-id="97046-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="97046-104">Ruft 10 Analyse Alternativen für alle dem [**iinkanalyzer**](iinkanalyzer.md)zugeordneten frei Hand Eingaben ab.</span><span class="sxs-lookup"><span data-stu-id="97046-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97046-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97046-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="97046-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97046-107">*ppalternativen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="97046-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97046-108">Ein Zeiger auf die ersten 10 [**ianalysisalternate**](ianalysisalternate.md) -Objekte für alle frei Hand Eingaben, die mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="97046-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97046-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97046-109">Return value</span></span>

<span data-ttu-id="97046-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="97046-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97046-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97046-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="97046-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="97046-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="97046-113">Die obere Alternative wird als erste Alternative der Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97046-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="97046-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97046-114">Requirements</span></span>



| <span data-ttu-id="97046-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97046-115">Requirement</span></span> | <span data-ttu-id="97046-116">Wert</span><span class="sxs-lookup"><span data-stu-id="97046-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97046-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97046-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97046-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97046-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97046-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97046-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97046-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="97046-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97046-121">Header</span><span class="sxs-lookup"><span data-stu-id="97046-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="97046-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="97046-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="97046-123">DLL</span><span class="sxs-lookup"><span data-stu-id="97046-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97046-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97046-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="97046-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97046-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97046-126">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="97046-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="97046-127">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="97046-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="97046-128">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="97046-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="97046-129">**Iinkanalyzer:: getalternatesforcontextnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="97046-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="97046-130">**Iinkanalyzer:: getalternatesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="97046-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="97046-131">**Iinkanalyzer:: ModifyTopAlternate-Methode**</span><span class="sxs-lookup"><span data-stu-id="97046-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="97046-132">**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**</span><span class="sxs-lookup"><span data-stu-id="97046-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="97046-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="97046-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


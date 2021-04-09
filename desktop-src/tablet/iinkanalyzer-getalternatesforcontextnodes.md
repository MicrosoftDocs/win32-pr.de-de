---
description: Ruft Analyse Alternativen für die Knoten in einer angegebenen icontextnodes-Sammlung ab.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Iinkanalyzer:: getalternatesforcontextnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129460"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="12a65-103">Iinkanalyzer:: getalternatesforcontextnodes-Methode</span><span class="sxs-lookup"><span data-stu-id="12a65-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="12a65-104">Ruft Analyse Alternativen für die Knoten in einer angegebenen [**icontextnodes**](icontextnodes.md) -Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="12a65-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a65-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="12a65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a65-107">*pcontextnodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a65-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a65-108">Die [**icontextnodes**](icontextnodes.md) -Auflistung, für die die Analyse Alternativen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12a65-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="12a65-109">*ulmaximumalteraten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12a65-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a65-110">Die maximale Anzahl von Alternativen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12a65-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="12a65-111">*ppalternativen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12a65-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a65-112">Das [**ianalysisalterniert**](ianalysisalternates.md) -Objekt, das die Analyse Alternativen enthält.</span><span class="sxs-lookup"><span data-stu-id="12a65-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a65-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12a65-113">Return value</span></span>

<span data-ttu-id="12a65-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="12a65-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12a65-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12a65-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="12a65-116">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="12a65-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="12a65-117">Der oberste [**ianalysisalternate**](ianalysisalternate.md) wird als erste Alternative der Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12a65-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="12a65-118">Die [**icontextnode**](icontextnode.md) -Objekte in *pcontextnodes* müssen keine angrenzenden Bereiche des Dokuments darstellen.</span><span class="sxs-lookup"><span data-stu-id="12a65-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="12a65-119">Für jeden Analyse Hinweis in Knoten gibt [**iinkanalyzer**](iinkanalyzer.md) nur die ersten alternativen zurück.</span><span class="sxs-lookup"><span data-stu-id="12a65-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a65-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12a65-120">Requirements</span></span>



| <span data-ttu-id="12a65-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12a65-121">Requirement</span></span> | <span data-ttu-id="12a65-122">Wert</span><span class="sxs-lookup"><span data-stu-id="12a65-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12a65-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12a65-123">Minimum supported client</span></span><br/> | <span data-ttu-id="12a65-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12a65-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12a65-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12a65-125">Minimum supported server</span></span><br/> | <span data-ttu-id="12a65-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="12a65-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12a65-127">Header</span><span class="sxs-lookup"><span data-stu-id="12a65-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="12a65-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12a65-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12a65-129">DLL</span><span class="sxs-lookup"><span data-stu-id="12a65-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12a65-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12a65-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="12a65-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12a65-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a65-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="12a65-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="12a65-133">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="12a65-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="12a65-134">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="12a65-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="12a65-135">**Iinkanalyzer:: getalteraten-Methode**</span><span class="sxs-lookup"><span data-stu-id="12a65-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="12a65-136">**Iinkanalyzer:: getalternatesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="12a65-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="12a65-137">**Iinkanalyzer:: ModifyTopAlternate-Methode**</span><span class="sxs-lookup"><span data-stu-id="12a65-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="12a65-138">**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**</span><span class="sxs-lookup"><span data-stu-id="12a65-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="12a65-139">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="12a65-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


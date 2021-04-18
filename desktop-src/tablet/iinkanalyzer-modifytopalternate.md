---
description: Ändert die aktuelle obere Alternative in die angegebene alternative und löscht den bestätentyp für alle icontextnode-Objekte, die der alternativen zugeordnet sind.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Iinkanalyzer:: ModifyTopAlternate-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354499"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="f11be-103">Iinkanalyzer:: ModifyTopAlternate-Methode</span><span class="sxs-lookup"><span data-stu-id="f11be-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="f11be-104">Ändert die aktuelle obere Alternative in die angegebene alternative und löscht den bestätentyp für alle [**icontextnode**](icontextnode.md) -Objekte, die der alternativen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f11be-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f11be-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="f11be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f11be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11be-107">*palternate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f11be-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11be-108">Das [**ianalysisalternate**](ianalysisalternate.md) -Objekt, das die neue obere Alternative enthält.</span><span class="sxs-lookup"><span data-stu-id="f11be-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11be-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f11be-109">Return value</span></span>

<span data-ttu-id="f11be-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f11be-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f11be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f11be-111">Remarks</span></span>

<span data-ttu-id="f11be-112">Um Analyse Alternativen zu erhalten, verwenden Sie die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md), die [**iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)oder die [**iinkanalyzer:: getalternatesforstriche-Methode**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="f11be-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="f11be-113">Verwenden Sie die [**ianalysisalternate:: getalternatenodes-Methode**](ianalysisalternate-getalternatenodes.md), um die [**icontextnode**](icontextnode.md) -Objekte zu erhalten, die einer alternativen Analyse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f11be-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="f11be-114">Verwenden Sie [**icontextnode:: Confirm**](icontextnode-confirm.md), um den bestätentyp für einen Kontext Knoten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f11be-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f11be-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f11be-115">Requirements</span></span>



| <span data-ttu-id="f11be-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f11be-116">Requirement</span></span> | <span data-ttu-id="f11be-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f11be-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f11be-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f11be-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f11be-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f11be-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f11be-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f11be-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f11be-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f11be-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f11be-122">Header</span><span class="sxs-lookup"><span data-stu-id="f11be-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f11be-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f11be-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f11be-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f11be-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f11be-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11be-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f11be-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f11be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11be-127">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="f11be-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f11be-128">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="f11be-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="f11be-129">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="f11be-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f11be-130">**ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="f11be-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="f11be-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f11be-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





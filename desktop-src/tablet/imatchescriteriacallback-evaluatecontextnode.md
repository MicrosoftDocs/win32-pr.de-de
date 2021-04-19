---
description: Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes icontextnode-Objekt die Kriterien erfüllt.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Imatchescriteria acallback:: evaluatecontextnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348165"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="75d20-103">Imatchescriteria acallback:: evaluatecontextnode-Methode</span><span class="sxs-lookup"><span data-stu-id="75d20-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="75d20-104">Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes [**icontextnode**](icontextnode.md) -Objekt die Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="75d20-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d20-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="75d20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d20-107">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75d20-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d20-108">Das [**icontextnode**](icontextnode.md) -Objekt, das ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="75d20-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="75d20-109">*pbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75d20-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d20-110">**Variant \_ TRUE** , wenn *pcontextnodebug* den Kriterien entspricht. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="75d20-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d20-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75d20-111">Return value</span></span>

<span data-ttu-id="75d20-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="75d20-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75d20-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75d20-113">Remarks</span></span>

<span data-ttu-id="75d20-114">Um die [**iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md) oder die [**iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)zu verwenden, erstellen Sie eine Klasse, die [**imatchescriteria acallback**](imatchescriteriacallback.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="75d20-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="75d20-115">Implementieren Sie **imatchescriteria acallback:: evaluatecontextnode** , um **Variant \_ true** zurückzugeben, wenn das [**icontextnode**](icontextnode.md) -Objekt mit Ihren Kriterien übereinstimmt, und andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="75d20-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="75d20-116">Für einige Kriterien müssen Sie möglicherweise eine Möglichkeit zur Initialisierung oder Beibehaltung des Zustands Ihres **imatchescriteria** -Objekts bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="75d20-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d20-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75d20-117">Requirements</span></span>



| <span data-ttu-id="75d20-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75d20-118">Requirement</span></span> | <span data-ttu-id="75d20-119">Wert</span><span class="sxs-lookup"><span data-stu-id="75d20-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d20-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75d20-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75d20-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75d20-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75d20-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75d20-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75d20-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75d20-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75d20-124">Header</span><span class="sxs-lookup"><span data-stu-id="75d20-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d20-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75d20-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75d20-126">DLL</span><span class="sxs-lookup"><span data-stu-id="75d20-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d20-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d20-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75d20-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75d20-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d20-129">**Imatcheskriteriacallback**</span><span class="sxs-lookup"><span data-stu-id="75d20-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="75d20-130">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="75d20-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="75d20-131">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="75d20-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="75d20-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="75d20-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





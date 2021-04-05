---
description: Ruft alle icontextnode-Objekte ab, die den angegebenen Kriterien entsprechen.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'Iinkanalyzer:: findnodeswithcallback-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751832"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="06c79-103">Iinkanalyzer:: findnodeswithcallback-Methode</span><span class="sxs-lookup"><span data-stu-id="06c79-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="06c79-104">Ruft alle [**icontextnode**](icontextnode.md) -Objekte ab, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="06c79-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06c79-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="06c79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c79-107">*pcriteria* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06c79-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c79-108">Ein [**imatchescriteria**](imatchescriteriacallback.md) -Objekt, das verwendet wird, um zu überprüfen, ob ein [**icontextnode**](icontextnode.md) -Objekt die angegebenen Kriterien erfüllt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="06c79-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="06c79-109">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06c79-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c79-110">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die alle Knoten enthält, die die angegebenen Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="06c79-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c79-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06c79-111">Return value</span></span>

<span data-ttu-id="06c79-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="06c79-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06c79-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06c79-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="06c79-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="06c79-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="06c79-115">Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen derartigen [**icontextnode**](icontextnode.md)enthält, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06c79-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c79-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c79-116">Requirements</span></span>



| <span data-ttu-id="06c79-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06c79-117">Requirement</span></span> | <span data-ttu-id="06c79-118">Wert</span><span class="sxs-lookup"><span data-stu-id="06c79-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c79-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06c79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06c79-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06c79-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06c79-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06c79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06c79-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="06c79-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="06c79-123">Header</span><span class="sxs-lookup"><span data-stu-id="06c79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c79-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="06c79-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="06c79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="06c79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c79-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c79-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="06c79-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06c79-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c79-128">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="06c79-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="06c79-129">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="06c79-130">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="06c79-131">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="06c79-132">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="06c79-133">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="06c79-134">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="06c79-135">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="06c79-136">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="06c79-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="06c79-137">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="06c79-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


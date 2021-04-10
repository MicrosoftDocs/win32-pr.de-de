---
description: Ruft alle frei Hand Blattknoten ab.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Iinkanalyzer:: FindInkLeafNodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862696"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="21bc7-103">Iinkanalyzer:: FindInkLeafNodes-Methode</span><span class="sxs-lookup"><span data-stu-id="21bc7-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="21bc7-104">Ruft alle frei Hand Blattknoten ab.</span><span class="sxs-lookup"><span data-stu-id="21bc7-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21bc7-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="21bc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21bc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bc7-107">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21bc7-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21bc7-108">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die alle frei Hand Blattknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="21bc7-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bc7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21bc7-109">Return value</span></span>

<span data-ttu-id="21bc7-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="21bc7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21bc7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21bc7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="21bc7-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="21bc7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="21bc7-113">Blattknoten enthalten keine untergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="21bc7-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="21bc7-114">Frei Hand Knoten enthalten Strich Daten.</span><span class="sxs-lookup"><span data-stu-id="21bc7-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="21bc7-115">Beispiele für frei Hand Blattknoten sind InkWord-, InkDrawing-und InkBullet- [**icontextnode**](icontextnode.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="21bc7-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="21bc7-116">Weitere Informationen finden Sie unter [Kontext Knoten Typen](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="21bc7-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21bc7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21bc7-117">Requirements</span></span>



| <span data-ttu-id="21bc7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21bc7-118">Requirement</span></span> | <span data-ttu-id="21bc7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="21bc7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bc7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21bc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21bc7-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21bc7-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21bc7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21bc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21bc7-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="21bc7-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21bc7-124">Header</span><span class="sxs-lookup"><span data-stu-id="21bc7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21bc7-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="21bc7-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21bc7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="21bc7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21bc7-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21bc7-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21bc7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21bc7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bc7-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="21bc7-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="21bc7-130">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="21bc7-131">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="21bc7-132">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="21bc7-133">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="21bc7-134">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="21bc7-135">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="21bc7-136">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="21bc7-137">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="21bc7-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="21bc7-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="21bc7-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


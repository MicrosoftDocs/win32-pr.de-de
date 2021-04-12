---
description: Ruft alle Blattknoten ab.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'Iinkanalyzer:: findleafnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526498"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="e60ef-103">Iinkanalyzer:: findleafnodes-Methode</span><span class="sxs-lookup"><span data-stu-id="e60ef-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="e60ef-104">Ruft alle Blattknoten ab.</span><span class="sxs-lookup"><span data-stu-id="e60ef-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e60ef-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="e60ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e60ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e60ef-107">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e60ef-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e60ef-108">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die alle Blattknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="e60ef-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e60ef-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e60ef-109">Return value</span></span>

<span data-ttu-id="e60ef-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e60ef-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e60ef-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e60ef-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e60ef-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e60ef-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="e60ef-113">Blattknoten enthalten keine untergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="e60ef-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="e60ef-114">Beispiele für frei Hand Blattknoten sind InkWord-, textword-, Image-, InkDrawing-und InkBullet [**icontextnode**](icontextnode.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="e60ef-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="e60ef-115">Weitere Informationen finden Sie unter [Kontext Knoten Typen](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="e60ef-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e60ef-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e60ef-116">Requirements</span></span>



| <span data-ttu-id="e60ef-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e60ef-117">Requirement</span></span> | <span data-ttu-id="e60ef-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e60ef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e60ef-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e60ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e60ef-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e60ef-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e60ef-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e60ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e60ef-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e60ef-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e60ef-123">Header</span><span class="sxs-lookup"><span data-stu-id="e60ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e60ef-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e60ef-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e60ef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e60ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e60ef-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e60ef-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e60ef-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e60ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60ef-128">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="e60ef-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e60ef-129">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="e60ef-130">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="e60ef-131">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="e60ef-132">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="e60ef-133">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="e60ef-134">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="e60ef-135">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="e60ef-136">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="e60ef-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="e60ef-137">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e60ef-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


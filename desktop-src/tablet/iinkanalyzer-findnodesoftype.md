---
description: Ruft alle icontextnode-Objekte des angegebenen Typs ab.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Iinkanalyzer:: findnodesoft ype-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862691"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="76008-103">Iinkanalyzer:: findnodesoft ype-Methode</span><span class="sxs-lookup"><span data-stu-id="76008-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="76008-104">Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab.</span><span class="sxs-lookup"><span data-stu-id="76008-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="76008-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76008-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="76008-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76008-107">*pnodetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76008-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76008-108">Der **GUID** , der den Knotentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="76008-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="76008-109">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76008-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76008-110">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) , die alle Knoten des Typs " *pnodetype*" enthält.</span><span class="sxs-lookup"><span data-stu-id="76008-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76008-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76008-111">Return value</span></span>

<span data-ttu-id="76008-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="76008-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76008-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76008-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="76008-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="76008-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="76008-115">Die *pnodetype* -Eigenschaft muss eine GUID aus den [Kontext Knoten Typen](context-node-types.md) Konstanten enthalten.</span><span class="sxs-lookup"><span data-stu-id="76008-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="76008-116">Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen derartigen [**icontextnode**](icontextnode.md)enthält, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76008-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="76008-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76008-117">Requirements</span></span>



| <span data-ttu-id="76008-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76008-118">Requirement</span></span> | <span data-ttu-id="76008-119">Wert</span><span class="sxs-lookup"><span data-stu-id="76008-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76008-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76008-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76008-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76008-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="76008-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76008-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76008-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76008-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="76008-124">Header</span><span class="sxs-lookup"><span data-stu-id="76008-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76008-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="76008-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="76008-126">DLL</span><span class="sxs-lookup"><span data-stu-id="76008-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76008-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76008-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="76008-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76008-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76008-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="76008-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="76008-130">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="76008-131">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="76008-132">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="76008-133">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="76008-134">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="76008-135">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="76008-136">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="76008-137">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="76008-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="76008-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="76008-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


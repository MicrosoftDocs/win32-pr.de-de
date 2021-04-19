---
description: Ruft alle icontextnode-Objekte des angegebenen Typs ab, die die angegebenen Striche enthalten.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346957"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="1122a-103">Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="1122a-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="1122a-104">Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab, die die angegebenen Striche enthalten.</span><span class="sxs-lookup"><span data-stu-id="1122a-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1122a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1122a-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="1122a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1122a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1122a-107">*pnodetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1122a-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1122a-108">Der Globally Unique Identifier (GUID), der den Knotentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="1122a-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="1122a-109">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1122a-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1122a-110">Die Anzahl der über gebenen Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1122a-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="1122a-111">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1122a-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1122a-112">Ein Array der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1122a-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="1122a-113">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1122a-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1122a-114">Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, die alle Knoten vom Typ " *pnodetype* " enthalten, die die Striche mit bezeichern im *plstrokeids* -Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="1122a-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1122a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1122a-115">Return value</span></span>

<span data-ttu-id="1122a-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1122a-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1122a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1122a-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1122a-118">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="1122a-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1122a-119">Die *pnodetype* -Eigenschaft muss eine GUID aus den [Kontext Knoten Typen](context-node-types.md) Konstanten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1122a-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="1122a-120">Wenn der angegebene Knotentyp kein Blattknoten ist, aber einer der untergeordneten Knoten auf einen Strich in der Striche-Auflistung verweist, wird dieser Knoten der zurückgegebenen Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1122a-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="1122a-121">Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen derartigen [**icontextnode**](icontextnode.md)enthält, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1122a-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1122a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1122a-122">Requirements</span></span>



| <span data-ttu-id="1122a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1122a-123">Requirement</span></span> | <span data-ttu-id="1122a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1122a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1122a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1122a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1122a-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1122a-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1122a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1122a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1122a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1122a-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1122a-129">Header</span><span class="sxs-lookup"><span data-stu-id="1122a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1122a-130"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1122a-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1122a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1122a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1122a-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1122a-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1122a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1122a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1122a-134">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="1122a-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1122a-135">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="1122a-136">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="1122a-137">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="1122a-138">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="1122a-139">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="1122a-140">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="1122a-141">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="1122a-142">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="1122a-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="1122a-143">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="1122a-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


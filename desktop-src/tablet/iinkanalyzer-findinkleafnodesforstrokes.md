---
description: Ruft die frei Hand Blattknoten ab, die die angegebenen Striche enthalten.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Iinkanalyzer:: findinkleafnodesforstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862692"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="62ce4-103">Iinkanalyzer:: findinkleafnodesforstrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="62ce4-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="62ce4-104">Ruft die frei Hand Blattknoten ab, die die angegebenen Striche enthalten.</span><span class="sxs-lookup"><span data-stu-id="62ce4-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ce4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ce4-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="62ce4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ce4-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62ce4-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ce4-108">Die Anzahl der über gebenen Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="62ce4-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="62ce4-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62ce4-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ce4-110">Ein Array der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="62ce4-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="62ce4-111">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62ce4-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ce4-112">Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, die alle frei Hand Blattknoten enthalten, die die Striche mit bezeichern im *plstrokeids* -Array enthalten.</span><span class="sxs-lookup"><span data-stu-id="62ce4-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ce4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62ce4-113">Return value</span></span>

<span data-ttu-id="62ce4-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="62ce4-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62ce4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62ce4-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="62ce4-116">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="62ce4-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="62ce4-117">Blattknoten enthalten keine untergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="62ce4-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="62ce4-118">Frei Hand Knoten enthalten Strich Daten.</span><span class="sxs-lookup"><span data-stu-id="62ce4-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="62ce4-119">Beispiele für frei Hand Blattknoten sind InkWord-, InkDrawing-und andinkbullet- [**icontextnode**](icontextnode.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="62ce4-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="62ce4-120">Weitere Informationen finden Sie unter [Kontext Knoten Typen](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="62ce4-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="62ce4-121">Wenn keine Knoten die angegebenen Striche enthalten, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62ce4-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="62ce4-122">Wenn *ulstrokeidscount* gleich 0 (null) ist, wird eine leere **icontextnodes** -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62ce4-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ce4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62ce4-123">Requirements</span></span>



| <span data-ttu-id="62ce4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ce4-124">Requirement</span></span> | <span data-ttu-id="62ce4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="62ce4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ce4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62ce4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="62ce4-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62ce4-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="62ce4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62ce4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="62ce4-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="62ce4-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="62ce4-130">Header</span><span class="sxs-lookup"><span data-stu-id="62ce4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ce4-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="62ce4-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="62ce4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62ce4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ce4-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ce4-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="62ce4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ce4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ce4-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="62ce4-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="62ce4-136">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="62ce4-137">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="62ce4-138">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="62ce4-139">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="62ce4-140">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="62ce4-141">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="62ce4-142">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="62ce4-143">**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="62ce4-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="62ce4-144">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="62ce4-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


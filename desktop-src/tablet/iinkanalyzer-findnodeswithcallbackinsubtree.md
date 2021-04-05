---
description: Ruft alle icontextnode-Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen icontextnode-Objekts sind.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751825"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="9b73b-103">Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode</span><span class="sxs-lookup"><span data-stu-id="9b73b-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="9b73b-104">Ruft alle [**icontextnode**](icontextnode.md) -Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen **icontextnode** -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="9b73b-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b73b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b73b-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="9b73b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b73b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b73b-107">*pcriteria* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-108">Ein [**imatchescriteria**](imatchescriteriacallback.md) -Objekt, das verwendet wird, um zu überprüfen, ob ein [**icontextnode**](icontextnode.md) -Objekt die angegebenen Kriterien erfüllt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9b73b-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-109">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-110">Das [**icontextnode**](icontextnode.md) -Objekt, dessen Nachfolgern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="9b73b-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-111">*ppcontextnodesfound* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-112">Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) , die alle Knoten enthält, die die angegebenen Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9b73b-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b73b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b73b-113">Return value</span></span>

<span data-ttu-id="9b73b-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9b73b-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b73b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b73b-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9b73b-116">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="9b73b-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9b73b-117">Wenn [**iinkanalyzer**](iinkanalyzer.md) den *pcontextnodedesearchfrom* -Knoten nicht enthält, gibt diese Methode einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="9b73b-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="9b73b-118">Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen derartigen [**icontextnode**](icontextnode.md)enthält, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b73b-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b73b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b73b-119">Requirements</span></span>



| <span data-ttu-id="9b73b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b73b-120">Requirement</span></span> | <span data-ttu-id="9b73b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9b73b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b73b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b73b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b73b-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9b73b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b73b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b73b-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b73b-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9b73b-126">Header</span><span class="sxs-lookup"><span data-stu-id="9b73b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b73b-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9b73b-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9b73b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9b73b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b73b-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b73b-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9b73b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b73b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b73b-131">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="9b73b-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9b73b-132">**Iinkanalyzer:: FindInkLeafNodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="9b73b-133">**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9b73b-134">**Iinkanalyzer:: findleafnodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="9b73b-135">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="9b73b-136">**Iinkanalyzer:: findnodesoft ype-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="9b73b-137">**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9b73b-138">**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="9b73b-139">**Iinkanalyzer:: findnodeswithcallback-Methode**</span><span class="sxs-lookup"><span data-stu-id="9b73b-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="9b73b-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="9b73b-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


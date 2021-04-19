---
description: Ruft die Position und die Größe des icontextnode-Objekts ab.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'Icontextnode:: GetLocation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359855"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="6e609-103">Icontextnode:: GetLocation-Methode</span><span class="sxs-lookup"><span data-stu-id="6e609-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="6e609-104">Ruft die Position und die Größe des [**icontextnode**](icontextnode.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="6e609-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e609-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e609-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="6e609-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e609-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e609-107">*ppianalysisregion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6e609-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e609-108">Ein Zeiger auf die Position und Größe des [**icontextnode**](icontextnode.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6e609-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e609-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e609-109">Return value</span></span>

<span data-ttu-id="6e609-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6e609-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e609-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e609-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6e609-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) in \* *ppianalysisregion* , wenn Sie den Analysebereich nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="6e609-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="6e609-113">Der Speicherort für einen Container Knoten wird ermittelt, indem die Vereinigung aller Standorte des Blatts gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6e609-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="6e609-114">Der Speicherort für einen frei Hand Blattknoten wird ermittelt, indem die Gesamtmenge des umgebenden Felds der zugeordneten Striche gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6e609-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="6e609-115">Der Speicherort für einen nicht frei Hand Blattknoten wird beim Erstellen des Knotens festgelegt und kann mithilfe von [**icontextnode:: setLocation**](icontextnode-setlocation.md)aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e609-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6e609-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e609-116">Examples</span></span>

<span data-ttu-id="6e609-117">Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft.</span><span class="sxs-lookup"><span data-stu-id="6e609-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="6e609-118">Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.</span><span class="sxs-lookup"><span data-stu-id="6e609-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="6e609-119">**Icontextnode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="6e609-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="6e609-120">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="6e609-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="6e609-121">**Icontextnode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="6e609-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="6e609-122">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="6e609-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6e609-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e609-123">Requirements</span></span>



| <span data-ttu-id="6e609-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e609-124">Requirement</span></span> | <span data-ttu-id="6e609-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6e609-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e609-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e609-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6e609-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e609-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6e609-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e609-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6e609-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e609-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6e609-130">Header</span><span class="sxs-lookup"><span data-stu-id="6e609-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e609-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6e609-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6e609-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6e609-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e609-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e609-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6e609-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e609-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e609-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="6e609-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6e609-136">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="6e609-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="6e609-137">**Icontextnode:: setLocation**</span><span class="sxs-lookup"><span data-stu-id="6e609-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="6e609-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="6e609-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


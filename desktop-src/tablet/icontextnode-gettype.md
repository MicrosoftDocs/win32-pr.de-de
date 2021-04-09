---
description: Ruft den Typ des icontextnode-Objekts ab.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'Icontextnode:: GetType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129493"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="d6ec0-103">Icontextnode:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="d6ec0-103">IContextNode::GetType method</span></span>

<span data-ttu-id="d6ec0-104">Ruft den Typ des [**icontextnode**](icontextnode.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ec0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6ec0-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="d6ec0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6ec0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ec0-107">*pcontextnodetype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d6ec0-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec0-108">Der Typ des [**icontextnode**](icontextnode.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ec0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6ec0-109">Return value</span></span>

<span data-ttu-id="d6ec0-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d6ec0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ec0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6ec0-111">Remarks</span></span>

<span data-ttu-id="d6ec0-112">Knoten Typen werden in den [Kontext Knoten Typen](context-node-types.md) -Konstanten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="d6ec0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6ec0-113">Examples</span></span>

<span data-ttu-id="d6ec0-114">Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="d6ec0-115">Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="d6ec0-116">**Icontextnode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="d6ec0-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="d6ec0-117">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="d6ec0-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="d6ec0-118">**Icontextnode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="d6ec0-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="d6ec0-119">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="d6ec0-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="d6ec0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6ec0-120">Requirements</span></span>



| <span data-ttu-id="d6ec0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6ec0-121">Requirement</span></span> | <span data-ttu-id="d6ec0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6ec0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ec0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6ec0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ec0-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6ec0-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d6ec0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6ec0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ec0-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6ec0-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d6ec0-127">Header</span><span class="sxs-lookup"><span data-stu-id="d6ec0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ec0-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d6ec0-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d6ec0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d6ec0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6ec0-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ec0-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d6ec0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6ec0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ec0-132">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="d6ec0-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d6ec0-133">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="d6ec0-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="d6ec0-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d6ec0-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Ruft den übergeordneten Knoten dieses icontextnode in der Kontext Knoten Struktur ab.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'Icontextnode:: getcentnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526528"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="15378-103">Icontextnode:: getcentnode-Methode</span><span class="sxs-lookup"><span data-stu-id="15378-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="15378-104">Ruft den übergeordneten Knoten dieses [**icontextnode**](icontextnode.md) in der Kontext Knoten Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="15378-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="15378-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15378-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="15378-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15378-107">*ppparameentcontextnode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="15378-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15378-108">Ein Zeiger auf den übergeordneten Knoten dieses [**icontextnode**](icontextnode.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="15378-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15378-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15378-109">Return value</span></span>

<span data-ttu-id="15378-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="15378-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15378-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15378-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="15378-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppparameentcontextnode* , wenn Sie den übergeordneten Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="15378-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="15378-113">Wenn dies der Stamm Knoten ist, wird der Parameter *ppparameentcontextnode* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15378-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="15378-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15378-114">Examples</span></span>

<span data-ttu-id="15378-115">Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft.</span><span class="sxs-lookup"><span data-stu-id="15378-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="15378-116">Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.</span><span class="sxs-lookup"><span data-stu-id="15378-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="15378-117">**Icontextnode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="15378-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="15378-118">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="15378-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="15378-119">**Icontextnode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="15378-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="15378-120">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="15378-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="15378-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15378-121">Requirements</span></span>



| <span data-ttu-id="15378-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15378-122">Requirement</span></span> | <span data-ttu-id="15378-123">Wert</span><span class="sxs-lookup"><span data-stu-id="15378-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15378-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15378-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15378-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15378-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15378-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15378-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15378-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15378-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="15378-128">Header</span><span class="sxs-lookup"><span data-stu-id="15378-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="15378-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15378-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15378-130">DLL</span><span class="sxs-lookup"><span data-stu-id="15378-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15378-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15378-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="15378-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15378-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15378-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="15378-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="15378-134">**Icontextnode:: getsubnodes**</span><span class="sxs-lookup"><span data-stu-id="15378-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="15378-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="15378-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


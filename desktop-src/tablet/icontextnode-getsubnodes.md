---
description: Ruft die direkten untergeordneten Knoten des icontextnode-Objekts ab.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'Icontextnode:: getsubnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372836"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="8a5f6-103">Icontextnode:: getsubnodes-Methode</span><span class="sxs-lookup"><span data-stu-id="8a5f6-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="8a5f6-104">Ruft die direkten untergeordneten Knoten des [**icontextnode**](icontextnode.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a5f6-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="8a5f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a5f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5f6-107">*ppsubcontextnodes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a5f6-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5f6-108">Eine Auflistung der [**icontextnode**](icontextnode.md) -Objekte, die direkt untergeordnete Knoten dieses **icontextnode** sind.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a5f6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a5f6-109">Return value</span></span>

<span data-ttu-id="8a5f6-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8a5f6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5f6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a5f6-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a5f6-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppsubcontextnodes* , wenn Sie die Auflistung der untergeordneten Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="8a5f6-113">Dies gibt nur die direkten untergeordneten Knoten zurück, nicht alle untergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="8a5f6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a5f6-114">Examples</span></span>

<span data-ttu-id="8a5f6-115">Dieses Beispiel zeigt eine Methode, `ExploreContextNode` , die einen [**icontextnode**](icontextnode.md)untersucht.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="8a5f6-116">Die-Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8a5f6-116">The method does the following:</span></span>

-   <span data-ttu-id="8a5f6-117">Ruft den Typ des Kontext Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="8a5f6-118">Überprüft bestimmte Eigenschaften des Knoten Typs durch Aufrufen einer Hilfsmethode, wenn es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten handelt.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="8a5f6-119">Prüft jeden unter Knoten durch Aufrufen von sich selbst, wenn der Knoten über untergeordnete Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="8a5f6-120">Untersucht die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode, wenn der Knoten ein frei Hand Blattknoten ist.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="8a5f6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a5f6-121">Requirements</span></span>



| <span data-ttu-id="8a5f6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a5f6-122">Requirement</span></span> | <span data-ttu-id="8a5f6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8a5f6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5f6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a5f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5f6-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a5f6-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a5f6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a5f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5f6-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8a5f6-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a5f6-128">Header</span><span class="sxs-lookup"><span data-stu-id="8a5f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a5f6-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5f6-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a5f6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5f6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5f6-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a5f6-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a5f6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a5f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5f6-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="8a5f6-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8a5f6-134">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="8a5f6-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="8a5f6-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8a5f6-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


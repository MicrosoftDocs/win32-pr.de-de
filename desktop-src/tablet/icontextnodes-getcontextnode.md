---
description: Ruft das icontextnode-Objekt am angegebenen Index in dieser Auflistung ab.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'Icontextnodes:: getcontextnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485099"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="afc25-103">Icontextnodes:: getcontextnode-Methode</span><span class="sxs-lookup"><span data-stu-id="afc25-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="afc25-104">Ruft das [**icontextnode**](icontextnode.md) -Objekt am angegebenen Index in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="afc25-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc25-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="afc25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc25-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc25-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc25-108">Der null basierte Index des abzurufenden [**icontextnode**](icontextnode.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="afc25-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="afc25-109">*ppcontextnode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="afc25-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc25-110">Zeiger auf den [**icontextnode**](icontextnode.md) , auf den am angegebenen Index verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="afc25-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc25-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afc25-111">Return value</span></span>

<span data-ttu-id="afc25-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="afc25-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afc25-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc25-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="afc25-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextnode* , wenn Sie den Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="afc25-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="afc25-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afc25-115">Examples</span></span>

<span data-ttu-id="afc25-116">Dieses Beispiel zeigt eine Methode, `ExploreContextNode` , die einen [**icontextnode**](icontextnode.md)untersucht.</span><span class="sxs-lookup"><span data-stu-id="afc25-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="afc25-117">Die-Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="afc25-117">The method does the following:</span></span>

-   <span data-ttu-id="afc25-118">Ruft den Typ des Kontext Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="afc25-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="afc25-119">Überprüft bestimmte Eigenschaften des Knoten Typs durch Aufrufen einer Hilfsmethode, wenn es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten handelt.</span><span class="sxs-lookup"><span data-stu-id="afc25-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="afc25-120">Prüft jeden unter Knoten durch Aufrufen von sich selbst, wenn der Knoten über untergeordnete Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="afc25-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="afc25-121">Untersucht die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode, wenn der Knoten ein frei Hand Blattknoten ist.</span><span class="sxs-lookup"><span data-stu-id="afc25-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="afc25-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc25-122">Requirements</span></span>



| <span data-ttu-id="afc25-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc25-123">Requirement</span></span> | <span data-ttu-id="afc25-124">Wert</span><span class="sxs-lookup"><span data-stu-id="afc25-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc25-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc25-125">Minimum supported client</span></span><br/> | <span data-ttu-id="afc25-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc25-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="afc25-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc25-127">Minimum supported server</span></span><br/> | <span data-ttu-id="afc25-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="afc25-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="afc25-129">Header</span><span class="sxs-lookup"><span data-stu-id="afc25-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc25-130"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="afc25-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="afc25-131">DLL</span><span class="sxs-lookup"><span data-stu-id="afc25-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc25-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc25-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="afc25-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afc25-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc25-134">**Icontextnodes**</span><span class="sxs-lookup"><span data-stu-id="afc25-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="afc25-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="afc25-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Ruft die Anzahl der Striche ab, die dem icontextnode-Objekt zugeordnet sind.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'Icontextnode:: getstrokecount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485107"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="f19bd-103">Icontextnode:: getstrokecount-Methode</span><span class="sxs-lookup"><span data-stu-id="f19bd-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="f19bd-104">Ruft die Anzahl der Striche ab, die dem [**icontextnode**](icontextnode.md) -Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f19bd-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f19bd-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="f19bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f19bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19bd-107">*pulstrokecount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f19bd-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f19bd-108">Die Anzahl der Striche, die dem [**icontextnode**](icontextnode.md) -Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f19bd-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19bd-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f19bd-109">Return value</span></span>

<span data-ttu-id="f19bd-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f19bd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f19bd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f19bd-111">Remarks</span></span>

<span data-ttu-id="f19bd-112">Nur frei Hand Blatt Kontext Knoten verfügen über zugeordnete Strich Daten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="f19bd-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="f19bd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f19bd-113">Examples</span></span>

<span data-ttu-id="f19bd-114">Dieses Beispiel zeigt eine Methode, `ExploreContextNode` , die einen [**icontextnode**](icontextnode.md)untersucht.</span><span class="sxs-lookup"><span data-stu-id="f19bd-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="f19bd-115">Die-Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="f19bd-115">The method does the following:</span></span>

-   <span data-ttu-id="f19bd-116">Ruft den Typ des Kontext Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="f19bd-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="f19bd-117">Überprüft bestimmte Eigenschaften des Knoten Typs durch Aufrufen einer Hilfsmethode, wenn es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten handelt.</span><span class="sxs-lookup"><span data-stu-id="f19bd-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="f19bd-118">Prüft jeden unter Knoten durch Aufrufen von sich selbst, wenn der Knoten über untergeordnete Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="f19bd-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="f19bd-119">Untersucht die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode, wenn der Knoten ein frei Hand Blattknoten ist.</span><span class="sxs-lookup"><span data-stu-id="f19bd-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f19bd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f19bd-120">Requirements</span></span>



| <span data-ttu-id="f19bd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f19bd-121">Requirement</span></span> | <span data-ttu-id="f19bd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f19bd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19bd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f19bd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f19bd-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f19bd-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f19bd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f19bd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f19bd-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f19bd-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f19bd-127">Header</span><span class="sxs-lookup"><span data-stu-id="f19bd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f19bd-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f19bd-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f19bd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f19bd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f19bd-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f19bd-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f19bd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f19bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19bd-132">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="f19bd-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f19bd-133">**Icontextnode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="f19bd-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="f19bd-134">**Icontextnode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="f19bd-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="f19bd-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f19bd-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Ruft den Bezeichner für das icontextnode-Objekt ab.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Icontextnode:: GetId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862719"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="f8328-103">Icontextnode:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="f8328-103">IContextNode::GetId method</span></span>

<span data-ttu-id="f8328-104">Ruft den Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f8328-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8328-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8328-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="f8328-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8328-107">*pId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f8328-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8328-108">Der Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f8328-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8328-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8328-109">Return value</span></span>

<span data-ttu-id="f8328-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f8328-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8328-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8328-111">Remarks</span></span>

<span data-ttu-id="f8328-112">Der Ink Analyzer weist allen erstellten Kontext Knoten einen eindeutigen Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="f8328-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="f8328-113">Während der frei Hand Analyse kann der Ink-Analyzer den Bezeichner für einen Kontext Knoten ändern.</span><span class="sxs-lookup"><span data-stu-id="f8328-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="f8328-114">Beispielsweise kann der Ink Analyzer einen Word-Knoten als zwei Word-Knoten neu klassifizieren und den ursprünglichen Bezeichner dann einem und einem neuen Bezeichner zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f8328-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="f8328-115">Oder der Ink Analyzer kann zwei Word-Knoten als einen Word-Knoten neu klassifizieren und einen der ursprünglichen Bezeichner dem neuen Word-Knoten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f8328-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="f8328-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8328-116">Examples</span></span>

<span data-ttu-id="f8328-117">Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft.</span><span class="sxs-lookup"><span data-stu-id="f8328-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="f8328-118">Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.</span><span class="sxs-lookup"><span data-stu-id="f8328-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="f8328-119">**Icontextnode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="f8328-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="f8328-120">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="f8328-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="f8328-121">**Icontextnode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="f8328-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="f8328-122">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="f8328-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="f8328-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8328-123">Requirements</span></span>



| <span data-ttu-id="f8328-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8328-124">Requirement</span></span> | <span data-ttu-id="f8328-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f8328-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8328-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8328-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f8328-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8328-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f8328-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8328-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f8328-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8328-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f8328-130">Header</span><span class="sxs-lookup"><span data-stu-id="f8328-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8328-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f8328-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f8328-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8328-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8328-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8328-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f8328-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8328-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8328-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="f8328-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f8328-136">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f8328-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





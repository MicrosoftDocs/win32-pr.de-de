---
description: Erstellt ein untergeordnetes icontextnode-Objekt, das nur Informationen über Typ, Bezeichner und Speicherort enthält.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Icontextnode:: kreatepartiallypopulatedsubnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862723"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="e6c3b-103">Icontextnode:: kreatepartiallypopulatedsubnode-Methode</span><span class="sxs-lookup"><span data-stu-id="e6c3b-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="e6c3b-104">Erstellt ein untergeordnetes [**icontextnode**](icontextnode.md) -Objekt, das nur Informationen über Typ, Bezeichner und Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6c3b-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="e6c3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6c3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c3b-107">*pnodetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c3b-108">Der Typ des zu erstellenden Kontext Knotens.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="e6c3b-109">*pnodeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c3b-110">Der Bezeichner für den neuen Knoten.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="e6c3b-111">*pnodelokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c3b-112">Der Speicherort des neuen Knotens.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="e6c3b-113">*ppartiallypopulatedcontextnode created* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c3b-114">Ein Zeiger auf den neuen, teilweise aufgefüllten [**icontextnode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e6c3b-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c3b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6c3b-115">Return value</span></span>

<span data-ttu-id="e6c3b-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e6c3b-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c3b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6c3b-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e6c3b-118">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppartiallypopulatedcontextnodecreated* aufrufen, wenn Sie den Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="e6c3b-119">Der neue [**icontextnode**](icontextnode.md) wird der Auflistung von untergeordneten Knoten dieses Kontext Knotens hinzugefügt (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="e6c3b-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="e6c3b-120">Wenn vorhandene untergeordnete Knoten vorhanden sind, wird der neu erstellte **icontextnode** als letzter untergeordneter Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="e6c3b-121">Weitere Informationen zu Typ, Bezeichner und Speicherort finden Sie unter [**icontextnode:: GetType**](icontextnode-gettype.md), [**icontextnode:: GetId**](icontextnode-getid.md)und [**icontextnode:: getLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="e6c3b-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="e6c3b-122">Diese Methode wird für Daten Proxys als Möglichkeit zum Erstellen eines [**icontextnode**](icontextnode.md) -Objekts in der Kontext Knoten Struktur verwendet, bevor alle Informationen über diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e6c3b-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="e6c3b-123">Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e6c3b-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c3b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6c3b-124">Requirements</span></span>



| <span data-ttu-id="e6c3b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6c3b-125">Requirement</span></span> | <span data-ttu-id="e6c3b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e6c3b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c3b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6c3b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c3b-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6c3b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6c3b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c3b-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e6c3b-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e6c3b-131">Header</span><span class="sxs-lookup"><span data-stu-id="e6c3b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c3b-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c3b-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e6c3b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c3b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c3b-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c3b-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e6c3b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6c3b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c3b-136">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="e6c3b-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e6c3b-137">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="e6c3b-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e6c3b-138">**Icontextnode:: getpartiallyaufgefüllt**</span><span class="sxs-lookup"><span data-stu-id="e6c3b-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="e6c3b-139">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="e6c3b-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="e6c3b-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e6c3b-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


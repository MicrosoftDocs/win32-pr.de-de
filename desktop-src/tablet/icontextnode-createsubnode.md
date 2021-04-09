---
description: Erstellt ein neues untergeordnetes icontextnode-Objekt.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Icontextnode:: kreatesubnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862720"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="c8855-103">Icontextnode:: kreatesubnode-Methode</span><span class="sxs-lookup"><span data-stu-id="c8855-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="c8855-104">Erstellt ein neues untergeordnetes [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c8855-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8855-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8855-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="c8855-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8855-107">*pnodetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8855-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8855-108">Eine **GUID** , die den Typ des zu erstellenden [**icontextnode**](icontextnode.md) darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8855-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="c8855-109">*ppcontextnode created* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c8855-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8855-110">Ein Zeiger auf den neuen [**icontextnode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="c8855-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8855-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8855-111">Return value</span></span>

<span data-ttu-id="c8855-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8855-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8855-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8855-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c8855-114">Um einen Speichermangel zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppcontextnodecreated* , wenn Sie den Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8855-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="c8855-115">Der neue [**icontextnode**](icontextnode.md) wird der Auflistung von untergeordneten Knoten dieses Kontext Knotens hinzugefügt (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="c8855-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="c8855-116">Wenn vorhandene untergeordnete Knoten vorhanden sind, wird der neu erstellte **icontextnode** als letzter untergeordneter Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c8855-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="c8855-117">Eine Liste der Kontext Knoten Typen finden Sie unter [Kontext Knoten Typen](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="c8855-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8855-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8855-118">Requirements</span></span>



| <span data-ttu-id="c8855-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8855-119">Requirement</span></span> | <span data-ttu-id="c8855-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c8855-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8855-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8855-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8855-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8855-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8855-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8855-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8855-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8855-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c8855-125">Header</span><span class="sxs-lookup"><span data-stu-id="c8855-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8855-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c8855-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8855-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c8855-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8855-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8855-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c8855-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8855-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8855-130">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="c8855-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c8855-131">**Icontextnode::D eletesubnode**</span><span class="sxs-lookup"><span data-stu-id="c8855-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="c8855-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="c8855-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


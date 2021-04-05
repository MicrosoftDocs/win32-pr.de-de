---
description: Verschiebt dieses icontextnode-Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Icontextnode:: Analyse-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041766"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="104fe-103">Icontextnode:: Analyse-Methode</span><span class="sxs-lookup"><span data-stu-id="104fe-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="104fe-104">Verschiebt dieses [**icontextnode**](icontextnode.md) -Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.</span><span class="sxs-lookup"><span data-stu-id="104fe-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="104fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="104fe-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="104fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="104fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104fe-107">*pnewparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="104fe-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104fe-108">Der neue übergeordnete Knoten für dieses [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="104fe-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104fe-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="104fe-109">Return value</span></span>

<span data-ttu-id="104fe-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="104fe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="104fe-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="104fe-111">Requirements</span></span>



| <span data-ttu-id="104fe-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="104fe-112">Requirement</span></span> | <span data-ttu-id="104fe-113">Wert</span><span class="sxs-lookup"><span data-stu-id="104fe-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="104fe-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="104fe-114">Minimum supported client</span></span><br/> | <span data-ttu-id="104fe-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="104fe-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="104fe-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="104fe-116">Minimum supported server</span></span><br/> | <span data-ttu-id="104fe-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="104fe-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="104fe-118">Header</span><span class="sxs-lookup"><span data-stu-id="104fe-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="104fe-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="104fe-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="104fe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="104fe-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="104fe-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="104fe-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="104fe-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="104fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104fe-123">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="104fe-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="104fe-124">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="104fe-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="104fe-125">**Icontextnode:: getsubnodes**</span><span class="sxs-lookup"><span data-stu-id="104fe-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="104fe-126">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="104fe-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





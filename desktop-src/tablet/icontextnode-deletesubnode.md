---
description: Entfernt einen untergeordneten icontextnode.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: Icontextnode::D eletesubnode-Methode (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526531"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="84093-103">Icontextnode::D eletesubnode-Methode</span><span class="sxs-lookup"><span data-stu-id="84093-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="84093-104">Entfernt einen untergeordneten [**icontextnode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="84093-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84093-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84093-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="84093-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84093-107">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84093-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84093-108">Der [**icontextnode**](icontextnode.md) , der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84093-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84093-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84093-109">Return value</span></span>

<span data-ttu-id="84093-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="84093-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84093-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84093-111">Remarks</span></span>

<span data-ttu-id="84093-112">E \_ invalidArg wird zurückgegeben, wenn der *pcontextnodebug* -Parameter kein untergeordnetes Element dieses [**icontextnode**](icontextnode.md) -Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="84093-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="84093-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84093-113">Requirements</span></span>



| <span data-ttu-id="84093-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84093-114">Requirement</span></span> | <span data-ttu-id="84093-115">Wert</span><span class="sxs-lookup"><span data-stu-id="84093-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84093-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84093-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84093-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84093-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84093-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84093-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84093-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="84093-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="84093-120">Header</span><span class="sxs-lookup"><span data-stu-id="84093-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84093-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="84093-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="84093-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84093-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84093-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84093-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="84093-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84093-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84093-125">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="84093-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="84093-126">**Icontextnode:: "kreatesubnode"**</span><span class="sxs-lookup"><span data-stu-id="84093-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="84093-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="84093-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





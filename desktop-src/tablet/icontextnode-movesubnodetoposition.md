---
description: Ordnet ein angegebenes untergeordnetes icontextnode-Objekt an den angegebenen Index zurück.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Icontextnode:: muvesubnodetoposition-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343315"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="3a7ed-103">Icontextnode:: muvesubnodetoposition-Methode</span><span class="sxs-lookup"><span data-stu-id="3a7ed-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="3a7ed-104">Ordnet ein angegebenes untergeordnetes [**icontextnode**](icontextnode.md) -Objekt an den angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="3a7ed-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a7ed-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="3a7ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a7ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a7ed-107">*psubnoabtomove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a7ed-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7ed-108">Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a7ed-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="3a7ed-109">*ulnetwindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a7ed-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7ed-110">Der Index für die neue Position des unter Knotens.</span><span class="sxs-lookup"><span data-stu-id="3a7ed-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a7ed-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a7ed-111">Return value</span></span>

<span data-ttu-id="3a7ed-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3a7ed-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a7ed-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a7ed-113">Remarks</span></span>

<span data-ttu-id="3a7ed-114">Gibt " **E \_ invalidArg** " zurück, wenn " *psubnoenttomove* " kein untergeordneter Knoten dieses [**icontextnode**](icontextnode.md)ist.</span><span class="sxs-lookup"><span data-stu-id="3a7ed-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7ed-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a7ed-115">Requirements</span></span>



| <span data-ttu-id="3a7ed-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a7ed-116">Requirement</span></span> | <span data-ttu-id="3a7ed-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3a7ed-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7ed-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a7ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7ed-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a7ed-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3a7ed-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a7ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7ed-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a7ed-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3a7ed-122">Header</span><span class="sxs-lookup"><span data-stu-id="3a7ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a7ed-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ed-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3a7ed-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3a7ed-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a7ed-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ed-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3a7ed-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a7ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a7ed-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="3a7ed-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3a7ed-128">**Icontextnode:: "kreatesubnode"**</span><span class="sxs-lookup"><span data-stu-id="3a7ed-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="3a7ed-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="3a7ed-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





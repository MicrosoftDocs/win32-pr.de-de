---
description: Ruft einen lesbaren Typnamen dieses icontextnode ab.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'Icontextnode:: gettypame-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129492"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="c5a7c-103">Icontextnode:: gettypame-Methode</span><span class="sxs-lookup"><span data-stu-id="c5a7c-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="c5a7c-104">Ruft einen lesbaren Typnamen dieses [**icontextnode**](icontextnode.md)ab.</span><span class="sxs-lookup"><span data-stu-id="c5a7c-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5a7c-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="c5a7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5a7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a7c-107">*pbstraucontextnodetype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5a7c-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a7c-108">Ein lesbarer Typname dieses [**icontextnode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="c5a7c-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a7c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5a7c-109">Return value</span></span>

<span data-ttu-id="c5a7c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c5a7c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a7c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5a7c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c5a7c-112">Um einen Speichermangel zu vermeiden, nennen Sie [**sysfrestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für \* *pbstraucontextnodetype* , wenn Sie die Zeichenfolge nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="c5a7c-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="c5a7c-113">Diese Methode legt z. *b. pbstraucontextnodetype* für einen Ink Word-Knoten auf "InkWordNode" fest (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="c5a7c-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a7c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5a7c-114">Requirements</span></span>



| <span data-ttu-id="c5a7c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5a7c-115">Requirement</span></span> | <span data-ttu-id="c5a7c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c5a7c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a7c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5a7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a7c-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5a7c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c5a7c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5a7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a7c-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5a7c-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c5a7c-121">Header</span><span class="sxs-lookup"><span data-stu-id="c5a7c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a7c-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a7c-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c5a7c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c5a7c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5a7c-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5a7c-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c5a7c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5a7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a7c-126">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="c5a7c-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c5a7c-127">**Icontextnode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="c5a7c-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="c5a7c-128">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="c5a7c-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="c5a7c-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="c5a7c-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Die AddAfter-Methode fügt eine Liste nach der angegebenen Position ein und verwendet die Parameter "POS" und "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Cgenericlist. AddAfter-Methode (wxlist. h)-POS, plist-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531106"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="f0283-103">Cgenericlist. AddAfter-Methode (wxlist. h)-POS, plist-Parameter</span><span class="sxs-lookup"><span data-stu-id="f0283-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="f0283-104">Die- `AddAfter` Methode fügt eine Liste nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="f0283-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0283-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0283-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="f0283-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0283-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0283-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="f0283-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="f0283-108">Position zum Einfügen der Liste.</span><span class="sxs-lookup"><span data-stu-id="f0283-108">Position to insert the list.</span></span> <span data-ttu-id="f0283-109">Die Liste wird nach dieser Position eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f0283-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="f0283-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="f0283-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="f0283-111">Ein Zeiger auf die einzufügende Liste.</span><span class="sxs-lookup"><span data-stu-id="f0283-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0283-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0283-112">Return value</span></span>

<span data-ttu-id="f0283-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f0283-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0283-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0283-114">Requirements</span></span>

| <span data-ttu-id="f0283-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0283-115">Requirement</span></span> | <span data-ttu-id="f0283-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f0283-116">Value</span></span> |
|-|-|
| <span data-ttu-id="f0283-117">Header</span><span class="sxs-lookup"><span data-stu-id="f0283-117">Header</span></span> | <span data-ttu-id="f0283-118">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="f0283-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="f0283-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0283-119">Library</span></span>| <span data-ttu-id="f0283-120">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="f0283-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f0283-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0283-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0283-122">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0283-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





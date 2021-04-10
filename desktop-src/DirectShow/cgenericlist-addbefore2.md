---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein. Diese Methode verwendet die Parameter "POS" und "plist".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Cgenericlist. AddBefore-Methode (wxlist. h)-POS, plist-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762423"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="28849-104">Cgenericlist. AddBefore-Methode (wxlist. h)-POS, plist-Parameter</span><span class="sxs-lookup"><span data-stu-id="28849-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="28849-105">Die- `AddBefore` Methode fügt eine Liste vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="28849-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="28849-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="28849-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="28849-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="28849-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28849-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="28849-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="28849-109">Position zum Einfügen der Liste.</span><span class="sxs-lookup"><span data-stu-id="28849-109">Position to insert the list.</span></span> <span data-ttu-id="28849-110">Die Liste wird vor dieser Position eingefügt.</span><span class="sxs-lookup"><span data-stu-id="28849-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="28849-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="28849-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="28849-112">Ein Zeiger auf die einzufügende Liste.</span><span class="sxs-lookup"><span data-stu-id="28849-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28849-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28849-113">Return value</span></span>

<span data-ttu-id="28849-114">Gibt **true** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="28849-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="28849-115">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28849-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28849-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28849-116">Requirements</span></span>

| <span data-ttu-id="28849-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28849-117">Requirement</span></span> | <span data-ttu-id="28849-118">Wert</span><span class="sxs-lookup"><span data-stu-id="28849-118">Value</span></span> |
|-|-|
| <span data-ttu-id="28849-119">Header</span><span class="sxs-lookup"><span data-stu-id="28849-119">Header</span></span> | <span data-ttu-id="28849-120">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="28849-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="28849-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28849-121">Library</span></span>| <span data-ttu-id="28849-122">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="28849-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="28849-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28849-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28849-124">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="28849-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





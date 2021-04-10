---
description: Die AddBefore-Methode fügt ein Element vor der angegebenen Position ein. Diese Methode verwendet die Parameter "p" und "pobj".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Cgenericlist. AddBefore-Methode (wxlist. h)-p, pobj-Parameter
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961786"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="b942a-104">Cgenericlist. AddBefore-Methode (wxlist. h)-p, pobj-Parameter</span><span class="sxs-lookup"><span data-stu-id="b942a-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="b942a-105">Die- `AddBefore` Methode fügt ein Element vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="b942a-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b942a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b942a-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="b942a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b942a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b942a-108">*cker*</span><span class="sxs-lookup"><span data-stu-id="b942a-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="b942a-109">Die Position, an der die Liste eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b942a-109">Position before which to insert the list.</span></span> <span data-ttu-id="b942a-110">Wenn *p* **null** ist, fügt diese Methode das Element am Ende der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="b942a-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="b942a-111">*pobj*</span><span class="sxs-lookup"><span data-stu-id="b942a-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="b942a-112">Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="b942a-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b942a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b942a-113">Return value</span></span>

<span data-ttu-id="b942a-114">Gibt den Positionsindikator für das eingefügte Element zurück.</span><span class="sxs-lookup"><span data-stu-id="b942a-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="b942a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b942a-115">Requirements</span></span>

| <span data-ttu-id="b942a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b942a-116">Requirement</span></span> | <span data-ttu-id="b942a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b942a-117">Value</span></span> |
|-|-|
| <span data-ttu-id="b942a-118">Header</span><span class="sxs-lookup"><span data-stu-id="b942a-118">Header</span></span> | <span data-ttu-id="b942a-119">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="b942a-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="b942a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b942a-120">Library</span></span>| <span data-ttu-id="b942a-121">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="b942a-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b942a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b942a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b942a-123">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b942a-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





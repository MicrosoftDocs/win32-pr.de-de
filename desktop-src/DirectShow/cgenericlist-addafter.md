---
description: Die AddAfter-Methode fügt ein Element nach der angegebenen Position ein und verwendet die Parameter "p" und "pobj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Cgenericlist. AddAfter-Methode (wxlist. h)-p, pobj-Parameter
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356156"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="a1b23-103">Cgenericlist. AddAfter-Methode (wxlist. h)-p, pobj-Parameter</span><span class="sxs-lookup"><span data-stu-id="a1b23-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="a1b23-104">Die- `AddAfter` Methode fügt ein Element nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="a1b23-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1b23-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="a1b23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1b23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b23-107">*cker*</span><span class="sxs-lookup"><span data-stu-id="a1b23-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b23-108">Die Position, an der das Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1b23-108">Position after which to add the item.</span></span> <span data-ttu-id="a1b23-109">Wenn *p* **null** ist, fügt die Methode das Element am Anfang der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1b23-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="a1b23-110">*pobj*</span><span class="sxs-lookup"><span data-stu-id="a1b23-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b23-111">Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="a1b23-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b23-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1b23-112">Return value</span></span>

<span data-ttu-id="a1b23-113">Gibt den Positionsindikator des eingefügten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="a1b23-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b23-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1b23-114">Requirements</span></span>

| <span data-ttu-id="a1b23-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1b23-115">Requirement</span></span> | <span data-ttu-id="a1b23-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a1b23-116">Value</span></span> |
|-|-|
| <span data-ttu-id="a1b23-117">Header</span><span class="sxs-lookup"><span data-stu-id="a1b23-117">Header</span></span> | <span data-ttu-id="a1b23-118">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="a1b23-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="a1b23-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a1b23-119">Library</span></span>| <span data-ttu-id="a1b23-120">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="a1b23-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a1b23-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1b23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b23-122">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a1b23-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





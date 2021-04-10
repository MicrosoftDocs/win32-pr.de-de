---
description: Die AddHead-Methode fügt ein Element am Anfang der Liste hinzu.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Cgenericlist. AddHead-Methode (wxlist. h)-pobj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104050954"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="f1f16-103">Cgenericlist. AddHead-Methode (wxlist. h)-pobj-Parameter</span><span class="sxs-lookup"><span data-stu-id="f1f16-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="f1f16-104">Mit der- `AddHead` Methode wird ein Element am Anfang der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1f16-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1f16-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="f1f16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f16-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="f1f16-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="f1f16-108">Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="f1f16-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f16-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1f16-109">Return value</span></span>

<span data-ttu-id="f1f16-110">Gibt einen Positionswert zurück, der die neue Head-Position angibt.</span><span class="sxs-lookup"><span data-stu-id="f1f16-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="f1f16-111">Wenn die Methode fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="f1f16-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f16-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1f16-112">Requirements</span></span>

| <span data-ttu-id="f1f16-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1f16-113">Requirement</span></span> | <span data-ttu-id="f1f16-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f1f16-114">Value</span></span> |
|-|-|
| <span data-ttu-id="f1f16-115">Header</span><span class="sxs-lookup"><span data-stu-id="f1f16-115">Header</span></span> | <span data-ttu-id="f1f16-116">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="f1f16-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="f1f16-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1f16-117">Library</span></span>| <span data-ttu-id="f1f16-118">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="f1f16-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f1f16-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1f16-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f16-120">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f1f16-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





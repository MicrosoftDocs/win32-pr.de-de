---
description: Die AddTail-Methode fügt ein Element am Ende der Liste an.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Cgenericlist. AddTail-Methode (wxlist. h)-pobj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365877"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="ee99e-103">Cgenericlist. AddTail-Methode (wxlist. h)-pobj-Parameter</span><span class="sxs-lookup"><span data-stu-id="ee99e-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="ee99e-104">Die- `AddTail` Methode fügt ein Element am Ende der Liste an.</span><span class="sxs-lookup"><span data-stu-id="ee99e-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee99e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee99e-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="ee99e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee99e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee99e-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="ee99e-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="ee99e-108">Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).</span><span class="sxs-lookup"><span data-stu-id="ee99e-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee99e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee99e-109">Return value</span></span>

<span data-ttu-id="ee99e-110">Gibt einen Positionswert für die neue Endposition zurück.</span><span class="sxs-lookup"><span data-stu-id="ee99e-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="ee99e-111">Wenn die Methode fehlschlägt, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee99e-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee99e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee99e-112">Requirements</span></span>

| <span data-ttu-id="ee99e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee99e-113">Requirement</span></span> | <span data-ttu-id="ee99e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ee99e-114">Value</span></span> |
|-|-|
| <span data-ttu-id="ee99e-115">Header</span><span class="sxs-lookup"><span data-stu-id="ee99e-115">Header</span></span> | <span data-ttu-id="ee99e-116">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="ee99e-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ee99e-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee99e-117">Library</span></span>| <span data-ttu-id="ee99e-118">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="ee99e-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ee99e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee99e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee99e-120">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ee99e-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





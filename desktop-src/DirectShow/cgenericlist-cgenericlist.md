---
description: Erfahren Sie mehr über die Konstruktormethode für cgenericlist. cgenericlist (wxlist. h). Diese Methode verwendet die Parameter "pname" und "IItems".
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Cgenericlist. cgenericlist-Konstruktor (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356197"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="0f3d8-104">Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName, IItems-Parameter</span><span class="sxs-lookup"><span data-stu-id="0f3d8-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="0f3d8-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f3d8-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="0f3d8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f3d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3d8-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="0f3d8-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0f3d8-109">Zeiger auf den Namen der Liste.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="0f3d8-110">*IItems*</span><span class="sxs-lookup"><span data-stu-id="0f3d8-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="0f3d8-111">Größe des Knoten Caches.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="0f3d8-112">*Baustein*</span><span class="sxs-lookup"><span data-stu-id="0f3d8-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0f3d8-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f3d8-114">*balert*</span><span class="sxs-lookup"><span data-stu-id="0f3d8-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="0f3d8-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f3d8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f3d8-116">Remarks</span></span>

<span data-ttu-id="0f3d8-117">Aus Effizienzgründen verwaltet die- `CGenericList` Klasse einen Cache von Listen Knoten.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="0f3d8-118">Wenn Sie ungefähr wissen, wie viele Elemente in der Liste enthalten sein werden, verwenden Sie diese Version des Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="0f3d8-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3d8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f3d8-119">Requirements</span></span>

| <span data-ttu-id="0f3d8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f3d8-120">Requirement</span></span> | <span data-ttu-id="0f3d8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0f3d8-121">Value</span></span> |
|-|-|
| <span data-ttu-id="0f3d8-122">Header</span><span class="sxs-lookup"><span data-stu-id="0f3d8-122">Header</span></span> | <span data-ttu-id="0f3d8-123">Wxlist. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="0f3d8-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="0f3d8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f3d8-124">Library</span></span>| <span data-ttu-id="0f3d8-125">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="0f3d8-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0f3d8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f3d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3d8-127">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f3d8-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





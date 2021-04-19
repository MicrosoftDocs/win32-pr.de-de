---
description: Die getallocatorrequirements-Methode ruft die von der eingabepin angeforderten zuordnereigenschaften ab.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Cbaseinputpin. getalloovorrequirements-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352898"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="3b413-103">Cbaseinputpin. getalloovorrequirements-Methode</span><span class="sxs-lookup"><span data-stu-id="3b413-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="3b413-104">Die- `GetAllocatorRequirements` Methode ruft die von der eingabepin angeforderten zuordnereigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="3b413-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b413-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b413-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="3b413-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b413-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b413-107">*p-Eigenschaften*</span><span class="sxs-lookup"><span data-stu-id="3b413-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="3b413-108">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die mit den Anforderungen ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3b413-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b413-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b413-109">Return value</span></span>

<span data-ttu-id="3b413-110">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="3b413-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b413-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b413-111">Remarks</span></span>

<span data-ttu-id="3b413-112">Wenn eine Ausgabe-PIN eine Speicherzuweisung initialisiert, kann diese Methode aufgerufen werden, um zu bestimmen, ob die Eingabe-PIN über Puffer Anforderungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="3b413-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="3b413-113">Weitere Informationen finden Sie unter [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3b413-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="3b413-114">Das Implementieren dieser Methode ist optional.</span><span class="sxs-lookup"><span data-stu-id="3b413-114">Implementing this method is optional.</span></span> <span data-ttu-id="3b413-115">Wenn der Filter bestimmte Ausrichtung oder Präfix Anforderungen aufweist, überschreiben Sie diese Methode.</span><span class="sxs-lookup"><span data-stu-id="3b413-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b413-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b413-116">Requirements</span></span>



| <span data-ttu-id="3b413-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b413-117">Requirement</span></span> | <span data-ttu-id="3b413-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3b413-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b413-119">Header</span><span class="sxs-lookup"><span data-stu-id="3b413-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3b413-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b413-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3b413-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3b413-121">Library</span></span><br/> | <dl> <span data-ttu-id="3b413-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3b413-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b413-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b413-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b413-124">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3b413-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 





---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen fest.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Cbaseoutputpin. decidebuffersize-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352094"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="b3cb0-103">Cbaseoutputpin. decidebuffersize-Methode</span><span class="sxs-lookup"><span data-stu-id="b3cb0-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="b3cb0-104">Die- `DecideBufferSize` Methode legt die Puffer Anforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3cb0-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b3cb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3cb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3cb0-107">*palloc*</span><span class="sxs-lookup"><span data-stu-id="b3cb0-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b3cb0-108">Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b3cb0-109">*ppropinputrequest*</span><span class="sxs-lookup"><span data-stu-id="b3cb0-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="b3cb0-110">Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="b3cb0-111">Wenn die Eingabe-PIN keine Anforderungen hat, sollte der Aufrufer die Elemente dieser Struktur vor dem Aufrufen der-Methode 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b3cb0-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3cb0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3cb0-112">Return value</span></span>

<span data-ttu-id="b3cb0-113">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cb0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3cb0-114">Remarks</span></span>

<span data-ttu-id="b3cb0-115">Überschreiben Sie diese Methode in der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-115">Override this method in your derived class.</span></span> <span data-ttu-id="b3cb0-116">Aufrufen der [**imemzuzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) -Methode, um die Puffer Anforderungen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="b3cb0-117">In der Regel berücksichtigt die abgeleitete Klasse die Puffer Anforderungen der Eingabe-PIN, Sie ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3cb0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3cb0-118">Requirements</span></span>



| <span data-ttu-id="b3cb0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3cb0-119">Requirement</span></span> | <span data-ttu-id="b3cb0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b3cb0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cb0-121">Header</span><span class="sxs-lookup"><span data-stu-id="b3cb0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b3cb0-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3cb0-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3cb0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3cb0-123">Library</span></span><br/> | <dl> <span data-ttu-id="b3cb0-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b3cb0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3cb0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3cb0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3cb0-126">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b3cb0-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





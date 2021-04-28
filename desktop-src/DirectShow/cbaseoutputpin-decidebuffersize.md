---
description: 'CBaseOutputPin.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen fest.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: CBaseOutputPin.DecideBufferSize-Methode (Amfilter.h)
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
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099528"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="7bad6-103">CBaseOutputPin.DecideBufferSize-Methode</span><span class="sxs-lookup"><span data-stu-id="7bad6-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="7bad6-104">Die `DecideBufferSize` -Methode legt die Pufferanforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="7bad6-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bad6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bad6-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="7bad6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bad6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bad6-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="7bad6-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="7bad6-108">Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="7bad6-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7bad6-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="7bad6-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="7bad6-110">Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen des Eingabepins enthält.</span><span class="sxs-lookup"><span data-stu-id="7bad6-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="7bad6-111">Wenn der Eingabepin keine Anforderungen hat, sollte der Aufrufer die Member dieser Struktur vor dem Aufrufen der -Methode auf null setzen.</span><span class="sxs-lookup"><span data-stu-id="7bad6-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bad6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bad6-112">Return value</span></span>

<span data-ttu-id="7bad6-113">Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="7bad6-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bad6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bad6-114">Remarks</span></span>

<span data-ttu-id="7bad6-115">Überschreiben Sie diese Methode in der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="7bad6-115">Override this method in your derived class.</span></span> <span data-ttu-id="7bad6-116">Rufen Sie die [**IMemAllocator::SetProperties-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) auf, um Ihre Pufferanforderungen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7bad6-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="7bad6-117">In der Regel berücksichtigt die abgeleitete Klasse die Pufferanforderungen des Eingabepins, dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7bad6-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bad6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bad6-118">Requirements</span></span>



| <span data-ttu-id="7bad6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bad6-119">Requirement</span></span> | <span data-ttu-id="7bad6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7bad6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bad6-121">Header</span><span class="sxs-lookup"><span data-stu-id="7bad6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7bad6-122"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7bad6-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7bad6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bad6-123">Library</span></span><br/> | <dl> <span data-ttu-id="7bad6-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7bad6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bad6-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7bad6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bad6-126">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7bad6-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





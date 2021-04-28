---
description: 'CTransformOutputPin.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen fest.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: CTransformOutputPin.DecideBufferSize-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084838"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="e223d-103">CTransformOutputPin.DecideBufferSize-Methode</span><span class="sxs-lookup"><span data-stu-id="e223d-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="e223d-104">Die `DecideBufferSize` -Methode legt die Pufferanforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="e223d-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e223d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e223d-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="e223d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e223d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e223d-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="e223d-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="e223d-108">Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="e223d-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e223d-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="e223d-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="e223d-110">Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen des Eingabepins enthält.</span><span class="sxs-lookup"><span data-stu-id="e223d-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e223d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e223d-111">Return value</span></span>

<span data-ttu-id="e223d-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="e223d-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e223d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e223d-113">Remarks</span></span>

<span data-ttu-id="e223d-114">Diese Methode überschreibt die [**CBaseOutputPin::D ecideBufferSize-Methode.**](cbaseoutputpin-decidebuffersize.md)</span><span class="sxs-lookup"><span data-stu-id="e223d-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="e223d-115">Sie ruft die rein virtuelle [**CTransformFilter::D ecideBufferSize-Methode**](ctransformfilter-decidebuffersize.md) des Filters auf, die die abgeleitete Klasse des Filters implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="e223d-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="e223d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e223d-116">Requirements</span></span>



| <span data-ttu-id="e223d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e223d-117">Requirement</span></span> | <span data-ttu-id="e223d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e223d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e223d-119">Header</span><span class="sxs-lookup"><span data-stu-id="e223d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e223d-120"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e223d-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e223d-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e223d-121">Library</span></span><br/> | <dl> <span data-ttu-id="e223d-122"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e223d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





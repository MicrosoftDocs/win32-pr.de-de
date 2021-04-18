---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen fest.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Ctransformoutputpin. decidebuffersize-Methode (Transfrm. h)
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372181"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="06c64-103">Ctransformoutputpin. decidebuffersize-Methode</span><span class="sxs-lookup"><span data-stu-id="06c64-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="06c64-104">Die- `DecideBufferSize` Methode legt die Puffer Anforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="06c64-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c64-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06c64-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="06c64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c64-107">*palloc*</span><span class="sxs-lookup"><span data-stu-id="06c64-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="06c64-108">Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="06c64-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="06c64-109">*ppropinputrequest*</span><span class="sxs-lookup"><span data-stu-id="06c64-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="06c64-110">Zeiger eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="06c64-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c64-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06c64-111">Return value</span></span>

<span data-ttu-id="06c64-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06c64-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c64-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06c64-113">Remarks</span></span>

<span data-ttu-id="06c64-114">Diese Methode überschreibt die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="06c64-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="06c64-115">Sie ruft die rein virtuelle [**ctransformfilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) -Methode des Filters auf, die von der abgeleiteten Klasse des Filters implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="06c64-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c64-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c64-116">Requirements</span></span>



| <span data-ttu-id="06c64-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06c64-117">Requirement</span></span> | <span data-ttu-id="06c64-118">Wert</span><span class="sxs-lookup"><span data-stu-id="06c64-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c64-119">Header</span><span class="sxs-lookup"><span data-stu-id="06c64-119">Header</span></span><br/>  | <dl> <span data-ttu-id="06c64-120"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06c64-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06c64-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06c64-121">Library</span></span><br/> | <dl> <span data-ttu-id="06c64-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="06c64-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





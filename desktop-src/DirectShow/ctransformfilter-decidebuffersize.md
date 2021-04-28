---
description: 'CTransformFilter.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen des Ausgabepins fest.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: CTransformFilter.DecideBufferSize-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095148"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="a71ee-103">CTransformFilter.DecideBufferSize-Methode</span><span class="sxs-lookup"><span data-stu-id="a71ee-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="a71ee-104">Die `DecideBufferSize` -Methode legt die Pufferanforderungen des Ausgabepins fest.</span><span class="sxs-lookup"><span data-stu-id="a71ee-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a71ee-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a71ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a71ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="a71ee-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="a71ee-108">Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) auf der Zuweisung des Ausgabepins.</span><span class="sxs-lookup"><span data-stu-id="a71ee-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="a71ee-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a71ee-110">Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die Pufferanforderungen des downstream-Eingabepins enthält.</span><span class="sxs-lookup"><span data-stu-id="a71ee-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a71ee-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a71ee-111">Return value</span></span>

<span data-ttu-id="a71ee-112">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="a71ee-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a71ee-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a71ee-113">Remarks</span></span>

<span data-ttu-id="a71ee-114">Die [**CTransformOutputPin::D ecideBufferSize-Methode**](ctransformoutputpin-decidebuffersize.md) des Ausgabepins ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a71ee-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="a71ee-115">Die abgeleitete Klasse muss diese Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="a71ee-115">The derived class must implement this method.</span></span> <span data-ttu-id="a71ee-116">Weitere Informationen finden Sie unter [**CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="a71ee-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a71ee-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a71ee-117">Requirements</span></span>



| <span data-ttu-id="a71ee-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a71ee-118">Requirement</span></span> | <span data-ttu-id="a71ee-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a71ee-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71ee-120">Header</span><span class="sxs-lookup"><span data-stu-id="a71ee-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a71ee-121"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a71ee-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a71ee-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a71ee-122">Library</span></span><br/> | <dl> <span data-ttu-id="a71ee-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a71ee-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a71ee-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a71ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71ee-125">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a71ee-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





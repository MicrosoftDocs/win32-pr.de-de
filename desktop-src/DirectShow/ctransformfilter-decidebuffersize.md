---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Ctransformfilter. decidebuffersize-Methode (Transfrm. h)
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
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371148"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="b2a00-103">Ctransformfilter. decidebuffersize-Methode</span><span class="sxs-lookup"><span data-stu-id="b2a00-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="b2a00-104">Die `DecideBufferSize` -Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.</span><span class="sxs-lookup"><span data-stu-id="b2a00-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2a00-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b2a00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2a00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a00-107">*palloc*</span><span class="sxs-lookup"><span data-stu-id="b2a00-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b2a00-108">Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle für die Zuweisung der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="b2a00-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="b2a00-109">*ppropinputrequest*</span><span class="sxs-lookup"><span data-stu-id="b2a00-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="b2a00-110">Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur, die Puffer Anforderungen aus der nachgeschalteten Eingabe-PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="b2a00-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a00-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2a00-111">Return value</span></span>

<span data-ttu-id="b2a00-112">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2a00-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a00-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2a00-113">Remarks</span></span>

<span data-ttu-id="b2a00-114">Die [**ctransformoutputpin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) -Methode der Ausgabe-PIN ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b2a00-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="b2a00-115">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2a00-115">The derived class must implement this method.</span></span> <span data-ttu-id="b2a00-116">Weitere Informationen finden Sie unter [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="b2a00-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a00-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2a00-117">Requirements</span></span>



| <span data-ttu-id="b2a00-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2a00-118">Requirement</span></span> | <span data-ttu-id="b2a00-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b2a00-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a00-120">Header</span><span class="sxs-lookup"><span data-stu-id="b2a00-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b2a00-121"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2a00-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2a00-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2a00-122">Library</span></span><br/> | <dl> <span data-ttu-id="b2a00-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b2a00-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2a00-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2a00-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a00-125">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2a00-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





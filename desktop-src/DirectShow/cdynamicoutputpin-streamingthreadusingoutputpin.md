---
description: Die streamingthreadusingoutputpin-Methode bestimmt, ob ein Thread einen Streamingvorgang auf der PIN ausführt.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Cdynamicoutputpin. streamingthreadusingoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352076"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="75d25-103">Cdynamicoutputpin. streamingthreadusingoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="75d25-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="75d25-104">Die streamingthreadusingoutputpin-Methode bestimmt, ob ein Thread einen Streamingvorgang auf der PIN ausführt.</span><span class="sxs-lookup"><span data-stu-id="75d25-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d25-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="75d25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d25-106">Parameters</span></span>

<span data-ttu-id="75d25-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="75d25-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75d25-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75d25-108">Return value</span></span>

<span data-ttu-id="75d25-109">Gibt " **true** " zurück, wenn ein Thread einen Streamingvorgang auf der PIN ausführt.</span><span class="sxs-lookup"><span data-stu-id="75d25-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="75d25-110">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75d25-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d25-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75d25-111">Remarks</span></span>

<span data-ttu-id="75d25-112">Wenn Threads von der [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode erfolgreich zurückgegeben wurden und kein entsprechender Aufrufen der [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode vorgenommen wurden, gibt diese Methode **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="75d25-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d25-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75d25-113">Requirements</span></span>



| <span data-ttu-id="75d25-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75d25-114">Requirement</span></span> | <span data-ttu-id="75d25-115">Wert</span><span class="sxs-lookup"><span data-stu-id="75d25-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d25-116">Header</span><span class="sxs-lookup"><span data-stu-id="75d25-116">Header</span></span><br/>  | <dl> <span data-ttu-id="75d25-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75d25-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75d25-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75d25-118">Library</span></span><br/> | <dl> <span data-ttu-id="75d25-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="75d25-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d25-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75d25-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d25-121">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="75d25-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





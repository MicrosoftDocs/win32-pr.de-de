---
description: Die abortplayback-Methode wird verwendet, um einen Streamingfehler zu signalisieren. Es sendet ein EC \_ errorabort-Ereignis an den Filter Graph-Manager und sendet eine downstreambenachrichtigung.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Cvideotransformfilter. abortplayback-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353794"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="01697-104">Cvideotransformfilter. abortplayback-Methode</span><span class="sxs-lookup"><span data-stu-id="01697-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="01697-105">Die- `AbortPlayback` Methode wird verwendet, um einen Streamingfehler zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="01697-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="01697-106">Es sendet ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an den Filter Graph-Manager und sendet eine downstreambenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="01697-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="01697-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="01697-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="01697-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="01697-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01697-109">*Std.*</span><span class="sxs-lookup"><span data-stu-id="01697-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="01697-110">**HRESULT** -Wert des Vorgangs, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="01697-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="01697-111">Dieser Wert wird als erster Ereignis Parameter für das EC \_ errorabort-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="01697-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01697-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01697-112">Return value</span></span>

<span data-ttu-id="01697-113">Gibt den Wert des *HR* -Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="01697-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="01697-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01697-114">Requirements</span></span>



| <span data-ttu-id="01697-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01697-115">Requirement</span></span> | <span data-ttu-id="01697-116">Wert</span><span class="sxs-lookup"><span data-stu-id="01697-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01697-117">Header</span><span class="sxs-lookup"><span data-stu-id="01697-117">Header</span></span><br/>  | <dl> <span data-ttu-id="01697-118"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01697-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="01697-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01697-119">Library</span></span><br/> | <dl> <span data-ttu-id="01697-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="01697-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01697-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01697-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01697-122">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="01697-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 





---
description: Die Pause-Methode signalisiert, dass der streamingingthread aktiv wird.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Csourcestream. Pause-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371441"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="ea253-103">Csourcestream. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="ea253-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="ea253-104">Die- `Pause` Methode signalisiert, dass der streamingingthread aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="ea253-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea253-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea253-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="ea253-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea253-106">Parameters</span></span>

<span data-ttu-id="ea253-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ea253-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea253-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea253-108">Return value</span></span>

<span data-ttu-id="ea253-109">Gibt \_ OK oder E \_ unerwartet zurück.</span><span class="sxs-lookup"><span data-stu-id="ea253-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea253-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea253-110">Remarks</span></span>

<span data-ttu-id="ea253-111">Die [**csourcestream:: Active**](csourcestream-active.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ea253-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="ea253-112">Wenn die [**csourcestream:: ThreadProc**](csourcestream-threadproc.md) -Methode diese Anforderung empfängt, ruft Sie die [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ea253-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea253-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea253-113">Requirements</span></span>



| <span data-ttu-id="ea253-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea253-114">Requirement</span></span> | <span data-ttu-id="ea253-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ea253-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea253-116">Header</span><span class="sxs-lookup"><span data-stu-id="ea253-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ea253-117"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea253-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ea253-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea253-118">Library</span></span><br/> | <dl> <span data-ttu-id="ea253-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ea253-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea253-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea253-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea253-121">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea253-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





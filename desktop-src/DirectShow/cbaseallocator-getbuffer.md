---
description: 'Die GetBuffer-Methode ruft ein Medien Beispiel ab, das einen Puffer enthält. Diese Methode implementiert die imemzuzucator:: GetBuffer-Methode.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Cbasezucator. GetBuffer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358722"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="a990e-104">Cbasezucator. GetBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="a990e-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="a990e-105">Die- `GetBuffer` Methode ruft ein Medien Beispiel ab, das einen Puffer enthält.</span><span class="sxs-lookup"><span data-stu-id="a990e-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="a990e-106">Diese Methode implementiert die [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a990e-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a990e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a990e-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a990e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a990e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a990e-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="a990e-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a990e-110">Empfängt einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Puffers.</span><span class="sxs-lookup"><span data-stu-id="a990e-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="a990e-111">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="a990e-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a990e-112">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="a990e-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a990e-113">Zeiger auf die Startzeit des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="a990e-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a990e-114">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="a990e-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a990e-115">Zeiger auf die Endzeit der Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="a990e-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a990e-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a990e-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a990e-117">Bitweise Kombination von 0 (null) oder mehr Flags.</span><span class="sxs-lookup"><span data-stu-id="a990e-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="a990e-118">Die Basisklasse unterstützt das folgende Flag.</span><span class="sxs-lookup"><span data-stu-id="a990e-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="a990e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a990e-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="a990e-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a990e-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="a990e-121"><dt>**AM \_ GBF \_ nowait**</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="a990e-122">Warten Sie nicht, bis ein Puffer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="a990e-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a990e-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a990e-123">Return value</span></span>

<span data-ttu-id="a990e-124">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a990e-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="a990e-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a990e-125">Return code</span></span>                                                                                           | <span data-ttu-id="a990e-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a990e-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="a990e-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a990e-128">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a990e-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="a990e-129"><dt>**VFW \_ E \_ nicht committet \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="a990e-130">Ein Commit für die Zuweisung wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a990e-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="a990e-131"><dt>**VFW \_ E \_ Timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="a990e-132">Timeout.</span><span class="sxs-lookup"><span data-stu-id="a990e-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="a990e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a990e-133">Remarks</span></span>

<span data-ttu-id="a990e-134">Wenn der Aufrufer das **am \_ GBF \_ nowait** -Flag nicht in *dwFlags* angibt, wird diese Methode blockiert, bis das nächste Beispiel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a990e-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="a990e-135">Das abgerufene Medien Beispiel verfügt über einen gültigen Zeiger auf den zugeordneten Puffer.</span><span class="sxs-lookup"><span data-stu-id="a990e-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="a990e-136">Der Aufrufer ist dafür verantwortlich, alle anderen Eigenschaften für das Beispiel festzulegen, z. b. die Zeitstempel, die Medien Zeiten oder die Eigenschaft für den Synchronisierungs Punkt.</span><span class="sxs-lookup"><span data-stu-id="a990e-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="a990e-137">Weitere Informationen finden Sie unter [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="a990e-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="a990e-138">In der Basisklasse werden die Parameter *pstarttime* und *pdtime* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a990e-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="a990e-139">Abgeleitete Klassen können diese Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a990e-139">Derived classes can use these values.</span></span> <span data-ttu-id="a990e-140">Beispielsweise verwendet die Zuweisung für den [Videorenderer](video-renderer-filter.md) -Filter diese Werte, um den Wechsel zwischen DirectDraw-Oberflächen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a990e-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="a990e-141">Wenn die Methode auf ein Beispiel warten muss, erhöht Sie die Anzahl der wartenden Objekte ([**cbasezucator:: m \_ lCount**](cbaseallocator-m-lcount.md)) und ruft die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion für das Semaphor auf ([**cbasezuordcator:: m \_ hsem**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="a990e-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="a990e-142">Wenn ein Beispiel verfügbar wird, wird die [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode für die Zuweisung aufgerufen, die die Anzahl der Semaphor um **m \_ lCount** erhöht (wodurch die wartenden Threads freigegeben werden) und **m \_ lCount** auf 0 (null) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a990e-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a990e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a990e-143">Requirements</span></span>



| <span data-ttu-id="a990e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a990e-144">Requirement</span></span> | <span data-ttu-id="a990e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a990e-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a990e-146">Header</span><span class="sxs-lookup"><span data-stu-id="a990e-146">Header</span></span><br/>  | <dl> <span data-ttu-id="a990e-147"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a990e-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a990e-148">Library</span></span><br/> | <dl> <span data-ttu-id="a990e-149">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a990e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a990e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a990e-151">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a990e-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 


---
description: 'Die ReleaseBuffer-Methode gibt ein Medien Beispiel an die Liste der Beispiele für freie Medien zurück. Diese Methode implementiert die imemzuzucator:: ReleaseBuffer-Methode.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Cbasezucator. ReleaseBuffer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371493"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="9552c-104">Cbasezucator. ReleaseBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="9552c-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="9552c-105">Die- `ReleaseBuffer` Methode gibt ein Medien Beispiel zur Liste der Beispiele für freie Medien zurück.</span><span class="sxs-lookup"><span data-stu-id="9552c-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="9552c-106">Diese Methode implementiert die [**imemzuzucator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9552c-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9552c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9552c-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="9552c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9552c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9552c-109">*psample*</span><span class="sxs-lookup"><span data-stu-id="9552c-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9552c-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Medien Beispiel Objekts.</span><span class="sxs-lookup"><span data-stu-id="9552c-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9552c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9552c-111">Return value</span></span>

<span data-ttu-id="9552c-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9552c-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9552c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9552c-113">Remarks</span></span>

<span data-ttu-id="9552c-114">Wenn der Verweis Zähler eines Medien Beispiels Null erreicht, ruft das Beispiel **ReleaseBuffer** mit sich selbst als Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="9552c-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="9552c-115">Diese Methode führt die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="9552c-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="9552c-116">Gibt das Medien Beispiel in der kostenlosen Liste ([**cbasezucator:: m \_ lfree**](cbaseallocator-m-lfree.md)) zurück.</span><span class="sxs-lookup"><span data-stu-id="9552c-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="9552c-117">Ruft die [**cbasezucator:: notifysample**](cbaseallocator-notifysample.md) -Methode auf, die alle Threads freigibt, die bei Aufrufen der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="9552c-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="9552c-118">Wenn die [**cbasedepcator:: setnotify**](cbaseallocator-setnotify.md) -Methode zuvor aufgerufen wurde, ruft die **imemzuzucatornotifycallbacktemp:: notifyrelease** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9552c-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="9552c-119">Wenn das letzte Beispiel freigegeben ist, wenn ein [**ausstehender cbasebelegcator::D ecommit**](cbaseallocator-decommit.md) -Aufruf vorhanden ist, ruft die [**cbasezucator:: Free**](cbaseallocator-free.md) -Methode auf, um den Pufferspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9552c-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="9552c-120">(In der Basisklasse ist **Free** eine rein virtuelle Methode.)</span><span class="sxs-lookup"><span data-stu-id="9552c-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="9552c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9552c-121">Requirements</span></span>



| <span data-ttu-id="9552c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9552c-122">Requirement</span></span> | <span data-ttu-id="9552c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9552c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9552c-124">Header</span><span class="sxs-lookup"><span data-stu-id="9552c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9552c-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9552c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9552c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9552c-126">Library</span></span><br/> | <dl> <span data-ttu-id="9552c-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9552c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9552c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9552c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9552c-129">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9552c-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





---
description: 'Die setmediatime-Methode legt die Medien Zeiten für dieses Beispiel fest. Diese Methode implementiert die imediasample:: setmediatime-Methode.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Cmediasample. setmediatime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357555"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="b3304-104">Cmediasample. setmediatime-Methode</span><span class="sxs-lookup"><span data-stu-id="b3304-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="b3304-105">Die- `SetMediaTime` Methode legt die Medien Zeiten für dieses Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="b3304-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="b3304-106">Diese Methode implementiert die [**imediasample:: setmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b3304-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3304-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3304-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="b3304-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3304-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3304-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="b3304-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b3304-110">Ein Zeiger auf die Start Zeit des Mediums oder **null**.</span><span class="sxs-lookup"><span data-stu-id="b3304-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3304-111">*ausgesetzt*</span><span class="sxs-lookup"><span data-stu-id="b3304-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b3304-112">Ein Zeiger auf die Endzeit des Mediums oder **null**.</span><span class="sxs-lookup"><span data-stu-id="b3304-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3304-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3304-113">Return value</span></span>

<span data-ttu-id="b3304-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b3304-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3304-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3304-115">Remarks</span></span>

<span data-ttu-id="b3304-116">Die Zeit für das Medien Ende muss höher sein als die Start Zeit des Mediums.</span><span class="sxs-lookup"><span data-stu-id="b3304-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="b3304-117">Verwenden Sie **null** , um die Medien Zeiten für ungültig zu erklären.</span><span class="sxs-lookup"><span data-stu-id="b3304-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="b3304-118">Der *Pend* -Parameter gibt eine absolute Medien Zeit an, aber die [**cmediasample:: m \_ mediaend**](cmediasample-m-mediaend.md) -Member-Variable wird als Offset von *PStart* berechnet.</span><span class="sxs-lookup"><span data-stu-id="b3304-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="b3304-119">Anders ausgedrückt: **m \_ mediaend**  =  \* *ptimeend* \* *ptimestart*.  </span><span class="sxs-lookup"><span data-stu-id="b3304-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="b3304-120">Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b3304-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3304-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3304-121">Requirements</span></span>



| <span data-ttu-id="b3304-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3304-122">Requirement</span></span> | <span data-ttu-id="b3304-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b3304-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3304-124">Header</span><span class="sxs-lookup"><span data-stu-id="b3304-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b3304-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3304-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3304-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3304-126">Library</span></span><br/> | <dl> <span data-ttu-id="b3304-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b3304-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3304-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3304-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3304-129">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b3304-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





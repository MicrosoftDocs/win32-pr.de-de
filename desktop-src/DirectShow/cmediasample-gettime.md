---
description: 'Die getTime-Methode ruft die streamzeiten ab, zu denen das Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die imediasample:: getTime-Methode.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Cmediasample. getTime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354033"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="f96cd-104">Cmediasample. getTime-Methode</span><span class="sxs-lookup"><span data-stu-id="f96cd-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="f96cd-105">Die- `GetTime` Methode ruft die streamzeiten ab, zu denen das Beispiel beginnen und fertigstellen soll.</span><span class="sxs-lookup"><span data-stu-id="f96cd-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="f96cd-106">Diese Methode implementiert die [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f96cd-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f96cd-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="f96cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f96cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96cd-109">*ptimestart*</span><span class="sxs-lookup"><span data-stu-id="f96cd-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f96cd-110">Ein Zeiger auf eine Variable, die die beginnende streamzeit in 100-Nanosecond-Einheiten empfängt.</span><span class="sxs-lookup"><span data-stu-id="f96cd-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f96cd-111">*ptimeend*</span><span class="sxs-lookup"><span data-stu-id="f96cd-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f96cd-112">Ein Zeiger auf eine Variable, die die endstreamzeit in 100-Nanosecond-Einheiten empfängt.</span><span class="sxs-lookup"><span data-stu-id="f96cd-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="f96cd-113">Wenn das Beispiel keine Endzeit hat, wird der Wert auf die Startzeit plus 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f96cd-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96cd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f96cd-114">Return value</span></span>

<span data-ttu-id="f96cd-115">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f96cd-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f96cd-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f96cd-116">Return code</span></span>                                                                                                   | <span data-ttu-id="f96cd-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f96cd-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="f96cd-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f96cd-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="f96cd-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f96cd-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f96cd-120"><dt>**VFW \_ S \_ keine \_ \_ Endzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="f96cd-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="f96cd-121">Sample hat eine gültige Startzeit, aber keine Endzeit.</span><span class="sxs-lookup"><span data-stu-id="f96cd-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="f96cd-122"><dt>**VFW \_ E- \_ Beispiel \_ Zeit \_ nicht \_ festgelegt**</dt></span><span class="sxs-lookup"><span data-stu-id="f96cd-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="f96cd-123">Das Beispiel enthält keine gültigen Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="f96cd-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="f96cd-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f96cd-124">Remarks</span></span>

<span data-ttu-id="f96cd-125">Die endmember-Variablen " [**cmediasample:: m \_ Start**](cmediasample-m-start.md) " und " [**cmediasample:: m \_**](cmediasample-m-end.md) " geben die Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="f96cd-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="f96cd-126">Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt an, ob die Zeitstempel gültig sind.</span><span class="sxs-lookup"><span data-stu-id="f96cd-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="f96cd-127">Weitere Informationen zu Zeitstempeln finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="f96cd-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f96cd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f96cd-128">Requirements</span></span>



| <span data-ttu-id="f96cd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f96cd-129">Requirement</span></span> | <span data-ttu-id="f96cd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f96cd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96cd-131">Header</span><span class="sxs-lookup"><span data-stu-id="f96cd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f96cd-132"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f96cd-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f96cd-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f96cd-133">Library</span></span><br/> | <dl> <span data-ttu-id="f96cd-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f96cd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96cd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f96cd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96cd-136">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f96cd-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





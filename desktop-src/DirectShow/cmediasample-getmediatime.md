---
description: 'Die getmediatime-Methode ruft die Medien Zeiten für dieses Beispiel ab. Diese Methode implementiert die imediasample:: getmediatime-Methode.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Cmediasample. getmediatime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364881"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="cefe1-104">Cmediasample. getmediatime-Methode</span><span class="sxs-lookup"><span data-stu-id="cefe1-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="cefe1-105">Die- `GetMediaTime` Methode ruft die Medien Zeiten für dieses Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="cefe1-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="cefe1-106">Diese Methode implementiert die [**imediasample:: getmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cefe1-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cefe1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cefe1-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="cefe1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cefe1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefe1-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="cefe1-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="cefe1-110">Ein Zeiger auf eine Variable, die die Start Zeit der Medien empfängt.</span><span class="sxs-lookup"><span data-stu-id="cefe1-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="cefe1-111">*ausgesetzt*</span><span class="sxs-lookup"><span data-stu-id="cefe1-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cefe1-112">Ein Zeiger auf eine Variable, die die Endzeit des Mediums empfängt.</span><span class="sxs-lookup"><span data-stu-id="cefe1-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefe1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cefe1-113">Return value</span></span>

<span data-ttu-id="cefe1-114">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cefe1-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="cefe1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cefe1-115">Return code</span></span>                                                                                                  | <span data-ttu-id="cefe1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cefe1-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="cefe1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cefe1-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="cefe1-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cefe1-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cefe1-119"><dt>**VFW \_ E \_ Medien \_ Zeit \_ nicht \_ festgelegt**</dt></span><span class="sxs-lookup"><span data-stu-id="cefe1-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="cefe1-120">Für dieses Beispiel wurden keine Medien Zeiten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cefe1-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cefe1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cefe1-121">Remarks</span></span>

<span data-ttu-id="cefe1-122">Die [**cmediasample:: m \_ mediaend**](cmediasample-m-mediaend.md) -Member-Variable gibt einen Offset von [**cmediasample:: m \_ mediastart**](cmediasample-m-mediastart.md)an, aber der vom *Pend* -Parameter empfangene Wert ist eine absolute Medien Zeit, berechnet als **m \_ mediastart**  +  **m \_ mediaend**.</span><span class="sxs-lookup"><span data-stu-id="cefe1-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="cefe1-123">Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="cefe1-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cefe1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cefe1-124">Requirements</span></span>



| <span data-ttu-id="cefe1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cefe1-125">Requirement</span></span> | <span data-ttu-id="cefe1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cefe1-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cefe1-127">Header</span><span class="sxs-lookup"><span data-stu-id="cefe1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cefe1-128"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cefe1-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cefe1-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cefe1-129">Library</span></span><br/> | <dl> <span data-ttu-id="cefe1-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cefe1-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cefe1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cefe1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cefe1-132">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cefe1-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





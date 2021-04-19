---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Cbasonputpin. Notify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358679"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="9091c-104">Cbasinput PIN. Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="9091c-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="9091c-105">Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="9091c-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="9091c-106">Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9091c-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9091c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9091c-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="9091c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9091c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9091c-109">*pself*</span><span class="sxs-lookup"><span data-stu-id="9091c-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="9091c-110">Zeiger auf den Filter, der die Qualitäts Steuerungs Meldung sendet.</span><span class="sxs-lookup"><span data-stu-id="9091c-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="9091c-111">*Q1*</span><span class="sxs-lookup"><span data-stu-id="9091c-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="9091c-112">[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="9091c-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9091c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9091c-113">Return value</span></span>

<span data-ttu-id="9091c-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9091c-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9091c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9091c-115">Remarks</span></span>

<span data-ttu-id="9091c-116">Filter übergeben in der Regel Qualitäts Steuerungs Meldungen an eine upstreamausgabepin und nicht an eine Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="9091c-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="9091c-117">Daher gibt diese Methode S OK zurück, \_ ohne etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="9091c-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="9091c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9091c-118">Requirements</span></span>



| <span data-ttu-id="9091c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9091c-119">Requirement</span></span> | <span data-ttu-id="9091c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9091c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9091c-121">Header</span><span class="sxs-lookup"><span data-stu-id="9091c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9091c-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9091c-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9091c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9091c-123">Library</span></span><br/> | <dl> <span data-ttu-id="9091c-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9091c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9091c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9091c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9091c-126">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9091c-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="9091c-127">Qualitäts Steuerungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9091c-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 





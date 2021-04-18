---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Cbasepin. Notify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357693"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="94c55-104">Cbasepin. Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="94c55-104">CBasePin.Notify method</span></span>

<span data-ttu-id="94c55-105">Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="94c55-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="94c55-106">Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.</span><span class="sxs-lookup"><span data-stu-id="94c55-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c55-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="94c55-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="94c55-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94c55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94c55-109">*pself*</span><span class="sxs-lookup"><span data-stu-id="94c55-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="94c55-110">Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters, der die Qualitäts Steuerungs Meldung übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="94c55-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="94c55-111">*Q1*</span><span class="sxs-lookup"><span data-stu-id="94c55-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="94c55-112">Gibt eine [**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur an, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="94c55-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94c55-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94c55-113">Return value</span></span>

<span data-ttu-id="94c55-114">Die Basisklasse gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="94c55-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="94c55-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94c55-115">Remarks</span></span>

<span data-ttu-id="94c55-116">Ausgabe Pins sollten diese Methode überschreiben, um Qualitäts Steuerungs Meldungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="94c55-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="94c55-117">Wenn ein externer Quality Manager installiert wurde (siehe [**cbasepin:: setsink**](cbasepin-setsink.md)), übergeben Sie die Nachricht an diesen Quality Manager.</span><span class="sxs-lookup"><span data-stu-id="94c55-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="94c55-118">Andernfalls sollte der Filter die Nachricht selbst verarbeiten oder die Nachrichten-upstreamnachricht übergeben.</span><span class="sxs-lookup"><span data-stu-id="94c55-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="94c55-119">Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="94c55-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94c55-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94c55-120">Requirements</span></span>



| <span data-ttu-id="94c55-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94c55-121">Requirement</span></span> | <span data-ttu-id="94c55-122">Wert</span><span class="sxs-lookup"><span data-stu-id="94c55-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c55-123">Header</span><span class="sxs-lookup"><span data-stu-id="94c55-123">Header</span></span><br/>  | <dl> <span data-ttu-id="94c55-124"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94c55-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94c55-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94c55-125">Library</span></span><br/> | <dl> <span data-ttu-id="94c55-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="94c55-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c55-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94c55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c55-128">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="94c55-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





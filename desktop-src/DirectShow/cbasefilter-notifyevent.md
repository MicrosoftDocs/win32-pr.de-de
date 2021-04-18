---
description: Die notifyEvent-Methode sendet eine Ereignis Benachrichtigung an den Filter Graph-Manager.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Cbasefilter. notisyevent-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361449"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="4f9cc-103">Cbasefilter. notityevent-Methode</span><span class="sxs-lookup"><span data-stu-id="4f9cc-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="4f9cc-104">Die- `NotifyEvent` Methode sendet eine Ereignis Benachrichtigung an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9cc-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="4f9cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f9cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f9cc-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="4f9cc-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9cc-108">Ereignis Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4f9cc-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="4f9cc-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9cc-110">Der erste Parameter des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="4f9cc-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="4f9cc-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9cc-112">Der zweite Parameter des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f9cc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f9cc-113">Return value</span></span>

<span data-ttu-id="4f9cc-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4f9cc-115">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4f9cc-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4f9cc-116">Return code</span></span>                                                                               | <span data-ttu-id="4f9cc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f9cc-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f9cc-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9cc-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="4f9cc-119">Der Filter Graph-Manager akzeptiert keine Ereignis Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="4f9cc-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9cc-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4f9cc-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4f9cc-122"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4f9cc-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="4f9cc-123">Der Filter weist keinen Zeiger auf die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f9cc-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f9cc-124">Remarks</span></span>

<span data-ttu-id="4f9cc-125">Eine Liste von Benachrichtigungs Codes und Parameterwerten finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4f9cc-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="4f9cc-126">Wenn in der-Basisklasse der Ereignis Code EC \_ Complete lautet, legt die-Methode den *EventParam2* -Parameter auf einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters fest.</span><span class="sxs-lookup"><span data-stu-id="4f9cc-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9cc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9cc-127">Requirements</span></span>



| <span data-ttu-id="4f9cc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f9cc-128">Requirement</span></span> | <span data-ttu-id="4f9cc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9cc-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9cc-130">Header</span><span class="sxs-lookup"><span data-stu-id="4f9cc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4f9cc-131"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f9cc-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f9cc-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f9cc-132">Library</span></span><br/> | <dl> <span data-ttu-id="4f9cc-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4f9cc-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f9cc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9cc-135">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4f9cc-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





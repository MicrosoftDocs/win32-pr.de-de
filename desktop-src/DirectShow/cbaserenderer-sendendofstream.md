---
description: Wenn das Ende des Streams erreicht wurde, plant die Methode "sendendof Stream" ein EC \_ Complete-Ereignis für den Filter Graph-Manager.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Cbaserderderer. sendendof Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372310"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="84517-103">Cbaserderderer. sendendof Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="84517-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="84517-104">Wenn das Ende des Streams erreicht wurde, plant die- `SendEndOfStream` Methode ein EC \_ Complete-Ereignis für den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="84517-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="84517-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84517-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="84517-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84517-106">Parameters</span></span>

<span data-ttu-id="84517-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="84517-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84517-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84517-108">Return value</span></span>

<span data-ttu-id="84517-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="84517-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="84517-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="84517-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="84517-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84517-111">Return code</span></span>                                                                             | <span data-ttu-id="84517-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84517-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84517-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="84517-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="84517-114">Der Filter Graph-Manager akzeptiert keine Ereignis Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="84517-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="84517-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84517-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="84517-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="84517-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="84517-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84517-117">Remarks</span></span>

<span data-ttu-id="84517-118">Der Filter erhält möglicherweise vor der Endzeit des aktuellen Beispiels eine Benachrichtigung über das Ende des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="84517-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="84517-119">Wenn dies der Fall ist, sollte der Filter warten, bevor er eine [**EC \_ Complete**](ec-complete.md) -Benachrichtigung an den Filter Graph-Manager veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="84517-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="84517-120">Deshalb gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="84517-120">Therefore:</span></span>

-   <span data-ttu-id="84517-121">Wenn der Filter eine frühe End-of-Stream-Benachrichtigung (EOS) empfangen hat, plant diese Methode ein Timer-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="84517-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="84517-122">Wenn das Timer-Ereignis aktiviert ist, stellt der Filter das EC Complete-Ereignis zur Verfügung \_ .</span><span class="sxs-lookup"><span data-stu-id="84517-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="84517-123">Wenn der Filter eine nicht frühe EOS-Benachrichtigung erhalten hat, sendet diese Methode sofort das EC \_ Complete-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="84517-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="84517-124">Wenn der Filter keine ausstehende EOS-Benachrichtigung hat, gibt die Methode zurück, ohne etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="84517-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="84517-125">Die Timer-Rückruf Methode ist [**cbasererderderer:: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="84517-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="84517-126">Um das EC Complete-Ereignis zu übermitteln \_ , ruft der Filter die [**cbaserdenderer:: notifyendofstream**](cbaserenderer-notifyendofstream.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="84517-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84517-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84517-127">Requirements</span></span>



| <span data-ttu-id="84517-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84517-128">Requirement</span></span> | <span data-ttu-id="84517-129">Wert</span><span class="sxs-lookup"><span data-stu-id="84517-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84517-130">Header</span><span class="sxs-lookup"><span data-stu-id="84517-130">Header</span></span><br/>  | <dl> <span data-ttu-id="84517-131"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84517-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84517-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84517-132">Library</span></span><br/> | <dl> <span data-ttu-id="84517-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="84517-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84517-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84517-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84517-135">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="84517-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





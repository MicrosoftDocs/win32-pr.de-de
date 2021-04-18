---
description: Mit der changemediatype-Methode wird der Medientyp für die Verbindung dynamisch geändert.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Cdynamicoutputpin. changemediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352156"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="106ef-103">Cdynamicoutputpin. changemediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="106ef-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="106ef-104">Die- `ChangeMediaType` Methode ändert den Medientyp für die Verbindung dynamisch.</span><span class="sxs-lookup"><span data-stu-id="106ef-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="106ef-105">Die Änderung kann auftreten, während das Filter Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="106ef-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="106ef-106">Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="106ef-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="106ef-107">Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="106ef-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="106ef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="106ef-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="106ef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="106ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="106ef-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="106ef-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="106ef-111">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="106ef-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="106ef-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="106ef-112">Return value</span></span>

<span data-ttu-id="106ef-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="106ef-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="106ef-114">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="106ef-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="106ef-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="106ef-115">Return code</span></span>                                                                                           | <span data-ttu-id="106ef-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="106ef-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="106ef-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="106ef-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="106ef-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="106ef-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="106ef-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="106ef-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="106ef-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="106ef-120">Failure.</span></span> <span data-ttu-id="106ef-121">Möglicherweise hat der besitzende Filter [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md)nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="106ef-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="106ef-122"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="106ef-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="106ef-123">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="106ef-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="106ef-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="106ef-124">Remarks</span></span>

<span data-ttu-id="106ef-125">Rufen Sie die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode auf, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="106ef-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="106ef-126">Diese Methode prüft zunächst, ob die downstreameingabepin das neue Format akzeptieren kann, ohne dass eine erneute Verbindung hergestellt</span><span class="sxs-lookup"><span data-stu-id="106ef-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="106ef-127">Er fragt die Eingabe-PIN für die [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="106ef-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="106ef-128">Wenn die eingabepin **ipinconnection** unterstützt, ruft die Methode die [**ipinconnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) -Methode mit dem vorgeschlagenen Medientyp auf.</span><span class="sxs-lookup"><span data-stu-id="106ef-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="106ef-129">Wenn die Eingabe-PIN den neuen Medientyp annimmt, ruft die Methode die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode auf und verhandelt die zuordneranforderungen erneut.</span><span class="sxs-lookup"><span data-stu-id="106ef-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="106ef-130">Wenn dagegen der Downstream-Pin **ipinconnection** nicht unterstützt, oder wenn der neue Medientyp abgelehnt wird, ruft die-Methode die [**cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md) -Methode auf, um eine dynamische erneute Verbindung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="106ef-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="106ef-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="106ef-131">Requirements</span></span>



| <span data-ttu-id="106ef-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="106ef-132">Requirement</span></span> | <span data-ttu-id="106ef-133">Wert</span><span class="sxs-lookup"><span data-stu-id="106ef-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106ef-134">Header</span><span class="sxs-lookup"><span data-stu-id="106ef-134">Header</span></span><br/>  | <dl> <span data-ttu-id="106ef-135"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="106ef-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="106ef-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="106ef-136">Library</span></span><br/> | <dl> <span data-ttu-id="106ef-137">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="106ef-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="106ef-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="106ef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106ef-139">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="106ef-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





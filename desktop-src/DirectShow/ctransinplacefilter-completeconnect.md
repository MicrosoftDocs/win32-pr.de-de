---
description: Die completeconnect-Methode schließt eine PIN-Verbindung ab.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Ctransinplacefilter. completeconnect-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372734"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="bdbf9-103">Ctransinplacefilter. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="bdbf9-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="bdbf9-104">Die- `CompleteConnect` Methode schließt eine PIN-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbf9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdbf9-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="bdbf9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdbf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbf9-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="bdbf9-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbf9-108">Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="bdbf9-109">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="bdbf9-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbf9-110">Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbf9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdbf9-111">Return value</span></span>

<span data-ttu-id="bdbf9-112">Gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="bdbf9-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bdbf9-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bdbf9-114">Return code</span></span>                                                                                           | <span data-ttu-id="bdbf9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdbf9-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="bdbf9-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbf9-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bdbf9-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="bdbf9-118"><dt>**VFW \_ E \_ nicht \_ im \_ Diagramm**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbf9-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="bdbf9-119">Der Filter befindet sich nicht in einem Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdbf9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdbf9-120">Remarks</span></span>

<span data-ttu-id="bdbf9-121">Diese Methode überschreibt die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="bdbf9-122">Das Verhalten des Filters hängt von der Reihenfolge der PIN-Verbindungen ab:</span><span class="sxs-lookup"><span data-stu-id="bdbf9-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="bdbf9-123">Wenn die Eingabe-PIN zuerst verbunden ist, verwendet die Verbindung eine temporäre Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="bdbf9-124">Wenn die Ausgabe-PIN verbunden ist, verbindet der Filter die eingabepin erneut.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="bdbf9-125">Das erneute Verbinden der Eingabe-PIN bewirkt, dass der upstreamfilter die Zuweisung erneut ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="bdbf9-126">An diesem Punkt schlägt die Eingabe-PIN eine Zuweisung vom downstreamfilter vor.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="bdbf9-127">Weitere Informationen finden Sie unter [**ctransinplaceinputpin:: getallocator**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="bdbf9-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="bdbf9-128">Wenn die Ausgabe-PIN zuerst verbunden ist, wählt die Ausgabepin keinen Zuweiser aus.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="bdbf9-129">Wenn die eingabepin verbunden ist, aushandelte Sie eine Zuweisung für beide Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="bdbf9-130">Wenn die Eingabe-und Ausgabemedien Typen nicht identisch sind, verbindet der Filter die Ausgabe-PIN mit dem Eingabetyp erneut.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="bdbf9-131">Der Filter führt alle Pin-Neuverbindungen durch Aufrufen der [**cbasefilter:: reconnectpin**](cbasefilter-reconnectpin.md) -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="bdbf9-132">Die **reconnectpin** -Methode wiederum ruft die [**IFilterGraph2:: reconnectex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) -Methode für den Filter Graph-Manager auf.</span><span class="sxs-lookup"><span data-stu-id="bdbf9-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbf9-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdbf9-133">Requirements</span></span>



| <span data-ttu-id="bdbf9-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdbf9-134">Requirement</span></span> | <span data-ttu-id="bdbf9-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bdbf9-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbf9-136">Header</span><span class="sxs-lookup"><span data-stu-id="bdbf9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="bdbf9-137"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdbf9-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bdbf9-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdbf9-138">Library</span></span><br/> | <dl> <span data-ttu-id="bdbf9-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bdbf9-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbf9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdbf9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbf9-141">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bdbf9-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 





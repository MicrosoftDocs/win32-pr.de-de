---
description: 'Die cbaseinputpin-Methode startet einen Löschvorgang. Diese Methode implementiert die IPin:: beginflush-Methode.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Cbaseiniputpin. beginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357674"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="f8946-104">Cbaseiniputpin. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="f8946-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="f8946-105">Die- `CBaseInputPin` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="f8946-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="f8946-106">Diese Methode implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f8946-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8946-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8946-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="f8946-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8946-108">Parameters</span></span>

<span data-ttu-id="f8946-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8946-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8946-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8946-110">Return value</span></span>

<span data-ttu-id="f8946-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f8946-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8946-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8946-112">Remarks</span></span>

<span data-ttu-id="f8946-113">Diese Methode legt das [**\_ bgeleert-Flag "cbaseinputpin:: m**](cbaseinputpin-m-bflushing.md) " auf " **true**" fest. Dies bewirkt, dass die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode weitere Beispiele ablehnt.</span><span class="sxs-lookup"><span data-stu-id="f8946-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="f8946-114">Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="f8946-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="f8946-115">Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für nachgeschaltete Eingabe Pins.</span><span class="sxs-lookup"><span data-stu-id="f8946-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="f8946-116">Wenn die PIN noch keine Medien Beispiele nach unten übermittelt hat, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="f8946-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="f8946-117">Wenn die Ausgabe Pins von der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet werden, können Sie die [**cbaseoutputpin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f8946-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="f8946-118">Ruft die Methode der Basisklasse auf.</span><span class="sxs-lookup"><span data-stu-id="f8946-118">Call the base class method.</span></span>
3.  <span data-ttu-id="f8946-119">Mit dem Verwerfen von Daten in der Warteschlange beginnen.</span><span class="sxs-lookup"><span data-stu-id="f8946-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="f8946-120">Rückgabe von blockierten Aufrufen der **Receive** -Methode.</span><span class="sxs-lookup"><span data-stu-id="f8946-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8946-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8946-121">Requirements</span></span>



| <span data-ttu-id="f8946-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8946-122">Requirement</span></span> | <span data-ttu-id="f8946-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f8946-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8946-124">Header</span><span class="sxs-lookup"><span data-stu-id="f8946-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f8946-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8946-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8946-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8946-126">Library</span></span><br/> | <dl> <span data-ttu-id="f8946-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8946-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8946-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8946-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8946-129">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8946-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 





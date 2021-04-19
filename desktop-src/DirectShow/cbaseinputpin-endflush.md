---
description: 'Die endflush-Methode beendet einen Löschvorgang. Implementiert die IPin:: endflush-Methode.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Cbaseiniputpin. endflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366943"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="1feaf-104">Cbaseiniputpin. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="1feaf-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="1feaf-105">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="1feaf-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="1feaf-106">Implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1feaf-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1feaf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1feaf-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1feaf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1feaf-108">Parameters</span></span>

<span data-ttu-id="1feaf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1feaf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1feaf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1feaf-110">Return value</span></span>

<span data-ttu-id="1feaf-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="1feaf-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1feaf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1feaf-112">Remarks</span></span>

<span data-ttu-id="1feaf-113">Diese Methode legt das [**\_ bgeleert-Flag "cbaseinputpin:: m**](cbaseinputpin-m-bflushing.md) " auf " **true**" fest, wodurch die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode Beispiele annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="1feaf-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="1feaf-114">Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1feaf-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="1feaf-115">Geben Sie alle gepufferten Daten frei, und warten Sie, bis alle Samples in der Warteschlange verworfen wurden</span><span class="sxs-lookup"><span data-stu-id="1feaf-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="1feaf-116">Löschen Sie alle ausstehenden " [**EC \_ Complete**](ec-complete.md) "-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="1feaf-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="1feaf-117">Ruft die Methode der Basisklasse auf.</span><span class="sxs-lookup"><span data-stu-id="1feaf-117">Call the base class method.</span></span>
4.  <span data-ttu-id="1feaf-118">Nennen Sie [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für nachgeschaltete Eingabe Pins.</span><span class="sxs-lookup"><span data-stu-id="1feaf-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="1feaf-119">Wenn die PIN noch keine Medien Beispiele nach unten übermittelt hat, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="1feaf-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="1feaf-120">Wenn die Ausgabe Pins von der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet werden, können Sie die [**cbaseoutputpin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1feaf-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1feaf-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1feaf-121">Requirements</span></span>



| <span data-ttu-id="1feaf-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1feaf-122">Requirement</span></span> | <span data-ttu-id="1feaf-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1feaf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1feaf-124">Header</span><span class="sxs-lookup"><span data-stu-id="1feaf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1feaf-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1feaf-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1feaf-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1feaf-126">Library</span></span><br/> | <dl> <span data-ttu-id="1feaf-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1feaf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1feaf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1feaf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1feaf-129">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1feaf-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 





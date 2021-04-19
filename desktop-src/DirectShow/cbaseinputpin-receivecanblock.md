---
description: 'Die receivecanblock-Methode bestimmt, ob Aufrufe der IMemInputPin:: Receive-Methode blockiert werden könnten. Diese Methode implementiert die IMemInputPin:: receivecanblock-Methode.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Cbaseinputpin. receivecanblock-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369274"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="9ef9a-104">Cbaseinputpin. receivecanblock-Methode</span><span class="sxs-lookup"><span data-stu-id="9ef9a-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="9ef9a-105">Die- `ReceiveCanBlock` Methode bestimmt, ob Aufrufe der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode blockiert werden könnten.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="9ef9a-106">Diese Methode implementiert die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef9a-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="9ef9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef9a-108">Parameters</span></span>

<span data-ttu-id="9ef9a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ef9a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ef9a-110">Return value</span></span>

<span data-ttu-id="9ef9a-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9ef9a-112">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="9ef9a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ef9a-113">Return code</span></span>                                                                             | <span data-ttu-id="9ef9a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ef9a-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="9ef9a-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9ef9a-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9ef9a-116">Die PIN wird bei einem empfangenden **Empfang** nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="9ef9a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ef9a-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9ef9a-118">Die PIN kann bei einem **Empfangs Empfang** blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="9ef9a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ef9a-119">Remarks</span></span>

<span data-ttu-id="9ef9a-120">Gibt false zurück, \_ Wenn der Aufruf der **Receive** -Methode garantiert nicht blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="9ef9a-121">Andernfalls wird S \_ OK oder ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="9ef9a-122">Wenn die **Receive** -Methode **Receive** -Befehle für eine nachgeschaltete Pin aufruft, kann die downstreampin blockiert werden. `ReceiveCanBlock` muss diesen Faktor berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="9ef9a-123">Mit dieser Methode kann ein upstreamfilter die Threading Strategie bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="9ef9a-124">Wenn die **Receive** -Methode blockiert werden kann, kann der upstreamfilter entscheiden, einen Arbeits Thread zu verwenden, der Daten puffert.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="9ef9a-125">Eine Implementierung dieser Strategie finden Sie unter der [**coutputqueue**](coutputqueue.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="9ef9a-126">In der Basisklasse gibt diese Methode S OK zurück, \_ Wenn einer der folgenden Punkte zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9ef9a-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="9ef9a-127">Der Filter hat keine Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="9ef9a-128">Eine mit diesem Filter verbundene Eingabe-PIN signalisiert, dass Sie blockiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="9ef9a-129">Die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle wird von einer mit diesem Filter verbundenen Eingabe-PIN nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ef9a-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef9a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ef9a-130">Requirements</span></span>



| <span data-ttu-id="9ef9a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ef9a-131">Requirement</span></span> | <span data-ttu-id="9ef9a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9ef9a-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef9a-133">Header</span><span class="sxs-lookup"><span data-stu-id="9ef9a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9ef9a-134"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef9a-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ef9a-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ef9a-135">Library</span></span><br/> | <dl> <span data-ttu-id="9ef9a-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef9a-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef9a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ef9a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef9a-138">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9ef9a-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 





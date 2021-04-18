---
description: Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Ctransformfilter. Receive-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354709"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="169c5-103">Ctransformfilter. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="169c5-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="169c5-104">Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.</span><span class="sxs-lookup"><span data-stu-id="169c5-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="169c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="169c5-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="169c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="169c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="169c5-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="169c5-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="169c5-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle für das Eingabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="169c5-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="169c5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="169c5-109">Return value</span></span>

<span data-ttu-id="169c5-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="169c5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="169c5-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="169c5-111">Possible values include the following:</span></span>



| <span data-ttu-id="169c5-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="169c5-112">Return code</span></span>                                                                             | <span data-ttu-id="169c5-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="169c5-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="169c5-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="169c5-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="169c5-115">Der upstreamfilter sollte das Senden von Beispielen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="169c5-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="169c5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="169c5-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="169c5-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="169c5-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="169c5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="169c5-118">Remarks</span></span>

<span data-ttu-id="169c5-119">Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="169c5-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="169c5-120">Diese Methode ruft die [**ctransformfilter:: initializeoutputsample**](ctransformfilter-initializeoutputsample.md) -Methode auf, die ein neues Ausgabe Beispiel vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="169c5-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="169c5-121">Anschließend wird die [**ctransformfilter:: Transform**](ctransformfilter-transform.md) -Methode aufgerufen, die von der abgeleiteten Klasse implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="169c5-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="169c5-122">Die **Transformations** Methode verarbeitet die Eingabedaten und erzeugt Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="169c5-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="169c5-123">Wenn die **Transformations** Methode S false zurückgibt \_ , `Receive` Löscht die Methode dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="169c5-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="169c5-124">Im ersten gelöschten Beispiel sendet der Filter ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="169c5-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="169c5-125">Andernfalls liefert der  \_ Filter das Ausgabe Beispiel, wenn die Transform-Methode "S OK" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="169c5-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="169c5-126">Zu diesem Zweck wird die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die downstreameingabepin aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="169c5-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="169c5-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="169c5-127">Requirements</span></span>



| <span data-ttu-id="169c5-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="169c5-128">Requirement</span></span> | <span data-ttu-id="169c5-129">Wert</span><span class="sxs-lookup"><span data-stu-id="169c5-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="169c5-130">Header</span><span class="sxs-lookup"><span data-stu-id="169c5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="169c5-131"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="169c5-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="169c5-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="169c5-132">Library</span></span><br/> | <dl> <span data-ttu-id="169c5-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="169c5-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="169c5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="169c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="169c5-135">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="169c5-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





---
description: Die Receive-Methode wird aufgerufen, wenn das Objekt ein Medien Beispiel aus der Ausgabe-PIN empfängt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Cpullpin. Receive-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361624"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="a3f0c-104">Cpullpin. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="a3f0c-104">CPullPin.Receive method</span></span>

<span data-ttu-id="a3f0c-105">Die- `Receive` Methode wird aufgerufen, wenn das-Objekt ein Medien Beispiel aus der Ausgabe-PIN empfängt.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="a3f0c-106">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f0c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3f0c-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a3f0c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3f0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f0c-109">*psample*</span><span class="sxs-lookup"><span data-stu-id="a3f0c-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f0c-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Mediums Sample.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f0c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3f0c-111">Return value</span></span>

<span data-ttu-id="a3f0c-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a3f0c-113">Wenn Sie einen anderen Wert als S OK zurückgeben, \_ wird der datenzieh Thread beendet.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f0c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3f0c-114">Remarks</span></span>

<span data-ttu-id="a3f0c-115">Diese Methode wird immer dann aufgerufen, wenn ein neues Beispiel aus der Ausgabe-PIN eintrifft.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="a3f0c-116">Schreiben Sie diese Methode auf die gleiche Weise wie die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="a3f0c-117">Die Zeitstempel im Beispiel geben die Byte Offsets relativ zur ursprünglichen Startposition an, die in der [**cpullpin:: Seek**](cpullpin-seek.md) -Methode angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="a3f0c-118">Die Startposition wird auf die nächste Ausrichtungs Grenze gerundet, und die Position des Stopps wird auf die nächste Ausrichtungs Grenze aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="a3f0c-119">Außerdem wird die Dauer verwendet, wenn die anhalteposition die Gesamtdauer überschreitet.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="a3f0c-120">Alle Zeitstempel werden als Byte Offset multipliziert mit 10 Millionen angegeben, der als Konstante Einheiten definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="a3f0c-121">Folglich ist eine Sekunde eine Sekunde ein Byte.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="a3f0c-122">Um die tatsächlichen Byte Offsets zu ermitteln, müssen Sie [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) aufrufen und die Ergebnisse nach Einheiten aufteilen.</span><span class="sxs-lookup"><span data-stu-id="a3f0c-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f0c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3f0c-123">Requirements</span></span>



| <span data-ttu-id="a3f0c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3f0c-124">Requirement</span></span> | <span data-ttu-id="a3f0c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a3f0c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f0c-126">Header</span><span class="sxs-lookup"><span data-stu-id="a3f0c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f0c-127"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f0c-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a3f0c-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3f0c-128">Library</span></span><br/> | <dl> <span data-ttu-id="a3f0c-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f0c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f0c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3f0c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f0c-131">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a3f0c-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





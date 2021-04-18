---
description: Die dobufferprocessingloop-Methode generiert Mediendaten und übergibt sie an die downstreameingabepin.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Csourcestream. dobufferprocessingloop-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351378"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="a4f46-103">Csourcestream. dobufferprocessingloop-Methode</span><span class="sxs-lookup"><span data-stu-id="a4f46-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="a4f46-104">Die `DoBufferProcessingLoop` -Methode generiert Mediendaten und übergibt sie an die downstreameingabepin.</span><span class="sxs-lookup"><span data-stu-id="a4f46-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4f46-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="a4f46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4f46-106">Parameters</span></span>

<span data-ttu-id="a4f46-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4f46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4f46-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4f46-108">Return value</span></span>

<span data-ttu-id="a4f46-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a4f46-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a4f46-110">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4f46-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a4f46-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4f46-111">Return code</span></span>                                                                             | <span data-ttu-id="a4f46-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4f46-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4f46-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a4f46-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a4f46-114">Der Thread hat eine Anforderung zum Abbrechen empfangen.</span><span class="sxs-lookup"><span data-stu-id="a4f46-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="a4f46-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4f46-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a4f46-116">Der Stream wurde beendet, oder der Downstream-Filter akzeptiert keine Stichproben.</span><span class="sxs-lookup"><span data-stu-id="a4f46-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4f46-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4f46-117">Remarks</span></span>

<span data-ttu-id="a4f46-118">Diese Methode implementiert die Hauptschleife, die Daten verarbeitet und Sie nachgeschalteter Weise bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a4f46-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="a4f46-119">Jedes Mal, wenn die-Schleife durchlaufen wird, ruft die-Methode ein leeres Medien Beispiel aus der Zuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="a4f46-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="a4f46-120">Sie übergibt das Beispiel an die [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a4f46-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="a4f46-121">Die **FillBuffer** -Methode, die von der abgeleiteten Klasse implementiert werden muss, generiert Mediendaten und platziert Sie im Beispiel Puffer.</span><span class="sxs-lookup"><span data-stu-id="a4f46-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="a4f46-122">Die Schleife wird beendet, wenn eine der folgenden Aktionen auftritt:</span><span class="sxs-lookup"><span data-stu-id="a4f46-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="a4f46-123">Die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der Eingabe-PIN lehnt ein Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="a4f46-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="a4f46-124">Die **FillBuffer** -Methode gibt S \_ false zurück, um das Ende des Streams anzugeben, oder gibt einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="a4f46-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="a4f46-125">Der Thread empfängt eine [**csourcestream:: Beendigung**](csourcestream-stop.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a4f46-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="a4f46-126">Die- `DoBufferProcessingLoop` Methode verarbeitet das Ende der Stream-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a4f46-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="a4f46-127">Wenn ein Fehler auftritt, sendet er ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="a4f46-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f46-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4f46-128">Requirements</span></span>



| <span data-ttu-id="a4f46-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4f46-129">Requirement</span></span> | <span data-ttu-id="a4f46-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f46-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f46-131">Header</span><span class="sxs-lookup"><span data-stu-id="a4f46-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f46-132"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f46-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a4f46-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4f46-133">Library</span></span><br/> | <dl> <span data-ttu-id="a4f46-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f46-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f46-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4f46-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f46-136">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a4f46-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





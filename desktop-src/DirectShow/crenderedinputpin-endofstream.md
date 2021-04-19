---
description: 'Die EndOfStream-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis ein neuer Run-Befehl an den Filter ausgegeben wird. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Crenderedinputpin. EndOf Stream-Methode (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373821"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="5b3d6-104">Crenderedinputpin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="5b3d6-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="5b3d6-105">Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis ein neuer Run-Befehl an den Filter ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="5b3d6-106">Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b3d6-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="5b3d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b3d6-108">Parameters</span></span>

<span data-ttu-id="5b3d6-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b3d6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b3d6-110">Return value</span></span>

<span data-ttu-id="5b3d6-111">Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3d6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b3d6-112">Remarks</span></span>

<span data-ttu-id="5b3d6-113">Wenn der Filter ausgeführt wird, sendet diese Methode ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="5b3d6-114">Andernfalls wird von ein Flag festgelegt, sodass das EC \_ Complete-Ereignis gesendet wird, wenn der Filter das nächste Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="5b3d6-115">Durch das Leeren des Filters wird das Flag gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="5b3d6-116">Sie sollten diese Methode überschreiben, um die streamingabsperre der PIN zu halten:</span><span class="sxs-lookup"><span data-stu-id="5b3d6-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="5b3d6-117">Wenn die Filterprozesse außerdem asynchron Aufrufe **empfangen** , sollte die PIN warten, bis das "EC Complete"-Ereignis gesendet wird, \_ bis der Filter alle ausstehenden Stichproben verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="5b3d6-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3d6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b3d6-118">Requirements</span></span>



| <span data-ttu-id="5b3d6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b3d6-119">Requirement</span></span> | <span data-ttu-id="5b3d6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5b3d6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d6-121">Header</span><span class="sxs-lookup"><span data-stu-id="5b3d6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5b3d6-122"><dt>Amextra. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d6-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b3d6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b3d6-123">Library</span></span><br/> | <dl> <span data-ttu-id="5b3d6-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3d6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b3d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3d6-126">**Crenderedinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5b3d6-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 





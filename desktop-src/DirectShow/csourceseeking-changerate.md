---
description: Die changerate-Methode wird aufgerufen, wenn sich die Wiedergabe Rate ändert.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Csourceseeking. changerate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368331"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="bbd81-103">Csourceseeking. changerate-Methode</span><span class="sxs-lookup"><span data-stu-id="bbd81-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="bbd81-104">Die- `ChangeRate` Methode wird aufgerufen, wenn sich die Wiedergabe Rate ändert.</span><span class="sxs-lookup"><span data-stu-id="bbd81-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd81-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="bbd81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbd81-106">Parameters</span></span>

<span data-ttu-id="bbd81-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bbd81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbd81-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbd81-108">Return value</span></span>

<span data-ttu-id="bbd81-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd81-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd81-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbd81-110">Remarks</span></span>

<span data-ttu-id="bbd81-111">Die [**csourceseeking:: ctrate**](csourceseeking-setrate.md) -Methode ruft diese Methode auf, die von der abgeleiteten Klasse implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bbd81-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="bbd81-112">Die **Methode "** -Methode" aktualisiert die Element Variable " [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) ", überprüft jedoch nicht den neuen Wert.</span><span class="sxs-lookup"><span data-stu-id="bbd81-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="bbd81-113">Eine Rate von NULL sollte immer abgelehnt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd81-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="bbd81-114">Die Raten kleiner als 0 (null) deuten auf eine negative</span><span class="sxs-lookup"><span data-stu-id="bbd81-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="bbd81-115">Die meisten Filter unterstützen keine negativen Raten.</span><span class="sxs-lookup"><span data-stu-id="bbd81-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="bbd81-116">Das folgende Beispiel zeigt eine mögliche Implementierung:</span><span class="sxs-lookup"><span data-stu-id="bbd81-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="bbd81-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd81-117">Requirements</span></span>



| <span data-ttu-id="bbd81-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd81-118">Requirement</span></span> | <span data-ttu-id="bbd81-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd81-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd81-120">Header</span><span class="sxs-lookup"><span data-stu-id="bbd81-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bbd81-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd81-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbd81-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bbd81-122">Library</span></span><br/> | <dl> <span data-ttu-id="bbd81-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd81-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd81-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd81-125">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bbd81-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





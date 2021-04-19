---
description: 'Mit der GetState-Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die imediafilter:: GetState-Methode.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Cbasefilter. GetState-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370754"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="5b33e-104">Cbasefilter. GetState-Methode</span><span class="sxs-lookup"><span data-stu-id="5b33e-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="5b33e-105">Mit der `GetState` -Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="5b33e-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="5b33e-106">Diese Methode implementiert die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5b33e-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b33e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b33e-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="5b33e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b33e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b33e-109">*dwmillisecstimeout*</span><span class="sxs-lookup"><span data-stu-id="5b33e-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="5b33e-110">Timeout Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="5b33e-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="5b33e-111">*State*</span><span class="sxs-lookup"><span data-stu-id="5b33e-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="5b33e-112">Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.</span><span class="sxs-lookup"><span data-stu-id="5b33e-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b33e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b33e-113">Return value</span></span>

<span data-ttu-id="5b33e-114">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="5b33e-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b33e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b33e-115">Remarks</span></span>

<span data-ttu-id="5b33e-116">In der Basisklasse sind alle Zustandsübergänge synchron, und der Parameter " *dwmillisecstimeout* " wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5b33e-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="5b33e-117">Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte Sie diese Methode überschreiben, um während der Zustandsübergänge zu warten, wobei ein Timeout von *dwmillisecstimeout* -Millisekunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="5b33e-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="5b33e-118">Wenn der Filter keine Daten bereitstellt, während Sie angehalten werden, überschreiben Sie die- `GetState` Methode, um den Wert von VFW S nicht zu senden, \_ \_ \_ Wenn der Filter angehalten wird (siehe [Bereitstellung von Beispielen](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="5b33e-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="5b33e-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5b33e-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="5b33e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b33e-120">Requirements</span></span>



| <span data-ttu-id="5b33e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b33e-121">Requirement</span></span> | <span data-ttu-id="5b33e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5b33e-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b33e-123">Header</span><span class="sxs-lookup"><span data-stu-id="5b33e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5b33e-124"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b33e-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b33e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b33e-125">Library</span></span><br/> | <dl> <span data-ttu-id="5b33e-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5b33e-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b33e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b33e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b33e-128">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5b33e-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





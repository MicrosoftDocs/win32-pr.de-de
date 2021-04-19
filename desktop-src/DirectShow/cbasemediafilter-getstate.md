---
description: 'Die GetState-Methode ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die imediafilter:: GetState-Methode.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Cbasemediafilter. GetState-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352868"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="118c9-104">Cbasemediafilter. GetState-Methode</span><span class="sxs-lookup"><span data-stu-id="118c9-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="118c9-105">Die `GetState` -Methode ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="118c9-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="118c9-106">Diese Methode implementiert die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="118c9-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="118c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="118c9-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="118c9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="118c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118c9-109">*dwmillisecstimeout*</span><span class="sxs-lookup"><span data-stu-id="118c9-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="118c9-110">Timeout Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="118c9-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="118c9-111">*State*</span><span class="sxs-lookup"><span data-stu-id="118c9-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="118c9-112">Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="118c9-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118c9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="118c9-113">Return value</span></span>

<span data-ttu-id="118c9-114">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="118c9-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="118c9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="118c9-115">Remarks</span></span>

<span data-ttu-id="118c9-116">In der Basisklasse sind alle Zustandsübergänge synchron, und der Parameter " *dwmillisecstimeout* " wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="118c9-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="118c9-117">Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte Sie diese Methode überschreiben, um während der Zustandsübergänge zu warten, wobei ein Timeout von *dwmillisecstimeout* -Millisekunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="118c9-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="118c9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="118c9-118">Requirements</span></span>



| <span data-ttu-id="118c9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="118c9-119">Requirement</span></span> | <span data-ttu-id="118c9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="118c9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="118c9-121">Header</span><span class="sxs-lookup"><span data-stu-id="118c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="118c9-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="118c9-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="118c9-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="118c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="118c9-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="118c9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="118c9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="118c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118c9-126">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="118c9-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





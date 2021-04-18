---
description: Die notifyfilterstate-Methode benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Cbasestreamcontrol. notifyfilterstate-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358716"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="4558a-103">Cbasestreamcontrol. notifyfilterstate-Methode</span><span class="sxs-lookup"><span data-stu-id="4558a-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="4558a-104">Die `NotifyFilterState` -Methode benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4558a-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4558a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4558a-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="4558a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4558a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4558a-107">*neuer \_ Status*</span><span class="sxs-lookup"><span data-stu-id="4558a-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="4558a-108">Gibt den neuen Zustand als Member der [**Filter \_ Status**](/windows/win32/api/strmif/ne-strmif-filter_state) -Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="4558a-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="4558a-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="4558a-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4558a-110">Gibt die Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="4558a-110">Specifies the start time.</span></span> <span data-ttu-id="4558a-111">Wenn der neue Filter Zustand State \_ Running ist, übergeben Sie den Wert aus der [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4558a-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="4558a-112">Andernfalls verwenden Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="4558a-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4558a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4558a-113">Return value</span></span>

<span data-ttu-id="4558a-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4558a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4558a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4558a-115">Remarks</span></span>

<span data-ttu-id="4558a-116">Diese Methode bewirkt, dass die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode nicht mehr wartet.</span><span class="sxs-lookup"><span data-stu-id="4558a-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="4558a-117">Ruft diese Methode auf, sobald der besitzende Filter den Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="4558a-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="4558a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4558a-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="4558a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4558a-119">Requirements</span></span>



| <span data-ttu-id="4558a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4558a-120">Requirement</span></span> | <span data-ttu-id="4558a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4558a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4558a-122">Header</span><span class="sxs-lookup"><span data-stu-id="4558a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4558a-123"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4558a-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4558a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4558a-124">Library</span></span><br/> | <dl> <span data-ttu-id="4558a-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4558a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4558a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4558a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4558a-127">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4558a-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





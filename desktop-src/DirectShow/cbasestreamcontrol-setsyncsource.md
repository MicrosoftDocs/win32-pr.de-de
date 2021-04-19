---
description: Die setsyncsource-Methode benachrichtigt die Basisklasse der aktuellen verweisuhr.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Cbasestreamcontrol. setsyncsource-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355863"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="8b798-103">Cbasestreamcontrol. setsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="8b798-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="8b798-104">Die- `SetSyncSource` Methode benachrichtigt die Basisklasse der aktuellen verweisuhr.</span><span class="sxs-lookup"><span data-stu-id="8b798-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b798-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b798-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="8b798-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b798-107">*präfemuhr*</span><span class="sxs-lookup"><span data-stu-id="8b798-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="8b798-108">Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Referenzuhr.</span><span class="sxs-lookup"><span data-stu-id="8b798-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b798-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b798-109">Return value</span></span>

<span data-ttu-id="8b798-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b798-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b798-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b798-111">Remarks</span></span>

<span data-ttu-id="8b798-112">Aufrufen Sie diese Methode in der [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode des Filters.</span><span class="sxs-lookup"><span data-stu-id="8b798-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="8b798-113">Die **cbasestreamcontrol** -Klasse verwendet die **IReferenceClock** -Schnittstelle, um sicherzustellen, dass die Stichproben nicht zu schnell verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="8b798-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="8b798-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b798-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="8b798-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b798-115">Requirements</span></span>



| <span data-ttu-id="8b798-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b798-116">Requirement</span></span> | <span data-ttu-id="8b798-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8b798-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b798-118">Header</span><span class="sxs-lookup"><span data-stu-id="8b798-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8b798-119"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b798-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b798-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b798-120">Library</span></span><br/> | <dl> <span data-ttu-id="8b798-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8b798-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b798-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b798-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b798-123">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8b798-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





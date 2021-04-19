---
description: 'Die getsyncsource-Methode ruft die Referenzuhr ab, die vom-Objekt verwendet wird. Diese Methode implementiert die imediafilter:: getsyncsource-Methode.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Cbasemediafilter. getsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369970"
---
# <a name="cbasemediafiltergetsyncsource-method"></a><span data-ttu-id="e18a8-104">Cbasemediafilter. getsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="e18a8-104">CBaseMediaFilter.GetSyncSource method</span></span>

<span data-ttu-id="e18a8-105">Die- `GetSyncSource` Methode ruft die Referenzuhr ab, die vom-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e18a8-105">The `GetSyncSource` method retrieves the reference clock that the object is using.</span></span> <span data-ttu-id="e18a8-106">Diese Methode implementiert die [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e18a8-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e18a8-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="e18a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e18a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18a8-109">*pclock*</span><span class="sxs-lookup"><span data-stu-id="e18a8-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="e18a8-110">Adresse einer Variablen, die einen Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr empfängt.</span><span class="sxs-lookup"><span data-stu-id="e18a8-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e18a8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e18a8-111">Return value</span></span>

<span data-ttu-id="e18a8-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="e18a8-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="e18a8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e18a8-113">Remarks</span></span>

<span data-ttu-id="e18a8-114">Wenn das Objekt keine verweisuhr verwendet, wird *\* pclock* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e18a8-114">If the object is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="e18a8-115">Wenn **die-** Methode zurückgibt, hat pclock einen ausstehenden Verweis Zähler, wenn *\* pclock* nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="e18a8-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="e18a8-116">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="e18a8-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18a8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e18a8-117">Requirements</span></span>



| <span data-ttu-id="e18a8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e18a8-118">Requirement</span></span> | <span data-ttu-id="e18a8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e18a8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18a8-120">Header</span><span class="sxs-lookup"><span data-stu-id="e18a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e18a8-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e18a8-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e18a8-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e18a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="e18a8-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e18a8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18a8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e18a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18a8-125">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e18a8-125">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





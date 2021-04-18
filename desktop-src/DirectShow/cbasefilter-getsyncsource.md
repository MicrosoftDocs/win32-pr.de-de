---
description: 'Die getsyncsource-Methode ruft die Referenzuhr ab, die der Filter verwendet. Diese Methode implementiert die imediafilter:: getsyncsource-Methode.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Cbasefilter. getsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371484"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="a2422-104">Cbasefilter. getsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="a2422-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="a2422-105">Die- `GetSyncSource` Methode ruft die Referenzuhr ab, die vom Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2422-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="a2422-106">Diese Methode implementiert die [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a2422-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2422-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2422-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="a2422-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2422-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2422-109">*pclock*</span><span class="sxs-lookup"><span data-stu-id="a2422-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="a2422-110">Adresse einer Variablen, die einen Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr empfängt.</span><span class="sxs-lookup"><span data-stu-id="a2422-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2422-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2422-111">Return value</span></span>

<span data-ttu-id="a2422-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="a2422-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2422-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2422-113">Remarks</span></span>

<span data-ttu-id="a2422-114">Wenn der Filter keine verweisuhr verwendet, wird *\* pclock* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a2422-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="a2422-115">Wenn **die-** Methode zurückgibt, hat pclock einen ausstehenden Verweis Zähler, wenn *\* pclock* nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="a2422-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="a2422-116">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="a2422-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2422-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2422-117">Requirements</span></span>



| <span data-ttu-id="a2422-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2422-118">Requirement</span></span> | <span data-ttu-id="a2422-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a2422-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2422-120">Header</span><span class="sxs-lookup"><span data-stu-id="a2422-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a2422-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2422-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2422-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2422-122">Library</span></span><br/> | <dl> <span data-ttu-id="a2422-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a2422-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2422-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2422-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2422-125">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a2422-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





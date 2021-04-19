---
description: 'Die setsyncsource-Methode legt eine Referenzuhr für den Filter fest. Diese Methode implementiert die imediafilter:: setsyncsource-Methode.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Cbasefilter. setsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366849"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="c5144-104">Cbasefilter. setsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="c5144-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="c5144-105">Die **setsyncsource** -Methode legt eine Referenzuhr für den Filter fest.</span><span class="sxs-lookup"><span data-stu-id="c5144-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="c5144-106">Diese Methode implementiert die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c5144-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5144-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5144-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="c5144-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5144-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5144-109">*pclock*</span><span class="sxs-lookup"><span data-stu-id="c5144-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="c5144-110">Ein Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c5144-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5144-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5144-111">Return value</span></span>

<span data-ttu-id="c5144-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5144-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5144-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5144-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5144-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5144-114">Requirements</span></span>



| <span data-ttu-id="c5144-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5144-115">Requirement</span></span> | <span data-ttu-id="c5144-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c5144-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5144-117">Header</span><span class="sxs-lookup"><span data-stu-id="c5144-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c5144-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5144-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c5144-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5144-119">Library</span></span><br/> | <dl> <span data-ttu-id="c5144-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c5144-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5144-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5144-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5144-122">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5144-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





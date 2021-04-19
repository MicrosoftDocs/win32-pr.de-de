---
description: 'Die setsyncsource-Methode legt eine Referenzuhr für das-Objekt fest. Diese Methode implementiert die imediafilter:: setsyncsource-Methode.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Cbasemediafilter. setsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356342"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="dea92-104">Cbasemediafilter. setsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="dea92-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="dea92-105">Die- `SetSyncSource` Methode legt eine Referenzuhr für das-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="dea92-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="dea92-106">Diese Methode implementiert die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dea92-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea92-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dea92-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="dea92-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dea92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea92-109">*pclock*</span><span class="sxs-lookup"><span data-stu-id="dea92-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="dea92-110">Ein Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr oder **null**.</span><span class="sxs-lookup"><span data-stu-id="dea92-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea92-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dea92-111">Return value</span></span>

<span data-ttu-id="dea92-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dea92-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea92-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dea92-113">Requirements</span></span>



| <span data-ttu-id="dea92-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dea92-114">Requirement</span></span> | <span data-ttu-id="dea92-115">Wert</span><span class="sxs-lookup"><span data-stu-id="dea92-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea92-116">Header</span><span class="sxs-lookup"><span data-stu-id="dea92-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dea92-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dea92-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dea92-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dea92-118">Library</span></span><br/> | <dl> <span data-ttu-id="dea92-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dea92-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea92-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dea92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea92-121">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dea92-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





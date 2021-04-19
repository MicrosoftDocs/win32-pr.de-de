---
description: 'Die queryaccept-Methode bestimmt, ob die PIN einen angegebenen Medientyp akzeptiert. Diese Methode implementiert die IPin:: queryaccept-Methode.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Cbasepin. queryaccept-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360446"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="8535e-104">Cbasepin. queryaccept-Methode</span><span class="sxs-lookup"><span data-stu-id="8535e-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="8535e-105">Die- `QueryAccept` Methode bestimmt, ob die PIN einen angegebenen Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8535e-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="8535e-106">Diese Methode implementiert die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8535e-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8535e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8535e-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8535e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8535e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8535e-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="8535e-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8535e-110">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="8535e-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8535e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8535e-111">Return value</span></span>

<span data-ttu-id="8535e-112">Gibt S \_ OK zurück, wenn der Medientyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8535e-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="8535e-113">Andernfalls gibt S \_ false zurück.</span><span class="sxs-lookup"><span data-stu-id="8535e-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="8535e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8535e-114">Remarks</span></span>

<span data-ttu-id="8535e-115">In der Basisklasse delegiert diese Methode an die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8535e-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="8535e-116">Wenn **checkmediatype** fehlschlägt, `QueryAccept` gibt S \_ false zurück.</span><span class="sxs-lookup"><span data-stu-id="8535e-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="8535e-117">Diese Methode enthält nicht den kritischen Abschnitt der PIN ([**cbasepin:: m \_ Plock**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="8535e-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="8535e-118">Wenn die abgeleitete Klasse den Satz zulässiger Medientypen dynamisch ändert, sollten Sie diese Methode überschreiben, um den kritischen Abschnitt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8535e-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="8535e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8535e-119">Requirements</span></span>



| <span data-ttu-id="8535e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8535e-120">Requirement</span></span> | <span data-ttu-id="8535e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8535e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8535e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8535e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8535e-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8535e-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8535e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8535e-124">Library</span></span><br/> | <dl> <span data-ttu-id="8535e-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8535e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8535e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8535e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8535e-127">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8535e-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





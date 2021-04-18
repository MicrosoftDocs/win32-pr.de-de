---
description: 'Die Connect-Methode verbindet die PIN mit einer anderen Pin. Diese Methode implementiert die IPin:: Connect-Methode.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Cbasepin. Connect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364529"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="e469f-104">Cbasepin. Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="e469f-104">CBasePin.Connect method</span></span>

<span data-ttu-id="e469f-105">Die- `Connect` Methode verbindet die PIN mit einer anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="e469f-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="e469f-106">Diese Methode implementiert die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e469f-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e469f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e469f-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e469f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e469f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e469f-109">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="e469f-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="e469f-110">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="e469f-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e469f-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e469f-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e469f-112">Ein Zeiger auf eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp für die Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="e469f-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e469f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e469f-113">Return value</span></span>

<span data-ttu-id="e469f-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e469f-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e469f-115">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="e469f-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e469f-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e469f-116">Return code</span></span>                                                                                                  | <span data-ttu-id="e469f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e469f-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e469f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e469f-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e469f-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="e469f-120"><dt>**VFW \_ E \_ bereits \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="e469f-121">Die PIN ist bereits verbunden.</span><span class="sxs-lookup"><span data-stu-id="e469f-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="e469f-122"><dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="e469f-123">Es konnte kein akzeptabler Medientyp gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e469f-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="e469f-124"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="e469f-125">Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e469f-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="e469f-126"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="e469f-127">Der angegebene Medientyp ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e469f-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="e469f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e469f-128">Remarks</span></span>

<span data-ttu-id="e469f-129">Der *PMT* -Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e469f-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="e469f-130">Außerdem kann ein partieller Medientyp mit dem Wert GUID \_ NULL für den Haupttyp, den Untertyp oder das Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e469f-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="e469f-131">In der Basisklasse testet diese Methode, ob die PIN bereits verbunden ist und ob der Filter beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e469f-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="e469f-132">Der Rest des Verbindungsprozesses wird an die [**cbasepin:: agreemediatype**](cbasepin-agreemediatype.md) -Methode delegiert.</span><span class="sxs-lookup"><span data-stu-id="e469f-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e469f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e469f-133">Requirements</span></span>



| <span data-ttu-id="e469f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e469f-134">Requirement</span></span> | <span data-ttu-id="e469f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e469f-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e469f-136">Header</span><span class="sxs-lookup"><span data-stu-id="e469f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e469f-137"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e469f-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e469f-138">Library</span></span><br/> | <dl> <span data-ttu-id="e469f-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e469f-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e469f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e469f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e469f-141">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e469f-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





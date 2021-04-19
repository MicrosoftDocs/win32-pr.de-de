---
description: 'Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaseeking:: GetCurrentPosition-Methode.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Cpospassthru. GetCurrentPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373822"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="8074e-104">Cpospassthru. GetCurrentPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="8074e-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="8074e-105">Die- `GetCurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="8074e-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="8074e-106">Diese Methode implementiert die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8074e-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8074e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8074e-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="8074e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8074e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8074e-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="8074e-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="8074e-110">Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="8074e-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8074e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8074e-111">Return value</span></span>

<span data-ttu-id="8074e-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8074e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8074e-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8074e-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8074e-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8074e-114">Return code</span></span>                                                                               | <span data-ttu-id="8074e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8074e-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8074e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8074e-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8074e-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8074e-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="8074e-118"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="8074e-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="8074e-119">Die Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8074e-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="8074e-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8074e-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8074e-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="8074e-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8074e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8074e-122">Remarks</span></span>

<span data-ttu-id="8074e-123">Diese Methode ruft die [**cpospassthru:: getmediatime**](cpospassthru-getmediatime.md) -Methode auf, um die aktuelle Position abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8074e-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="8074e-124">Wenn **getmediatime** fehlschlägt, ruft die Methode **imediaseeking:: GetCurrentPosition** für die verbundene PIN auf.</span><span class="sxs-lookup"><span data-stu-id="8074e-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="8074e-125">Die **getmediatime** -Methode schlägt standardmäßig in der Basisklasse fehl.</span><span class="sxs-lookup"><span data-stu-id="8074e-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="8074e-126">Wenn der Filter die aktuelle Position zwischenspeichert, überschreiben Sie **getmediatime** , um den zwischengespeicherten Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8074e-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8074e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8074e-127">Requirements</span></span>



| <span data-ttu-id="8074e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8074e-128">Requirement</span></span> | <span data-ttu-id="8074e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8074e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8074e-130">Header</span><span class="sxs-lookup"><span data-stu-id="8074e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8074e-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8074e-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8074e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8074e-132">Library</span></span><br/> | <dl> <span data-ttu-id="8074e-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8074e-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8074e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8074e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8074e-135">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8074e-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





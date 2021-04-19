---
description: Die dynamikreconnect-Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus. Die erneute Verbindung kann auftreten, während das Filter Diagramm ausgeführt wird.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Cdynamicoutputpin. dynamikreconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355258"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="b889c-104">Cdynamicoutputpin. dynamikreconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="b889c-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="b889c-105">Die- `DynamicReconnect` Methode führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus.</span><span class="sxs-lookup"><span data-stu-id="b889c-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="b889c-106">Die erneute Verbindung kann auftreten, während das Filter Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b889c-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b889c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b889c-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b889c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b889c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b889c-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b889c-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b889c-110">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="b889c-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b889c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b889c-111">Return value</span></span>

<span data-ttu-id="b889c-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b889c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b889c-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b889c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b889c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b889c-114">Return code</span></span>                                                                            | <span data-ttu-id="b889c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b889c-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b889c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b889c-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b889c-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b889c-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="b889c-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b889c-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b889c-119">Fehler.</span><span class="sxs-lookup"><span data-stu-id="b889c-119">Failure.</span></span> <span data-ttu-id="b889c-120">Möglicherweise hat der besitzende Filter die [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) -Methode nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b889c-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b889c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b889c-121">Remarks</span></span>

<span data-ttu-id="b889c-122">Diese Methode muss vom gleichen Thread aufgerufen werden, der Daten an die PIN übergibt.</span><span class="sxs-lookup"><span data-stu-id="b889c-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="b889c-123">Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b889c-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="b889c-124">Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="b889c-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="b889c-125">Rufen Sie [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) auf, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b889c-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b889c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b889c-126">Requirements</span></span>



| <span data-ttu-id="b889c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b889c-127">Requirement</span></span> | <span data-ttu-id="b889c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b889c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b889c-129">Header</span><span class="sxs-lookup"><span data-stu-id="b889c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b889c-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b889c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b889c-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b889c-131">Library</span></span><br/> | <dl> <span data-ttu-id="b889c-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b889c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b889c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b889c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b889c-134">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b889c-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





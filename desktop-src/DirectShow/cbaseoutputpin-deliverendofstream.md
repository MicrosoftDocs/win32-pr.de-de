---
description: Die deliverendofstream-Methode übergibt eine streamingbenachrichtigung an die verbundene Eingabe-PIN.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Cbaseoutputpin. deliverendof-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373954"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="ac554-103">Cbaseoutputpin. deliverendosstream-Methode</span><span class="sxs-lookup"><span data-stu-id="ac554-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="ac554-104">Die- `DeliverEndOfStream` Methode übermittelt eine Streamende-Benachrichtigung an die verbundene Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="ac554-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac554-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac554-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="ac554-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac554-106">Parameters</span></span>

<span data-ttu-id="ac554-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ac554-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac554-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac554-108">Return value</span></span>

<span data-ttu-id="ac554-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac554-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ac554-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="ac554-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="ac554-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac554-111">Return code</span></span>                                                                                           | <span data-ttu-id="ac554-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac554-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac554-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac554-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="ac554-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ac554-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="ac554-115"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="ac554-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ac554-116">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="ac554-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac554-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac554-117">Remarks</span></span>

<span data-ttu-id="ac554-118">Diese Methode ruft die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="ac554-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac554-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac554-119">Requirements</span></span>



| <span data-ttu-id="ac554-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac554-120">Requirement</span></span> | <span data-ttu-id="ac554-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ac554-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac554-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac554-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ac554-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac554-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ac554-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac554-124">Library</span></span><br/> | <dl> <span data-ttu-id="ac554-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ac554-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac554-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac554-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac554-127">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ac554-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





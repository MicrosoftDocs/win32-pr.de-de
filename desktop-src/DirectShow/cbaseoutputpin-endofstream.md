---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Cbaseoutputpin. EndOf Stream-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354761"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="aa63a-104">Cbaseoutputpin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="aa63a-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="aa63a-105">Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="aa63a-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="aa63a-106">Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="aa63a-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa63a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa63a-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="aa63a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa63a-108">Parameters</span></span>

<span data-ttu-id="aa63a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa63a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa63a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa63a-110">Return value</span></span>

<span data-ttu-id="aa63a-111">Gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="aa63a-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa63a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa63a-112">Remarks</span></span>

<span data-ttu-id="aa63a-113">Diese Methode sollte nur für Eingabe Pins aufgerufen werden, sodass die **cbaseoutputpin** -Implementierung E \_ unerwartet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aa63a-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa63a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa63a-114">Requirements</span></span>



| <span data-ttu-id="aa63a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa63a-115">Requirement</span></span> | <span data-ttu-id="aa63a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="aa63a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa63a-117">Header</span><span class="sxs-lookup"><span data-stu-id="aa63a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="aa63a-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa63a-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa63a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa63a-119">Library</span></span><br/> | <dl> <span data-ttu-id="aa63a-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa63a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa63a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa63a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa63a-122">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa63a-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





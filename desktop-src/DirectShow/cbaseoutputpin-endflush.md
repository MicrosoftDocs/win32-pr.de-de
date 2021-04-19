---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Cbaseoutputpin. endflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367772"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="7c67d-104">Cbaseoutputpin. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="7c67d-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="7c67d-105">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="7c67d-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="7c67d-106">Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7c67d-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c67d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c67d-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="7c67d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c67d-108">Parameters</span></span>

<span data-ttu-id="7c67d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c67d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c67d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c67d-110">Return value</span></span>

<span data-ttu-id="7c67d-111">Gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="7c67d-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c67d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c67d-112">Remarks</span></span>

<span data-ttu-id="7c67d-113">Diese Methode sollte nur für Eingabe Pins aufgerufen werden, sodass die **cbaseoutputpin** -Implementierung E \_ unerwartet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7c67d-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c67d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c67d-114">Requirements</span></span>



| <span data-ttu-id="7c67d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c67d-115">Requirement</span></span> | <span data-ttu-id="7c67d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7c67d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c67d-117">Header</span><span class="sxs-lookup"><span data-stu-id="7c67d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c67d-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c67d-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c67d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c67d-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c67d-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7c67d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c67d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c67d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c67d-122">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7c67d-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





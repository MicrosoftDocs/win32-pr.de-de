---
description: Die inaktive Methode benachrichtigt die PIN, dass der Filter beendet wurde.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Cdynamicoutputpin. inaktive Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356303"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="5f807-103">Cdynamicoutputpin. inaktive Methode</span><span class="sxs-lookup"><span data-stu-id="5f807-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="5f807-104">Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f807-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f807-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f807-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="5f807-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f807-106">Parameters</span></span>

<span data-ttu-id="5f807-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5f807-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f807-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f807-108">Return value</span></span>

<span data-ttu-id="5f807-109">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="5f807-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f807-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f807-110">Remarks</span></span>

<span data-ttu-id="5f807-111">Diese Methode überschreibt die [**cbaseoutputpin:: inaktive**](cbaseoutputpin-inactive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5f807-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="5f807-112">Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f807-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f807-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f807-113">Requirements</span></span>



| <span data-ttu-id="5f807-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f807-114">Requirement</span></span> | <span data-ttu-id="5f807-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f807-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f807-116">Header</span><span class="sxs-lookup"><span data-stu-id="5f807-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5f807-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f807-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f807-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f807-118">Library</span></span><br/> | <dl> <span data-ttu-id="5f807-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5f807-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f807-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f807-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f807-121">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5f807-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





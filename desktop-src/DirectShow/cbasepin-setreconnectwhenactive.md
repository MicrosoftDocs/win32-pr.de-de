---
description: Die Methode "streconnect-Active" gibt an, ob die PIN dynamische erneute Verbindungen unterstützt.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Cbasepin. cbasept-Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358203"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="13c37-103">Cbasepin. abtreconnect. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="13c37-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="13c37-104">Die- `SetReconnectWhenActive` Methode gibt an, ob die PIN dynamische erneute Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="13c37-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13c37-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="13c37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c37-107">*bcanreconnect*</span><span class="sxs-lookup"><span data-stu-id="13c37-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="13c37-108">Boolescher Wert, der angibt, ob die PIN dynamisch erneut eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="13c37-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="13c37-109">**True** gibt an, dass die PIN dynamisch erneut eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="13c37-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c37-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13c37-110">Return value</span></span>

<span data-ttu-id="13c37-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="13c37-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c37-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13c37-112">Remarks</span></span>

<span data-ttu-id="13c37-113">Standardmäßig müssen Sie einen Filter vor dem erneuten Verbinden der Pins abbrechen.</span><span class="sxs-lookup"><span data-stu-id="13c37-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="13c37-114">Wenn die PIN die Verbindung wiederherstellen kann, während der Filter aktiv ist, wird diese Methode mit dem Wert " **true**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="13c37-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="13c37-115">Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="13c37-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13c37-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13c37-116">Requirements</span></span>



| <span data-ttu-id="13c37-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13c37-117">Requirement</span></span> | <span data-ttu-id="13c37-118">Wert</span><span class="sxs-lookup"><span data-stu-id="13c37-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c37-119">Header</span><span class="sxs-lookup"><span data-stu-id="13c37-119">Header</span></span><br/>  | <dl> <span data-ttu-id="13c37-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="13c37-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13c37-121">Library</span></span><br/> | <dl> <span data-ttu-id="13c37-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c37-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c37-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c37-124">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="13c37-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





---
description: Die Methode canreconnect-aktiv fragt ab, ob die PIN dynamische erneute Verbindungen unterstützt.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Cbasepin. canreconnect-Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367724"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="5324f-103">Cbasepin. canreconnect-Active-Methode</span><span class="sxs-lookup"><span data-stu-id="5324f-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="5324f-104">Die- `CanReconnectWhenActive` Methode fragt ab, ob die PIN dynamische erneute Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5324f-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="5324f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5324f-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="5324f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5324f-106">Parameters</span></span>

<span data-ttu-id="5324f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5324f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5324f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5324f-108">Return value</span></span>

<span data-ttu-id="5324f-109">Gibt einen booleschen Wert zurück, der angibt, ob die PIN dynamisch erneut eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5324f-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="5324f-110">**True** gibt an, dass die PIN dynamisch erneut eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5324f-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="5324f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5324f-111">Remarks</span></span>

<span data-ttu-id="5324f-112">Standardmäßig müssen Sie einen Filter vor dem erneuten Verbinden der Pins abbrechen.</span><span class="sxs-lookup"><span data-stu-id="5324f-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="5324f-113">Wenn eine PIN eine dynamische erneute Verbindung unterstützt, kann Sie die Verbindung wiederherstellen, während der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5324f-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="5324f-114">Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="5324f-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5324f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5324f-115">Requirements</span></span>



| <span data-ttu-id="5324f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5324f-116">Requirement</span></span> | <span data-ttu-id="5324f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5324f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5324f-118">Header</span><span class="sxs-lookup"><span data-stu-id="5324f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5324f-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5324f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5324f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5324f-120">Library</span></span><br/> | <dl> <span data-ttu-id="5324f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5324f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5324f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5324f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5324f-123">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5324f-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





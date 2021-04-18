---
description: Die disconnectinternal-Methode unterbricht die aktuelle PIN-Verbindung.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Cbasepin. disconnectinternal-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364772"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="863d8-103">Cbasepin. disconnectinternal-Methode</span><span class="sxs-lookup"><span data-stu-id="863d8-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="863d8-104">Die- `DisconnectInternal` Methode unterbricht die aktuelle PIN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="863d8-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="863d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="863d8-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="863d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="863d8-106">Parameters</span></span>

<span data-ttu-id="863d8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="863d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="863d8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="863d8-108">Return value</span></span>

<span data-ttu-id="863d8-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="863d8-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="863d8-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="863d8-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="863d8-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="863d8-111">Return code</span></span>                                                                                         | <span data-ttu-id="863d8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="863d8-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="863d8-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="863d8-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="863d8-114">Die PIN war nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="863d8-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="863d8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="863d8-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="863d8-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="863d8-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="863d8-117"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="863d8-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="863d8-118">Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.</span><span class="sxs-lookup"><span data-stu-id="863d8-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="863d8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="863d8-119">Remarks</span></span>

<span data-ttu-id="863d8-120">Die [**cbasepin::D isconnect**](cbasepin-disconnect.md) -Methode delegiert den Disconnect-Prozess an diese Methode.</span><span class="sxs-lookup"><span data-stu-id="863d8-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="863d8-121">Diese Methode ruft die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="863d8-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="863d8-122">Außerdem wird der Verweis Zähler für die andere Pin freigegeben, die von der in [**cbasepin:: m \_ verbundenen**](cbasepin-m-connected.md) Member-Variable gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="863d8-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="863d8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="863d8-123">Requirements</span></span>



| <span data-ttu-id="863d8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="863d8-124">Requirement</span></span> | <span data-ttu-id="863d8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="863d8-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="863d8-126">Header</span><span class="sxs-lookup"><span data-stu-id="863d8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="863d8-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="863d8-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="863d8-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="863d8-128">Library</span></span><br/> | <dl> <span data-ttu-id="863d8-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="863d8-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="863d8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="863d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863d8-131">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="863d8-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





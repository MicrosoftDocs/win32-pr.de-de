---
description: Die Disconnect-Methode unterbricht die aktuelle PIN-Verbindung. Diese Methode implementiert die IPin::D isconnect-Methode.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Cbasepin. Disconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354648"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="1e414-104">Cbasepin. Disconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="1e414-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="1e414-105">Die- `Disconnect` Methode unterbricht die aktuelle PIN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1e414-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="1e414-106">Diese Methode implementiert die [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e414-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e414-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e414-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="1e414-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e414-108">Parameters</span></span>

<span data-ttu-id="1e414-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e414-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e414-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e414-110">Return value</span></span>

<span data-ttu-id="1e414-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e414-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e414-112">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="1e414-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="1e414-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1e414-113">Return code</span></span>                                                                                         | <span data-ttu-id="1e414-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e414-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e414-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1e414-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="1e414-116">Die PIN war nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="1e414-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="1e414-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e414-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="1e414-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1e414-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="1e414-119"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="1e414-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="1e414-120">Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1e414-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e414-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e414-121">Remarks</span></span>

<span data-ttu-id="1e414-122">Die Basisklasse delegiert den größten Teil der Arbeit an die [**cbasepin::D isconnectinternal**](cbasepin-disconnectinternal.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e414-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e414-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e414-123">Requirements</span></span>



| <span data-ttu-id="1e414-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e414-124">Requirement</span></span> | <span data-ttu-id="1e414-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1e414-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e414-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e414-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1e414-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e414-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e414-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e414-128">Library</span></span><br/> | <dl> <span data-ttu-id="1e414-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1e414-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e414-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e414-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e414-131">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1e414-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





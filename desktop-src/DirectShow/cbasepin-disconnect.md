---
description: 'CBasePin.Disconnect-Methode: Die Disconnect-Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die IPin::D isconnect-Methode.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: CBasePin.Disconnect-Methode (Amfilter.h)
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
ms.openlocfilehash: bda01d02db2a93a90c63f206b723a55df2373418
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096008"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="91791-104">CBasePin.Disconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="91791-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="91791-105">Die `Disconnect` -Methode unterbricht die aktuelle Stecknadelverbindung.</span><span class="sxs-lookup"><span data-stu-id="91791-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="91791-106">Diese Methode implementiert die [**IPin::D isconnect-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="91791-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91791-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91791-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="91791-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91791-108">Parameters</span></span>

<span data-ttu-id="91791-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="91791-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91791-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91791-110">Return value</span></span>

<span data-ttu-id="91791-111">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="91791-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="91791-112">Mögliche Werte sind die werte in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="91791-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="91791-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="91791-113">Return code</span></span>                                                                                         | <span data-ttu-id="91791-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91791-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91791-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="91791-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="91791-116">Die Stecknadel war nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="91791-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="91791-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91791-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="91791-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="91791-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="91791-119"><dt>**VFW \_ E \_ NICHT \_ BEENDET**</dt></span><span class="sxs-lookup"><span data-stu-id="91791-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="91791-120">Der Filter ist aktiv, und der Pin unterstützt keine dynamische Wiederherstellung der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="91791-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91791-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91791-121">Remarks</span></span>

<span data-ttu-id="91791-122">Die Basisklasse delegiert den Großteil der Arbeit an die [**CBasePin::D isconnectInternal-Methode.**](cbasepin-disconnectinternal.md)</span><span class="sxs-lookup"><span data-stu-id="91791-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91791-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91791-123">Requirements</span></span>



| <span data-ttu-id="91791-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91791-124">Requirement</span></span> | <span data-ttu-id="91791-125">Wert</span><span class="sxs-lookup"><span data-stu-id="91791-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91791-126">Header</span><span class="sxs-lookup"><span data-stu-id="91791-126">Header</span></span><br/>  | <dl> <span data-ttu-id="91791-127"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="91791-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="91791-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91791-128">Library</span></span><br/> | <dl> <span data-ttu-id="91791-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="91791-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91791-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91791-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91791-131">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="91791-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





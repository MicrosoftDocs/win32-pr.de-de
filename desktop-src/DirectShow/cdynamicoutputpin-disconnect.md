---
description: Die Disconnect-Methode unterbricht die aktuelle PIN-Verbindung. Diese Methode implementiert die IPin::D isconnect-Methode.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Cdynamicoutputpin. Disconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372226"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="c95c5-104">Cdynamicoutputpin. Disconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="c95c5-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="c95c5-105">Die- `Disconnect` Methode unterbricht die aktuelle PIN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c95c5-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="c95c5-106">Diese Methode implementiert die [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c95c5-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c95c5-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="c95c5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c95c5-108">Parameters</span></span>

<span data-ttu-id="c95c5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c95c5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c95c5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c95c5-110">Return value</span></span>

<span data-ttu-id="c95c5-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c95c5-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c95c5-112">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c95c5-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c95c5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c95c5-113">Return code</span></span>                                                                             | <span data-ttu-id="c95c5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c95c5-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c95c5-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c95c5-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c95c5-116">Die PIN war nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="c95c5-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="c95c5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c95c5-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c95c5-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c95c5-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="c95c5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c95c5-119">Remarks</span></span>

<span data-ttu-id="c95c5-120">Diese Methode überschreibt die [**cbasepin::D isconnect**](cbasepin-disconnect.md) -Methode, um das Trennen der Verbindung zu ermöglichen, während der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c95c5-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95c5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c95c5-121">Requirements</span></span>



| <span data-ttu-id="c95c5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c95c5-122">Requirement</span></span> | <span data-ttu-id="c95c5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c95c5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95c5-124">Header</span><span class="sxs-lookup"><span data-stu-id="c95c5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c95c5-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c95c5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c95c5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c95c5-126">Library</span></span><br/> | <dl> <span data-ttu-id="c95c5-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c95c5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c95c5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c95c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95c5-129">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c95c5-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





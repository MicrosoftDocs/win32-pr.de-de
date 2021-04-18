---
description: Die deliverendflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Cbaseoutputpin. deliverendflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371729"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="48740-103">Cbaseoutputpin. deliverendflush-Methode</span><span class="sxs-lookup"><span data-stu-id="48740-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="48740-104">Die- `DeliverEndFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="48740-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="48740-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48740-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="48740-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48740-106">Parameters</span></span>

<span data-ttu-id="48740-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="48740-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48740-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48740-108">Return value</span></span>

<span data-ttu-id="48740-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48740-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="48740-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="48740-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="48740-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="48740-111">Return code</span></span>                                                                                           | <span data-ttu-id="48740-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48740-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="48740-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48740-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="48740-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="48740-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="48740-115"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="48740-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="48740-116">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="48740-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48740-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48740-117">Remarks</span></span>

<span data-ttu-id="48740-118">Diese Methode ruft die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="48740-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="48740-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48740-119">Requirements</span></span>



| <span data-ttu-id="48740-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48740-120">Requirement</span></span> | <span data-ttu-id="48740-121">Wert</span><span class="sxs-lookup"><span data-stu-id="48740-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48740-122">Header</span><span class="sxs-lookup"><span data-stu-id="48740-122">Header</span></span><br/>  | <dl> <span data-ttu-id="48740-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48740-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48740-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48740-124">Library</span></span><br/> | <dl> <span data-ttu-id="48740-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="48740-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48740-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48740-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48740-127">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="48740-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





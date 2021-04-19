---
description: Die deliverbeginflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu starten.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Cbaseoutputpin. deliverbeginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370308"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="0aec8-103">Cbaseoutputpin. deliverbeginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="0aec8-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="0aec8-104">Die- `DeliverBeginFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="0aec8-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aec8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0aec8-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="0aec8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aec8-106">Parameters</span></span>

<span data-ttu-id="0aec8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0aec8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0aec8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0aec8-108">Return value</span></span>

<span data-ttu-id="0aec8-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0aec8-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0aec8-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="0aec8-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0aec8-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0aec8-111">Return code</span></span>                                                                                           | <span data-ttu-id="0aec8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0aec8-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0aec8-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0aec8-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0aec8-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0aec8-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="0aec8-115"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="0aec8-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0aec8-116">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="0aec8-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0aec8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aec8-117">Remarks</span></span>

<span data-ttu-id="0aec8-118">Diese Methode ruft die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="0aec8-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aec8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aec8-119">Requirements</span></span>



| <span data-ttu-id="0aec8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aec8-120">Requirement</span></span> | <span data-ttu-id="0aec8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0aec8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aec8-122">Header</span><span class="sxs-lookup"><span data-stu-id="0aec8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0aec8-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aec8-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0aec8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0aec8-124">Library</span></span><br/> | <dl> <span data-ttu-id="0aec8-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0aec8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aec8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aec8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aec8-127">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0aec8-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





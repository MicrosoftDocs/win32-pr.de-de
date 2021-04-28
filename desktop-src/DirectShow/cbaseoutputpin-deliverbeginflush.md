---
description: 'CBaseOutputPin.DeliverBeginFlush-Methode: Die DeliverBeginFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: CBaseOutputPin.DeliverBeginFlush-Methode (Amfilter.h)
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
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099518"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="09a1b-103">CBaseOutputPin.DeliverBeginFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="09a1b-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="09a1b-104">Die `DeliverBeginFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="09a1b-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09a1b-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="09a1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09a1b-106">Parameters</span></span>

<span data-ttu-id="09a1b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="09a1b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09a1b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09a1b-108">Return value</span></span>

<span data-ttu-id="09a1b-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="09a1b-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09a1b-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="09a1b-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="09a1b-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="09a1b-111">Return code</span></span>                                                                                           | <span data-ttu-id="09a1b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09a1b-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="09a1b-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09a1b-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="09a1b-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="09a1b-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="09a1b-115"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="09a1b-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="09a1b-116">Pin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="09a1b-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09a1b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09a1b-117">Remarks</span></span>

<span data-ttu-id="09a1b-118">Diese Methode ruft die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Eingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="09a1b-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a1b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09a1b-119">Requirements</span></span>



| <span data-ttu-id="09a1b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09a1b-120">Requirement</span></span> | <span data-ttu-id="09a1b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="09a1b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a1b-122">Header</span><span class="sxs-lookup"><span data-stu-id="09a1b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="09a1b-123"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="09a1b-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09a1b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09a1b-124">Library</span></span><br/> | <dl> <span data-ttu-id="09a1b-125"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="09a1b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a1b-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09a1b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a1b-127">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="09a1b-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





---
description: 'CBaseOutputPin.DeliverEndFlush-Methode: Die DeliverEndFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.'
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: CBaseOutputPin.DeliverEndFlush-Methode (Amfilter.h)
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
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096178"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="126df-103">CBaseOutputPin.DeliverEndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="126df-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="126df-104">Die `DeliverEndFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="126df-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="126df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="126df-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="126df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="126df-106">Parameters</span></span>

<span data-ttu-id="126df-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="126df-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="126df-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="126df-108">Return value</span></span>

<span data-ttu-id="126df-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="126df-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="126df-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="126df-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="126df-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="126df-111">Return code</span></span>                                                                                           | <span data-ttu-id="126df-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="126df-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="126df-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="126df-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="126df-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="126df-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="126df-115"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="126df-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="126df-116">Die Stecknadel ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="126df-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="126df-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="126df-117">Remarks</span></span>

<span data-ttu-id="126df-118">Diese Methode ruft die [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für den Eingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="126df-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="126df-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="126df-119">Requirements</span></span>



| <span data-ttu-id="126df-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="126df-120">Requirement</span></span> | <span data-ttu-id="126df-121">Wert</span><span class="sxs-lookup"><span data-stu-id="126df-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="126df-122">Header</span><span class="sxs-lookup"><span data-stu-id="126df-122">Header</span></span><br/>  | <dl> <span data-ttu-id="126df-123"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="126df-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="126df-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="126df-124">Library</span></span><br/> | <dl> <span data-ttu-id="126df-125"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="126df-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="126df-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="126df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126df-127">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="126df-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





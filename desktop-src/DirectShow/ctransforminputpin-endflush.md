---
description: 'CTransformInputPin.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang. Diese Methode implementiert die IPin::EndFlush-Methode.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: CTransformInputPin.EndFlush-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095058"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="10f43-104">CTransformInputPin.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="10f43-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="10f43-105">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="10f43-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="10f43-106">Diese Methode implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="10f43-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f43-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10f43-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="10f43-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10f43-108">Parameters</span></span>

<span data-ttu-id="10f43-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="10f43-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10f43-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10f43-110">Return value</span></span>

<span data-ttu-id="10f43-111">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="10f43-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="10f43-112">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="10f43-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="10f43-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="10f43-113">Return code</span></span>                                                                                           | <span data-ttu-id="10f43-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10f43-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="10f43-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10f43-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="10f43-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="10f43-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="10f43-117"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="10f43-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="10f43-118">Der Ausgabepin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="10f43-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10f43-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10f43-119">Remarks</span></span>

<span data-ttu-id="10f43-120">Diese Methode ruft die [**CTransformFilter::EndFlush-Methode**](ctransformfilter-endflush.md) des Filters auf, um den Aufruf downstreamzu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="10f43-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="10f43-121">Anschließend wird die [**CBaseInputPin::EndFlush-Methode**](cbaseinputpin-endflush.md) des Pins aufrufen.</span><span class="sxs-lookup"><span data-stu-id="10f43-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f43-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f43-122">Requirements</span></span>



| <span data-ttu-id="10f43-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f43-123">Requirement</span></span> | <span data-ttu-id="10f43-124">Wert</span><span class="sxs-lookup"><span data-stu-id="10f43-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f43-125">Header</span><span class="sxs-lookup"><span data-stu-id="10f43-125">Header</span></span><br/>  | <dl> <span data-ttu-id="10f43-126"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="10f43-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="10f43-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10f43-127">Library</span></span><br/> | <dl> <span data-ttu-id="10f43-128"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="10f43-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





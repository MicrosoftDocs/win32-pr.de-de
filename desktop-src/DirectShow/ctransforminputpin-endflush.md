---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Ctransforminputpin. endflush-Methode (Transfrm. h)
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
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370737"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="0f1b7-104">Ctransforminputpin. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="0f1b7-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="0f1b7-105">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="0f1b7-106">Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1b7-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="0f1b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f1b7-108">Parameters</span></span>

<span data-ttu-id="0f1b7-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f1b7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f1b7-110">Return value</span></span>

<span data-ttu-id="0f1b7-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0f1b7-112">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0f1b7-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f1b7-113">Return code</span></span>                                                                                           | <span data-ttu-id="0f1b7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f1b7-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0f1b7-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f1b7-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0f1b7-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="0f1b7-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="0f1b7-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0f1b7-118">Die Ausgabepin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f1b7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f1b7-119">Remarks</span></span>

<span data-ttu-id="0f1b7-120">Diese Methode ruft die [**ctransformfilter:: endflush**](ctransformfilter-endflush.md) -Methode des Filters auf, um den Aufruf Downstream zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="0f1b7-121">Anschließend wird die [**cbaseiniputpin:: endflush**](cbaseinputpin-endflush.md) -Methode der PIN aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f1b7-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f1b7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f1b7-122">Requirements</span></span>



| <span data-ttu-id="0f1b7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f1b7-123">Requirement</span></span> | <span data-ttu-id="0f1b7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0f1b7-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1b7-125">Header</span><span class="sxs-lookup"><span data-stu-id="0f1b7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0f1b7-126"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f1b7-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f1b7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f1b7-127">Library</span></span><br/> | <dl> <span data-ttu-id="0f1b7-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f1b7-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





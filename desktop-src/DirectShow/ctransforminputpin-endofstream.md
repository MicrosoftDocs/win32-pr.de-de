---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Ctransforminputpin. EndOf Stream-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354206"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="eca6b-104">Ctransforminputpin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="eca6b-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="eca6b-105">Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="eca6b-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="eca6b-106">Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eca6b-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca6b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca6b-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="eca6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eca6b-108">Parameters</span></span>

<span data-ttu-id="eca6b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eca6b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eca6b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eca6b-110">Return value</span></span>

<span data-ttu-id="eca6b-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eca6b-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eca6b-112">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eca6b-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="eca6b-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eca6b-113">Return code</span></span>                                                                                           | <span data-ttu-id="eca6b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eca6b-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="eca6b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="eca6b-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eca6b-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="eca6b-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="eca6b-118">Die PIN wird zurzeit geleert.</span><span class="sxs-lookup"><span data-stu-id="eca6b-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="eca6b-119"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="eca6b-120">Die Ausgabe-PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="eca6b-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="eca6b-121"><dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="eca6b-122">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="eca6b-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="eca6b-123"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="eca6b-124">Die PIN wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="eca6b-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="eca6b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eca6b-125">Remarks</span></span>

<span data-ttu-id="eca6b-126">Diese Methode ruft die [**ctransformfilter:: EndOfStream**](ctransformfilter-endofstream.md) -Methode des Filters auf, um die Streamende Benachrichtigung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="eca6b-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="eca6b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eca6b-127">Requirements</span></span>



| <span data-ttu-id="eca6b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eca6b-128">Requirement</span></span> | <span data-ttu-id="eca6b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="eca6b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca6b-130">Header</span><span class="sxs-lookup"><span data-stu-id="eca6b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eca6b-131"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eca6b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eca6b-132">Library</span></span><br/> | <dl> <span data-ttu-id="eca6b-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eca6b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: 'CTransformInputPin.EndOfStream-Methode: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die IPin::EndOfStream-Methode.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: CTransformInputPin.EndOfStream-Methode (Transfrm.h)
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
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084978"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="2acb2-104">CTransformInputPin.EndOfStream-Methode</span><span class="sxs-lookup"><span data-stu-id="2acb2-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="2acb2-105">Die `EndOfStream` -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="2acb2-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="2acb2-106">Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)</span><span class="sxs-lookup"><span data-stu-id="2acb2-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2acb2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2acb2-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="2acb2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2acb2-108">Parameters</span></span>

<span data-ttu-id="2acb2-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2acb2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2acb2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2acb2-110">Return value</span></span>

<span data-ttu-id="2acb2-111">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="2acb2-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2acb2-112">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="2acb2-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2acb2-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2acb2-113">Return code</span></span>                                                                                           | <span data-ttu-id="2acb2-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2acb2-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="2acb2-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="2acb2-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2acb2-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="2acb2-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="2acb2-118">Die Stecknadel wird gerade geleert.</span><span class="sxs-lookup"><span data-stu-id="2acb2-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="2acb2-119"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2acb2-120">Der Ausgabepin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="2acb2-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="2acb2-121"><dt>**VFW \_ E \_ \_ RUNTIME-FEHLER**</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="2acb2-122">Es ist ein Laufzeitfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2acb2-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="2acb2-123"><dt>**VFW \_ E \_ WRONG \_ STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="2acb2-124">Die Stecknadel wird beendet.</span><span class="sxs-lookup"><span data-stu-id="2acb2-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="2acb2-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2acb2-125">Remarks</span></span>

<span data-ttu-id="2acb2-126">Diese Methode ruft die [**CTransformFilter::EndOfStream-Methode**](ctransformfilter-endofstream.md) des Filters auf, um die End-of-Stream-Benachrichtigung downstreamzu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="2acb2-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="2acb2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2acb2-127">Requirements</span></span>



| <span data-ttu-id="2acb2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2acb2-128">Requirement</span></span> | <span data-ttu-id="2acb2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2acb2-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acb2-130">Header</span><span class="sxs-lookup"><span data-stu-id="2acb2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2acb2-131"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2acb2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2acb2-132">Library</span></span><br/> | <dl> <span data-ttu-id="2acb2-133"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2acb2-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





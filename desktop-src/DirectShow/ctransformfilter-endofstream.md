---
description: Die EndOf Stream-Methode benachrichtigt den Filter, dass keine weiteren Daten von der Eingabe-PIN erwartet werden.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Ctransformfilter. EndOf Stream-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364660"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="5aca9-103">Ctransformfilter. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="5aca9-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="5aca9-104">Die- `EndOfStream` Methode benachrichtigt den Filter, dass keine zusätzlichen Daten von der eingabepin erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="5aca9-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aca9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aca9-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="5aca9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aca9-106">Parameters</span></span>

<span data-ttu-id="5aca9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5aca9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5aca9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aca9-108">Return value</span></span>

<span data-ttu-id="5aca9-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5aca9-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aca9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aca9-110">Remarks</span></span>

<span data-ttu-id="5aca9-111">Die [**ctransforminputpin:: endovstream**](ctransforminputpin-endofstream.md) -Methode der Eingabe-PIN ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5aca9-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="5aca9-112">Diese Methode übermittelt die downstreambenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="5aca9-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="5aca9-113">Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Medien Beispielen verwendet, sollte diese Methode überschrieben werden, und das Ende der Stream-Benachrichtigung wird in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="5aca9-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aca9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5aca9-114">Requirements</span></span>



| <span data-ttu-id="5aca9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aca9-115">Requirement</span></span> | <span data-ttu-id="5aca9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5aca9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aca9-117">Header</span><span class="sxs-lookup"><span data-stu-id="5aca9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5aca9-118"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aca9-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5aca9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5aca9-119">Library</span></span><br/> | <dl> <span data-ttu-id="5aca9-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5aca9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aca9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aca9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aca9-122">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5aca9-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





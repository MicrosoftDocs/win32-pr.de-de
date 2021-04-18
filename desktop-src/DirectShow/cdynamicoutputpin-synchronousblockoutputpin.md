---
description: Die synchronousblockoutputpin-Methode blockiert die PIN. gibt erst zurück, wenn die PIN blockiert ist.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Cdynamicoutputpin. synchronousblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371336"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="7b3aa-103">Cdynamicoutputpin. synchronousblockoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="7b3aa-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="7b3aa-104">Die- `SynchronousBlockOutputPin` Methode blockiert die PIN und gibt erst zurück, wenn die PIN blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b3aa-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="7b3aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b3aa-106">Parameters</span></span>

<span data-ttu-id="7b3aa-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b3aa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b3aa-108">Return value</span></span>

<span data-ttu-id="7b3aa-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7b3aa-110">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7b3aa-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7b3aa-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="7b3aa-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b3aa-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7b3aa-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3aa-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="7b3aa-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="7b3aa-115"><dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3aa-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="7b3aa-116">Die PIN ist bereits in einem anderen Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="7b3aa-117"><dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3aa-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="7b3aa-118">Die PIN ist bereits im aufrufenden Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b3aa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b3aa-119">Remarks</span></span>

<span data-ttu-id="7b3aa-120">Diese Methode nicht aus dem streamingthread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b3aa-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3aa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b3aa-121">Requirements</span></span>



| <span data-ttu-id="7b3aa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b3aa-122">Requirement</span></span> | <span data-ttu-id="7b3aa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7b3aa-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3aa-124">Header</span><span class="sxs-lookup"><span data-stu-id="7b3aa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3aa-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3aa-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7b3aa-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b3aa-126">Library</span></span><br/> | <dl> <span data-ttu-id="7b3aa-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3aa-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3aa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b3aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3aa-129">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7b3aa-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





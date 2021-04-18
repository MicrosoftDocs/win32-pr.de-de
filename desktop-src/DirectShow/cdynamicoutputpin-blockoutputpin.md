---
description: Die blockoutputpin-Methode blockiert die PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Cdynamicoutputpin. blockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371357"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="6eb79-103">Cdynamicoutputpin. blockoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="6eb79-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="6eb79-104">Die- `BlockOutputPin` Methode blockiert die PIN.</span><span class="sxs-lookup"><span data-stu-id="6eb79-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="6eb79-105">Während die PIN blockiert ist, wartet die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode auf die Blockierung der PIN.</span><span class="sxs-lookup"><span data-stu-id="6eb79-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="6eb79-106">Der blockierte Zustand verhindert, dass die Ausgabe-PIN Beispiele bereitstellt, das Ausgabeformat ändert oder eine erneute Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="6eb79-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb79-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6eb79-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="6eb79-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6eb79-108">Parameters</span></span>

<span data-ttu-id="6eb79-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6eb79-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6eb79-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6eb79-110">Return value</span></span>

<span data-ttu-id="6eb79-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6eb79-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eb79-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6eb79-112">Remarks</span></span>

<span data-ttu-id="6eb79-113">Halten Sie vor dem Aufrufen dieser Methode den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb79-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="6eb79-114">Diese Methode kann nicht aufgerufen werden, wenn ein streamingingthread die PIN verwendet, um Daten bereitzustellen oder um die Verbindung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6eb79-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="6eb79-115">Um zu überprüfen, ob ein streamingthread die PIN verwendet, können Sie die [**cdynamicoutputpin:: streamingthreadusingoutputpin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6eb79-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb79-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6eb79-116">Requirements</span></span>



| <span data-ttu-id="6eb79-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6eb79-117">Requirement</span></span> | <span data-ttu-id="6eb79-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6eb79-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb79-119">Header</span><span class="sxs-lookup"><span data-stu-id="6eb79-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb79-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb79-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6eb79-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6eb79-121">Library</span></span><br/> | <dl> <span data-ttu-id="6eb79-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb79-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb79-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6eb79-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb79-124">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6eb79-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





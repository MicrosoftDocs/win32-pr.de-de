---
description: 'CBaseOutputPin.EndOfStream-Methode: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die IPin::EndOfStream-Methode.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: CBaseOutputPin.EndOfStream-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096148"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="98b49-104">CBaseOutputPin.EndOfStream-Methode</span><span class="sxs-lookup"><span data-stu-id="98b49-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="98b49-105">Die `EndOfStream` -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="98b49-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="98b49-106">Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)</span><span class="sxs-lookup"><span data-stu-id="98b49-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="98b49-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="98b49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="98b49-108">Parameters</span></span>

<span data-ttu-id="98b49-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="98b49-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98b49-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98b49-110">Return value</span></span>

<span data-ttu-id="98b49-111">Gibt E \_ UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="98b49-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="98b49-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98b49-112">Remarks</span></span>

<span data-ttu-id="98b49-113">Diese Methode sollte nur für Eingabepins aufgerufen werden, sodass die **CBaseOutputPin-Implementierung** E \_ UNEXPECTED zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="98b49-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b49-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98b49-114">Requirements</span></span>



| <span data-ttu-id="98b49-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98b49-115">Requirement</span></span> | <span data-ttu-id="98b49-116">Wert</span><span class="sxs-lookup"><span data-stu-id="98b49-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b49-117">Header</span><span class="sxs-lookup"><span data-stu-id="98b49-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98b49-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="98b49-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98b49-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98b49-119">Library</span></span><br/> | <dl> <span data-ttu-id="98b49-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="98b49-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b49-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98b49-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b49-122">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="98b49-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





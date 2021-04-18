---
description: Die converttomilliseconds-Funktion konvertiert eine Verweis Zeit in Millisekunden.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Convertthmilliseconds-Funktion (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364929"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="ed398-103">Converttmilliseconds-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed398-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="ed398-104">Die- `ConvertToMilliseconds` Funktion konvertiert eine Verweis Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ed398-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed398-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed398-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="ed398-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed398-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed398-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="ed398-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ed398-108">Verweis Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ed398-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed398-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed398-109">Return value</span></span>

<span data-ttu-id="ed398-110">Gibt die in Millisekunden konvertierte Verweis Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="ed398-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed398-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed398-111">Requirements</span></span>



| <span data-ttu-id="ed398-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed398-112">Requirement</span></span> | <span data-ttu-id="ed398-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ed398-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed398-114">Header</span><span class="sxs-lookup"><span data-stu-id="ed398-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ed398-115"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed398-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ed398-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed398-116">Library</span></span><br/> | <dl> <span data-ttu-id="ed398-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ed398-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed398-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed398-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed398-119">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ed398-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 





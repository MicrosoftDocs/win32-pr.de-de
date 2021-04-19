---
description: Die Duration-Methode ruft die Dauer des Streams ab.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Cpullpin. Duration-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367740"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="33ed1-103">Cpullpin. Duration-Methode</span><span class="sxs-lookup"><span data-stu-id="33ed1-103">CPullPin.Duration method</span></span>

<span data-ttu-id="33ed1-104">Die- `Duration` Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="33ed1-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ed1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ed1-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="33ed1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ed1-107">*ptduration*</span><span class="sxs-lookup"><span data-stu-id="33ed1-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="33ed1-108">Ein Zeiger auf eine Variable, die die Dauer (in Bytes multipliziert mit 10 Millionen) empfängt.</span><span class="sxs-lookup"><span data-stu-id="33ed1-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ed1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33ed1-109">Return value</span></span>

<span data-ttu-id="33ed1-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="33ed1-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="33ed1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33ed1-111">Remarks</span></span>

<span data-ttu-id="33ed1-112">Die Dauer ist unbestimmt, bis die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="33ed1-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ed1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33ed1-113">Requirements</span></span>



| <span data-ttu-id="33ed1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33ed1-114">Requirement</span></span> | <span data-ttu-id="33ed1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="33ed1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ed1-116">Header</span><span class="sxs-lookup"><span data-stu-id="33ed1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="33ed1-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ed1-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="33ed1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33ed1-118">Library</span></span><br/> | <dl> <span data-ttu-id="33ed1-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33ed1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ed1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33ed1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ed1-121">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33ed1-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





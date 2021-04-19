---
description: Dieser Operator dividiert eine Verweis Zeit durch einen-Wert.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: Coaref time. Operator/Method (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370220"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="abb56-103">Coaref time. Operator/Method</span><span class="sxs-lookup"><span data-stu-id="abb56-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="abb56-104">Dieser Operator dividiert eine Verweis Zeit durch einen-Wert.</span><span class="sxs-lookup"><span data-stu-id="abb56-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb56-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="abb56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb56-107">*l*</span><span class="sxs-lookup"><span data-stu-id="abb56-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="abb56-108">Divisor.</span><span class="sxs-lookup"><span data-stu-id="abb56-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb56-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abb56-109">Return value</span></span>

<span data-ttu-id="abb56-110">Gibt ein neues **coareftime** -Objekt zurück, das dem Quotienten dieses-Objekts und **l** entspricht.</span><span class="sxs-lookup"><span data-stu-id="abb56-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb56-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abb56-111">Requirements</span></span>



| <span data-ttu-id="abb56-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abb56-112">Requirement</span></span> | <span data-ttu-id="abb56-113">Wert</span><span class="sxs-lookup"><span data-stu-id="abb56-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb56-114">Header</span><span class="sxs-lookup"><span data-stu-id="abb56-114">Header</span></span><br/>  | <dl> <span data-ttu-id="abb56-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abb56-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="abb56-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abb56-116">Library</span></span><br/> | <dl> <span data-ttu-id="abb56-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="abb56-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb56-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abb56-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb56-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="abb56-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





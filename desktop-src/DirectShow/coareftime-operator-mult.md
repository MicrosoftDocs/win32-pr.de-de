---
description: Dieser Operator multipliziert eine Verweis Zeit mit einem Wert.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Coaref time. Operator *-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365684"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="733cf-103">Coaref time. Operator- \* Methode</span><span class="sxs-lookup"><span data-stu-id="733cf-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="733cf-104">Dieser Operator multipliziert eine Verweis Zeit mit einem Wert.</span><span class="sxs-lookup"><span data-stu-id="733cf-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="733cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="733cf-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="733cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="733cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733cf-107">*l*</span><span class="sxs-lookup"><span data-stu-id="733cf-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="733cf-108">Multiplikator.</span><span class="sxs-lookup"><span data-stu-id="733cf-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733cf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="733cf-109">Return value</span></span>

<span data-ttu-id="733cf-110">Gibt ein neues **coareftime** -Objekt zurück, das dem Produkt dieses Objekts und **l** entspricht.</span><span class="sxs-lookup"><span data-stu-id="733cf-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="733cf-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="733cf-111">Requirements</span></span>



| <span data-ttu-id="733cf-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="733cf-112">Requirement</span></span> | <span data-ttu-id="733cf-113">Wert</span><span class="sxs-lookup"><span data-stu-id="733cf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733cf-114">Header</span><span class="sxs-lookup"><span data-stu-id="733cf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="733cf-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="733cf-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="733cf-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="733cf-116">Library</span></span><br/> | <dl> <span data-ttu-id="733cf-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="733cf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733cf-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="733cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733cf-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="733cf-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





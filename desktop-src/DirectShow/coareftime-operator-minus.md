---
description: Dieser Operator subtrahiert eine Verweis Zeit von einer anderen.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Coaref time. Operator-Method (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364935"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="3a7cf-103">Coaref time. Operator-Methode</span><span class="sxs-lookup"><span data-stu-id="3a7cf-103">COARefTime.operator- method</span></span>

<span data-ttu-id="3a7cf-104">Dieser Operator subtrahiert eine Verweis Zeit von einer anderen.</span><span class="sxs-lookup"><span data-stu-id="3a7cf-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a7cf-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="3a7cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a7cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a7cf-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="3a7cf-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7cf-108">Verweis auf das **coareftime** -Objekt, das subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a7cf-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a7cf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a7cf-109">Return value</span></span>

<span data-ttu-id="3a7cf-110">Gibt ein neues **coareftime** -Objekt zurück, das der Differenz der Verweis Zeiten entspricht.</span><span class="sxs-lookup"><span data-stu-id="3a7cf-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7cf-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a7cf-111">Requirements</span></span>



| <span data-ttu-id="3a7cf-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a7cf-112">Requirement</span></span> | <span data-ttu-id="3a7cf-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3a7cf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7cf-114">Header</span><span class="sxs-lookup"><span data-stu-id="3a7cf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3a7cf-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a7cf-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a7cf-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a7cf-116">Library</span></span><br/> | <dl> <span data-ttu-id="3a7cf-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3a7cf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a7cf-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a7cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a7cf-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3a7cf-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





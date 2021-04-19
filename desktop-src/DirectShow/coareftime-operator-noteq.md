---
description: Dieser Operator testet auf Ungleichheit zwischen zwei Verweis Zeiten.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Coaref time. Operator! =-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367698"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="6c2fc-103">Coaref time. Operator! =-Methode</span><span class="sxs-lookup"><span data-stu-id="6c2fc-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="6c2fc-104">Dieser Operator testet auf Ungleichheit zwischen zwei Verweis Zeiten.</span><span class="sxs-lookup"><span data-stu-id="6c2fc-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c2fc-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="6c2fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c2fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2fc-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="6c2fc-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6c2fc-108">Verweis auf das **coareftime** -Objekt, das verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c2fc-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2fc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c2fc-109">Return value</span></span>

<span data-ttu-id="6c2fc-110">Gibt **true** zurück, wenn die beiden-Objekte nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="6c2fc-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="6c2fc-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c2fc-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2fc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c2fc-112">Requirements</span></span>



| <span data-ttu-id="6c2fc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c2fc-113">Requirement</span></span> | <span data-ttu-id="6c2fc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c2fc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2fc-115">Header</span><span class="sxs-lookup"><span data-stu-id="6c2fc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6c2fc-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2fc-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c2fc-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c2fc-117">Library</span></span><br/> | <dl> <span data-ttu-id="6c2fc-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2fc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2fc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c2fc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2fc-120">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6c2fc-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





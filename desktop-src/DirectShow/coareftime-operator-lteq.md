---
description: Dieser Operator testet, ob eine Verweis Zeit größer oder gleich einer anderen ist.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: Coaref time. Operator<=-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4d7c8f212f175760473e5cfe2fdcbd85c4f89f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362013"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="7e454-103">Coaref time. Operator<=-Methode</span><span class="sxs-lookup"><span data-stu-id="7e454-103">COARefTime.operator<= method</span></span>

<span data-ttu-id="7e454-104">Dieser Operator testet, ob eine Verweis Zeit größer oder gleich einer anderen ist.</span><span class="sxs-lookup"><span data-stu-id="7e454-104">This operator tests if one reference time is greater than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e454-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e454-105">Syntax</span></span>


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7e454-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e454-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="7e454-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7e454-108">Verweis auf das **coareftime** -Objekt, das verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e454-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e454-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e454-109">Return value</span></span>

<span data-ttu-id="7e454-110">Gibt **true** zurück, wenn dieses Objekt größer oder gleich *RT* ist.</span><span class="sxs-lookup"><span data-stu-id="7e454-110">Returns **TRUE** if this object is greater than or equal to *rt*.</span></span> <span data-ttu-id="7e454-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e454-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e454-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e454-112">Requirements</span></span>



| <span data-ttu-id="7e454-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e454-113">Requirement</span></span> | <span data-ttu-id="7e454-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7e454-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e454-115">Header</span><span class="sxs-lookup"><span data-stu-id="7e454-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7e454-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e454-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7e454-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e454-117">Library</span></span><br/> | <dl> <span data-ttu-id="7e454-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7e454-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e454-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e454-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e454-120">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7e454-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





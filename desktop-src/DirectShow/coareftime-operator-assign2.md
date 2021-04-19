---
description: Der-Operator weist eine neue Verweis Zeit zu und verwendet den ' rt [REF] '-Parameter.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Coaref time. Operator = Method (ctlutil. h)-RT [REF]-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106364017"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="e95da-103">Coaref time. Operator = Method (ctlutil. h)-RT [REF]-Parameter</span><span class="sxs-lookup"><span data-stu-id="e95da-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="e95da-104">Dieser Operator weist eine neue Bezugszeit zu.</span><span class="sxs-lookup"><span data-stu-id="e95da-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e95da-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="e95da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e95da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95da-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="e95da-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e95da-108">Verweis auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der die neue Verweis Zeit in 100-Nanosecond-Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="e95da-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95da-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e95da-109">Return value</span></span>

<span data-ttu-id="e95da-110">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e95da-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e95da-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e95da-111">Requirements</span></span>

| <span data-ttu-id="e95da-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e95da-112">Requirement</span></span>                    | <span data-ttu-id="e95da-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e95da-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95da-114">Header</span><span class="sxs-lookup"><span data-stu-id="e95da-114">Header</span></span>  | <span data-ttu-id="e95da-115">Ctlutil. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="e95da-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="e95da-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e95da-116">Library</span></span> | <span data-ttu-id="e95da-117">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="e95da-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e95da-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e95da-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95da-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e95da-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





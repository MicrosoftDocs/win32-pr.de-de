---
description: Dieser Operator subtrahiert eine Verweis Zeit von einer anderen und legt dieses-Objekt auf das Ergebnis fest.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: Coaref time. Operator-=-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358651"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="da3de-103">Coaref time. Operator-=-Methode</span><span class="sxs-lookup"><span data-stu-id="da3de-103">COARefTime.operator-= method</span></span>

<span data-ttu-id="da3de-104">Dieser Operator subtrahiert eine Verweis Zeit von einer anderen und legt dieses-Objekt auf das Ergebnis fest.</span><span class="sxs-lookup"><span data-stu-id="da3de-104">This operator subtracts one reference time from another, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="da3de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da3de-105">Syntax</span></span>


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="da3de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da3de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3de-107">*RT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="da3de-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="da3de-108">Verweis auf das **coareftime** -Objekt, das subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="da3de-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3de-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da3de-109">Return value</span></span>

<span data-ttu-id="da3de-110">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="da3de-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="da3de-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da3de-111">Requirements</span></span>



| <span data-ttu-id="da3de-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da3de-112">Requirement</span></span> | <span data-ttu-id="da3de-113">Wert</span><span class="sxs-lookup"><span data-stu-id="da3de-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3de-114">Header</span><span class="sxs-lookup"><span data-stu-id="da3de-114">Header</span></span><br/>  | <dl> <span data-ttu-id="da3de-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da3de-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da3de-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da3de-116">Library</span></span><br/> | <dl> <span data-ttu-id="da3de-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="da3de-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da3de-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da3de-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3de-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="da3de-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





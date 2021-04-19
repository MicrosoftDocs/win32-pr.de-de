---
description: Dieser Operator weist eine neue Bezugszeit zu.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Coaref time. Operator =-Methode (ctlutil. h)
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
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370219"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="4d8f7-103">Coaref time. Operator =-Methode (ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="4d8f7-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="4d8f7-104">Dieser Operator weist eine neue Bezugszeit zu.</span><span class="sxs-lookup"><span data-stu-id="4d8f7-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d8f7-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="4d8f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8f7-107">*RD* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="4d8f7-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8f7-108">Verweis auf einen **Double** -Wert, der die neue Verweis Zeit in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="4d8f7-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8f7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d8f7-109">Return value</span></span>

<span data-ttu-id="4d8f7-110">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8f7-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8f7-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d8f7-111">Requirements</span></span>



| <span data-ttu-id="4d8f7-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d8f7-112">Requirement</span></span> | <span data-ttu-id="4d8f7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8f7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8f7-114">Header</span><span class="sxs-lookup"><span data-stu-id="4d8f7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4d8f7-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d8f7-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d8f7-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d8f7-116">Library</span></span><br/> | <dl> <span data-ttu-id="4d8f7-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4d8f7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8f7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8f7-119">**Coaref Time-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4d8f7-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





---
description: Die setsamplesize-Methode gibt eine festgelegte Stichprobengröße an oder gibt an, dass die Beispiele eine Variable Größe aufweisen.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Cmediatype. setsamplesize-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365457"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="857d2-103">Cmediatype. setsamplesize-Methode</span><span class="sxs-lookup"><span data-stu-id="857d2-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="857d2-104">Die- `SetSampleSize` Methode gibt eine festgelegte Stichprobengröße an oder gibt an, dass Beispiele eine Variable Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="857d2-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="857d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="857d2-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="857d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="857d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="857d2-107">*RT*</span><span class="sxs-lookup"><span data-stu-id="857d2-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="857d2-108">Stichprobengröße in Byte oder NULL.</span><span class="sxs-lookup"><span data-stu-id="857d2-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="857d2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="857d2-109">Return value</span></span>

<span data-ttu-id="857d2-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="857d2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="857d2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="857d2-111">Remarks</span></span>

<span data-ttu-id="857d2-112">Wenn der Wert von " *SZ* " 0 (null) ist, verwendet der Medientyp Variablen Stichprobengrößen.</span><span class="sxs-lookup"><span data-stu-id="857d2-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="857d2-113">Andernfalls wird die Stichprobengröße bei den *SZ* -Bytes korrigiert.</span><span class="sxs-lookup"><span data-stu-id="857d2-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="857d2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="857d2-114">Requirements</span></span>



| <span data-ttu-id="857d2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="857d2-115">Requirement</span></span> | <span data-ttu-id="857d2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="857d2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="857d2-117">Header</span><span class="sxs-lookup"><span data-stu-id="857d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="857d2-118"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="857d2-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="857d2-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="857d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="857d2-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="857d2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857d2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="857d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857d2-122">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="857d2-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





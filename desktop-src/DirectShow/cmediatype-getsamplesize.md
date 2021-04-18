---
description: Die getSampleSize-Methode ruft die Stichprobengröße ab.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Cmediatype. getSampleSize-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361269"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="0f7a5-103">Cmediatype. getSampleSize-Methode</span><span class="sxs-lookup"><span data-stu-id="0f7a5-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="0f7a5-104">Die- `GetSampleSize` Methode ruft die Stichprobengröße ab.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7a5-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="0f7a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f7a5-106">Parameters</span></span>

<span data-ttu-id="0f7a5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f7a5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f7a5-108">Return value</span></span>

<span data-ttu-id="0f7a5-109">Wenn die Stichprobengröße korrigiert ist, wird die Stichprobengröße in Byte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="0f7a5-110">Andernfalls wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f7a5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f7a5-111">Requirements</span></span>



| <span data-ttu-id="0f7a5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f7a5-112">Requirement</span></span> | <span data-ttu-id="0f7a5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0f7a5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7a5-114">Header</span><span class="sxs-lookup"><span data-stu-id="0f7a5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0f7a5-115"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7a5-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0f7a5-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f7a5-116">Library</span></span><br/> | <dl> <span data-ttu-id="0f7a5-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7a5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7a5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f7a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7a5-119">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f7a5-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





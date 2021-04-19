---
description: 'Die startstreaming-Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt. Diese Methode überschreibt die ctransformfilter:: startstreaming-Methode.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Cvideotransformfilter. startstreaming-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366910"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="7f702-104">Cvideotransformfilter. startstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="7f702-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="7f702-105">Die- `StartStreaming` Methode wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="7f702-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="7f702-106">Diese Methode überschreibt die [**ctransformfilter:: startstreaming**](ctransformfilter-startstreaming.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7f702-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f702-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f702-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="7f702-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f702-108">Parameters</span></span>

<span data-ttu-id="7f702-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7f702-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f702-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f702-110">Return value</span></span>

<span data-ttu-id="7f702-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7f702-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f702-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f702-112">Remarks</span></span>

<span data-ttu-id="7f702-113">Diese Methode setzt alle Leistungsstatistiken zurück.</span><span class="sxs-lookup"><span data-stu-id="7f702-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f702-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f702-114">Requirements</span></span>



| <span data-ttu-id="7f702-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f702-115">Requirement</span></span> | <span data-ttu-id="7f702-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7f702-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f702-117">Header</span><span class="sxs-lookup"><span data-stu-id="7f702-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7f702-118"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f702-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7f702-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f702-119">Library</span></span><br/> | <dl> <span data-ttu-id="7f702-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f702-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f702-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f702-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f702-122">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f702-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 





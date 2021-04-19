---
description: 'Die getrate-Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaseeking:: getrate-Methode.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Cpospassthru. getrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366911"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="48780-104">Cpospassthru. getrate-Methode</span><span class="sxs-lookup"><span data-stu-id="48780-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="48780-105">Die- `GetRate` Methode ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="48780-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="48780-106">Diese Methode implementiert die [**imediaseeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="48780-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48780-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48780-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="48780-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48780-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48780-109">*pdrate*</span><span class="sxs-lookup"><span data-stu-id="48780-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="48780-110">Ein Zeiger auf eine Variable, die die Wiedergabe Rate empfängt.</span><span class="sxs-lookup"><span data-stu-id="48780-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48780-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48780-111">Return value</span></span>

<span data-ttu-id="48780-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="48780-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="48780-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48780-113">Requirements</span></span>



| <span data-ttu-id="48780-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48780-114">Requirement</span></span> | <span data-ttu-id="48780-115">Wert</span><span class="sxs-lookup"><span data-stu-id="48780-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48780-116">Header</span><span class="sxs-lookup"><span data-stu-id="48780-116">Header</span></span><br/>  | <dl> <span data-ttu-id="48780-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48780-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48780-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48780-118">Library</span></span><br/> | <dl> <span data-ttu-id="48780-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="48780-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48780-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48780-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48780-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="48780-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





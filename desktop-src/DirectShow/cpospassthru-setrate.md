---
description: 'Die setRate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaseeking:: Server trate-Methode.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Cpospassthru. ctrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357692"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="60b44-104">Cpospassthru. ctrate-Methode</span><span class="sxs-lookup"><span data-stu-id="60b44-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="60b44-105">Die- `SetRate` Methode legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="60b44-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="60b44-106">Diese Methode implementiert die [**imediaseeking:: Server trate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="60b44-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b44-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="60b44-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60b44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b44-109">*drate*</span><span class="sxs-lookup"><span data-stu-id="60b44-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="60b44-110">Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="60b44-110">Playback rate.</span></span> <span data-ttu-id="60b44-111">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="60b44-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b44-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60b44-112">Return value</span></span>

<span data-ttu-id="60b44-113">Gibt E \_ invalidArg zurück, wenn *drate* 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="60b44-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="60b44-114">Andernfalls wird der **HRESULT** -Wert aus der verbundenen Pin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60b44-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b44-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b44-115">Requirements</span></span>



| <span data-ttu-id="60b44-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b44-116">Requirement</span></span> | <span data-ttu-id="60b44-117">Wert</span><span class="sxs-lookup"><span data-stu-id="60b44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b44-118">Header</span><span class="sxs-lookup"><span data-stu-id="60b44-118">Header</span></span><br/>  | <dl> <span data-ttu-id="60b44-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60b44-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60b44-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60b44-120">Library</span></span><br/> | <dl> <span data-ttu-id="60b44-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="60b44-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b44-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b44-123">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="60b44-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





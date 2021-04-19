---
description: Die Put \_ Rate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaposition::p UT- \_ Raten Methode.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: CPosPassThru.put_Rate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369366"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="3f532-104">Cpospassthru. Put \_ Rate-Methode</span><span class="sxs-lookup"><span data-stu-id="3f532-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="3f532-105">Die- `put_Rate` Methode legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="3f532-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="3f532-106">Diese Methode implementiert die [**imediaposition::p UT- \_ Raten**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) Methode.</span><span class="sxs-lookup"><span data-stu-id="3f532-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f532-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f532-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="3f532-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f532-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f532-109">*drate*</span><span class="sxs-lookup"><span data-stu-id="3f532-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="3f532-110">Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="3f532-110">Playback rate.</span></span> <span data-ttu-id="3f532-111">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3f532-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f532-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f532-112">Return value</span></span>

<span data-ttu-id="3f532-113">Gibt E \_ invalidArg zurück, wenn *drate* 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="3f532-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="3f532-114">Andernfalls wird der **HRESULT** -Wert aus der verbundenen Pin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f532-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f532-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f532-115">Remarks</span></span>

<span data-ttu-id="3f532-116">Negative Raten weisen auf die umgekehrte Wiedergabe hin.</span><span class="sxs-lookup"><span data-stu-id="3f532-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="3f532-117">Nicht alle Medien unterstützen die umgekehrte Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="3f532-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f532-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f532-118">Requirements</span></span>



| <span data-ttu-id="3f532-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f532-119">Requirement</span></span> | <span data-ttu-id="3f532-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3f532-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f532-121">Header</span><span class="sxs-lookup"><span data-stu-id="3f532-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f532-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f532-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f532-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f532-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f532-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3f532-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f532-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f532-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f532-126">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3f532-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





---
description: 'Die settimeformat-Methode legt das Zeitformat fest. Diese Methode implementiert die imediaseeking:: settimeformat-Methode.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Cpospassthru. settimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373773"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="daada-104">Cpospassthru. settimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="daada-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="daada-105">Die settimeformat-Methode legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="daada-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="daada-106">Diese Methode implementiert die [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="daada-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="daada-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="daada-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="daada-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="daada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daada-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="daada-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="daada-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="daada-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daada-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="daada-111">Return value</span></span>

<span data-ttu-id="daada-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="daada-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="daada-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daada-113">Requirements</span></span>



| <span data-ttu-id="daada-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daada-114">Requirement</span></span> | <span data-ttu-id="daada-115">Wert</span><span class="sxs-lookup"><span data-stu-id="daada-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daada-116">Header</span><span class="sxs-lookup"><span data-stu-id="daada-116">Header</span></span><br/>  | <dl> <span data-ttu-id="daada-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daada-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="daada-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="daada-118">Library</span></span><br/> | <dl> <span data-ttu-id="daada-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="daada-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daada-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daada-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daada-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="daada-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="daada-122">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="daada-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





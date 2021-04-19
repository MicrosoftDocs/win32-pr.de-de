---
description: 'Die getTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die imediaseeking:: getTimeFormat-Methode.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Cpospassthru. getTimeFormat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362146"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="e78a7-104">Cpospassthru. getTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="e78a7-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="e78a7-105">Die- `GetTimeFormat` Methode ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="e78a7-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="e78a7-106">Diese Methode implementiert die [**imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e78a7-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e78a7-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e78a7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e78a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78a7-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="e78a7-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e78a7-110">Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="e78a7-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78a7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e78a7-111">Return value</span></span>

<span data-ttu-id="e78a7-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="e78a7-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e78a7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e78a7-113">Requirements</span></span>



| <span data-ttu-id="e78a7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e78a7-114">Requirement</span></span> | <span data-ttu-id="e78a7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e78a7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78a7-116">Header</span><span class="sxs-lookup"><span data-stu-id="e78a7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e78a7-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e78a7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e78a7-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e78a7-118">Library</span></span><br/> | <dl> <span data-ttu-id="e78a7-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e78a7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e78a7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e78a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78a7-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e78a7-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="e78a7-122">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="e78a7-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





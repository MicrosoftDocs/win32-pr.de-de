---
description: 'Die querypreferredformat-Methode ruft das bevorzugte Zeitformat für den Stream ab. Diese Methode implementiert die imediaseeking:: querypreferredformat-Methode.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Cpospassthru. querypreferredformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372058"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="05639-104">Cpospassthru. querypreferredformat-Methode</span><span class="sxs-lookup"><span data-stu-id="05639-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="05639-105">Die- `QueryPreferredFormat` Methode ruft das bevorzugte Zeitformat für den Stream ab.</span><span class="sxs-lookup"><span data-stu-id="05639-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="05639-106">Diese Methode implementiert die [**imediaseeking:: querypreferredformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="05639-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05639-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05639-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="05639-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05639-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="05639-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="05639-110">Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="05639-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05639-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05639-111">Return value</span></span>

<span data-ttu-id="05639-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="05639-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="05639-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05639-113">Requirements</span></span>



| <span data-ttu-id="05639-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05639-114">Requirement</span></span> | <span data-ttu-id="05639-115">Wert</span><span class="sxs-lookup"><span data-stu-id="05639-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05639-116">Header</span><span class="sxs-lookup"><span data-stu-id="05639-116">Header</span></span><br/>  | <dl> <span data-ttu-id="05639-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05639-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05639-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05639-118">Library</span></span><br/> | <dl> <span data-ttu-id="05639-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="05639-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05639-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05639-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05639-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="05639-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="05639-122">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="05639-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





---
description: 'Die isusingtimeformat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist. Diese Methode implementiert die imediaseeking:: isusingtimeformat-Methode.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Cpospassthru. isusingtimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359817"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="eb0bc-104">Cpospassthru. isusingtimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="eb0bc-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="eb0bc-105">Die- `IsUsingTimeFormat` Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="eb0bc-106">Diese Methode implementiert die [**imediaseeking:: isusingtimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb0bc-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="eb0bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb0bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0bc-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="eb0bc-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="eb0bc-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0bc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb0bc-111">Return value</span></span>

<span data-ttu-id="eb0bc-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0bc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb0bc-113">Requirements</span></span>



| <span data-ttu-id="eb0bc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb0bc-114">Requirement</span></span> | <span data-ttu-id="eb0bc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="eb0bc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0bc-116">Header</span><span class="sxs-lookup"><span data-stu-id="eb0bc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eb0bc-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb0bc-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb0bc-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb0bc-118">Library</span></span><br/> | <dl> <span data-ttu-id="eb0bc-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb0bc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0bc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb0bc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0bc-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb0bc-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="eb0bc-122">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="eb0bc-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





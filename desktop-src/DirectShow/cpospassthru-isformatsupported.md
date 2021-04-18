---
description: 'Die isformatsupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die imediaseeking:: isformatsupported-Methode.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Cpospassthru. isformatsupported-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364474"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="2200a-104">Cpospassthru. isformatsupported-Methode</span><span class="sxs-lookup"><span data-stu-id="2200a-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="2200a-105">Die- `IsFormatSupported` Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2200a-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="2200a-106">Diese Methode implementiert die [**imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2200a-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2200a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2200a-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2200a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2200a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2200a-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="2200a-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2200a-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="2200a-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2200a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2200a-111">Return value</span></span>

<span data-ttu-id="2200a-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="2200a-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2200a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2200a-113">Requirements</span></span>



| <span data-ttu-id="2200a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2200a-114">Requirement</span></span> | <span data-ttu-id="2200a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2200a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2200a-116">Header</span><span class="sxs-lookup"><span data-stu-id="2200a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2200a-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2200a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2200a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2200a-118">Library</span></span><br/> | <dl> <span data-ttu-id="2200a-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2200a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2200a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2200a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2200a-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2200a-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="2200a-122">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="2200a-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





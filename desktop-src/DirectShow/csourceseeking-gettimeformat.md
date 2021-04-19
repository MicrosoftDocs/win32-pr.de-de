---
description: 'Die getTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die imediaseeking:: getTimeFormat-Methode.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Csourceseeking. getTimeFormat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372121"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="131b1-104">Csourceseeking. getTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="131b1-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="131b1-105">Die- `GetTimeFormat` Methode ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="131b1-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="131b1-106">Diese Methode implementiert die [**imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="131b1-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="131b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="131b1-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="131b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="131b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="131b1-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="131b1-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="131b1-110">Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="131b1-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="131b1-111">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="131b1-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="131b1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="131b1-112">Return value</span></span>

<span data-ttu-id="131b1-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="131b1-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="131b1-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="131b1-114">Return code</span></span>                                                                               | <span data-ttu-id="131b1-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="131b1-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="131b1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="131b1-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="131b1-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="131b1-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="131b1-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="131b1-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="131b1-119">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="131b1-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="131b1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="131b1-120">Remarks</span></span>

<span data-ttu-id="131b1-121">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="131b1-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="131b1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="131b1-122">Requirements</span></span>



| <span data-ttu-id="131b1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="131b1-123">Requirement</span></span> | <span data-ttu-id="131b1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="131b1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="131b1-125">Header</span><span class="sxs-lookup"><span data-stu-id="131b1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="131b1-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="131b1-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="131b1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="131b1-127">Library</span></span><br/> | <dl> <span data-ttu-id="131b1-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="131b1-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="131b1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="131b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="131b1-130">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="131b1-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





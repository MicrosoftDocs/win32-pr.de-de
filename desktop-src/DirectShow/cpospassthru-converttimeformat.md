---
description: 'Die converttimeformat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die imediaseeking:: converttimeformat-Methode.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Cpospassthru. converttimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367663"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="4039f-104">Cpospassthru. converttimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="4039f-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="4039f-105">Die- `ConvertTimeFormat` Methode konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="4039f-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="4039f-106">Diese Methode implementiert die [**imediaseeking:: converttimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4039f-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4039f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4039f-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4039f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4039f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4039f-109">*pTARGET*</span><span class="sxs-lookup"><span data-stu-id="4039f-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="4039f-110">Ein Zeiger auf eine Variable, die die konvertierte Zeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="4039f-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="4039f-111">*ptargetformat*</span><span class="sxs-lookup"><span data-stu-id="4039f-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4039f-112">Ein Zeiger auf die Zeitformat-GUID des Ziel Formats.</span><span class="sxs-lookup"><span data-stu-id="4039f-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="4039f-113">Wenn der Wert **null** ist, wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="4039f-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="4039f-114">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="4039f-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="4039f-115">Zeitwert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4039f-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="4039f-116">*psourceformat*</span><span class="sxs-lookup"><span data-stu-id="4039f-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4039f-117">Ein Zeiger auf die Zeitformat-GUID des zu konvertierenden Formats.</span><span class="sxs-lookup"><span data-stu-id="4039f-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="4039f-118">Wenn der Wert **null** ist, wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="4039f-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4039f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4039f-119">Return value</span></span>

<span data-ttu-id="4039f-120">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="4039f-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4039f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4039f-121">Requirements</span></span>



| <span data-ttu-id="4039f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4039f-122">Requirement</span></span> | <span data-ttu-id="4039f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4039f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4039f-124">Header</span><span class="sxs-lookup"><span data-stu-id="4039f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4039f-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4039f-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4039f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4039f-126">Library</span></span><br/> | <dl> <span data-ttu-id="4039f-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4039f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4039f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4039f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4039f-129">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4039f-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="4039f-130">**Zeit Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="4039f-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 





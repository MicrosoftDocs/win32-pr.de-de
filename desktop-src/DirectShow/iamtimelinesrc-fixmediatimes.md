---
description: Mit der fixmediatimes-Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Im Allgemeinen müssen Anwendungen diese Methode nicht aufzurufen.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Iamtimelinesrc:: fixmediatimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367520"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="de0a3-104">Iamtimelinesrc:: fixmediatimes-Methode</span><span class="sxs-lookup"><span data-stu-id="de0a3-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="de0a3-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="de0a3-105">\[Deprecated.</span></span> <span data-ttu-id="de0a3-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="de0a3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de0a3-107">Mit der- `FixMediaTimes` Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert.</span><span class="sxs-lookup"><span data-stu-id="de0a3-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="de0a3-108">Im Allgemeinen müssen Anwendungen diese Methode nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="de0a3-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de0a3-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="de0a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de0a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0a3-111">*PStart*</span><span class="sxs-lookup"><span data-stu-id="de0a3-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="de0a3-112">Zeiger auf eine Variable, die die Startzeit in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="de0a3-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="de0a3-113">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="de0a3-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="de0a3-114">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="de0a3-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="de0a3-115">Ein Zeiger auf eine Variable, die die Endzeit in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="de0a3-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="de0a3-116">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="de0a3-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0a3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de0a3-117">Return value</span></span>

<span data-ttu-id="de0a3-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="de0a3-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de0a3-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="de0a3-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de0a3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de0a3-120">Remarks</span></span>

<span data-ttu-id="de0a3-121">Diese Methode ähnelt der [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode, behält jedoch das ursprüngliche Verhältnis von Medien Zeiten und Zeitachsen Zeiten bei.</span><span class="sxs-lookup"><span data-stu-id="de0a3-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="de0a3-122">Wenn Sie nur die Zeiten auf die nächste Frame Grenze umrunden, kann dieses Verhältnis verzerrt werden.</span><span class="sxs-lookup"><span data-stu-id="de0a3-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="de0a3-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="de0a3-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de0a3-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="de0a3-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de0a3-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de0a3-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de0a3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de0a3-126">Requirements</span></span>



| <span data-ttu-id="de0a3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de0a3-127">Requirement</span></span> | <span data-ttu-id="de0a3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="de0a3-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de0a3-129">Header</span><span class="sxs-lookup"><span data-stu-id="de0a3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="de0a3-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="de0a3-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de0a3-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de0a3-131">Library</span></span><br/> | <dl> <span data-ttu-id="de0a3-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="de0a3-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0a3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de0a3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0a3-134">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="de0a3-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="de0a3-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="de0a3-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





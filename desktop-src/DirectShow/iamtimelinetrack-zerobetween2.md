---
description: 'Die ZeroBetween2-Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten. Diese Methode entspricht iamtimelinetrack:: zerobetween, erfordert jedoch reftime-Werte.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Iamtimelinetrack:: ZeroBetween2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360327"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="6fee6-104">Iamtimelinetrack:: ZeroBetween2-Methode</span><span class="sxs-lookup"><span data-stu-id="6fee6-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="6fee6-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6fee6-105">\[Deprecated.</span></span> <span data-ttu-id="6fee6-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6fee6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fee6-107">Die- `ZeroBetween2` Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten.</span><span class="sxs-lookup"><span data-stu-id="6fee6-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="6fee6-108">Diese Methode entspricht [**iamtimelinetrack:: zerobetween**](iamtimelinetrack-zerobetween.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="6fee6-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fee6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fee6-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="6fee6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fee6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fee6-111">*rtstart*</span><span class="sxs-lookup"><span data-stu-id="6fee6-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6fee6-112">Der Anfang des Bereichs, der gelöscht werden soll (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="6fee6-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="6fee6-113">*rtend*</span><span class="sxs-lookup"><span data-stu-id="6fee6-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6fee6-114">Das Ende des Bereichs, der gelöscht werden soll (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="6fee6-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fee6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fee6-115">Return value</span></span>

<span data-ttu-id="6fee6-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6fee6-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6fee6-117">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="6fee6-117">Possible values include the following.</span></span>



| <span data-ttu-id="6fee6-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6fee6-118">Return code</span></span>                                                                             | <span data-ttu-id="6fee6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fee6-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6fee6-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6fee6-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6fee6-121">Der Zeitbereich fällt über alle Elemente in der Spur hinaus.</span><span class="sxs-lookup"><span data-stu-id="6fee6-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="6fee6-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fee6-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6fee6-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6fee6-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="6fee6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fee6-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fee6-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6fee6-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fee6-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6fee6-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fee6-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6fee6-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fee6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fee6-128">Requirements</span></span>



| <span data-ttu-id="6fee6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fee6-129">Requirement</span></span> | <span data-ttu-id="6fee6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6fee6-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fee6-131">Header</span><span class="sxs-lookup"><span data-stu-id="6fee6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6fee6-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6fee6-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fee6-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fee6-133">Library</span></span><br/> | <dl> <span data-ttu-id="6fee6-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="6fee6-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fee6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fee6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fee6-136">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6fee6-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="6fee6-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="6fee6-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





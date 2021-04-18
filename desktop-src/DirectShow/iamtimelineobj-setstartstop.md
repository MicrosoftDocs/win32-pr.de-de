---
description: Mit der setstartend-Methode werden die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts festgelegt.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Iamtimelineobj:: setstartstation-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365554"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="15017-103">Iamtimelineobj:: setstartstation-Methode</span><span class="sxs-lookup"><span data-stu-id="15017-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="15017-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="15017-104">\[Deprecated.</span></span> <span data-ttu-id="15017-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="15017-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15017-106">Die `SetStartStop` -Methode legt die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="15017-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="15017-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15017-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="15017-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15017-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15017-109">*Starten*</span><span class="sxs-lookup"><span data-stu-id="15017-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="15017-110">Neue Startzeit in 100-Nanosecond-Einheiten oder – 1, um die vorhandene Startzeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="15017-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="15017-111">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="15017-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="15017-112">Neue Endzeit, in 100-Nanosecond-Einheiten oder – 1, um die vorhandene Endzeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="15017-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15017-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15017-113">Return value</span></span>

<span data-ttu-id="15017-114">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="15017-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="15017-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="15017-115">Return code</span></span>                                                                                  | <span data-ttu-id="15017-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15017-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="15017-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15017-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="15017-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="15017-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="15017-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="15017-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="15017-120">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="15017-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="15017-121"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="15017-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="15017-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="15017-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="15017-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15017-123">Remarks</span></span>

<span data-ttu-id="15017-124">Diese Methode wird von nachverfolgen, Kompositionen und Gruppen nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="15017-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="15017-125">Für diese Objekte ist die Startzeit immer 0 (null), und die Endzeit ist die maximale Endzeit der Objekte, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="15017-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="15017-126">Legen Sie keine Überlappungs Zeiten für Quell Objekte innerhalb desselben Titels fest. Dies kann zu nicht definiertem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="15017-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="15017-127">Bei Quell Objekten sind Start-und Endzeiten unabhängig von den Start-und Endzeiten des Mediums.</span><span class="sxs-lookup"><span data-stu-id="15017-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="15017-128">Wenn Sie ein Wertepaar ändern, ändert sich das andere nicht.</span><span class="sxs-lookup"><span data-stu-id="15017-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="15017-129">Um die Start-und Endzeit des Mediums festzulegen, müssen Sie die [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="15017-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="15017-130">Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="15017-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="15017-131">Um Frame-exakte Ausschnitte und Übergänge zu erhalten, legen Sie die Parameter *Start* und *Ende* auf Frame-Begrenzungen fest.</span><span class="sxs-lookup"><span data-stu-id="15017-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="15017-132">Sie können die [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode verwenden, um einen Zeitwert in die nächste Frame Grenze zu konvertieren, oder Sie können die folgende Funktion verwenden, um von der Frame Nummer in die Verweis Zeit zu konvertieren:</span><span class="sxs-lookup"><span data-stu-id="15017-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="15017-133">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="15017-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="15017-134">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="15017-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="15017-135">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15017-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15017-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15017-136">Requirements</span></span>



| <span data-ttu-id="15017-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15017-137">Requirement</span></span> | <span data-ttu-id="15017-138">Wert</span><span class="sxs-lookup"><span data-stu-id="15017-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15017-139">Header</span><span class="sxs-lookup"><span data-stu-id="15017-139">Header</span></span><br/>  | <dl> <span data-ttu-id="15017-140"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="15017-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="15017-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15017-141">Library</span></span><br/> | <dl> <span data-ttu-id="15017-142"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="15017-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15017-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15017-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15017-144">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="15017-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="15017-145">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="15017-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





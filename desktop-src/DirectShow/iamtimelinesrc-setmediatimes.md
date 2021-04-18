---
description: Die setmediatimes-Methode legt die Start-und Startzeiten des Mediums fest.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Iamtimelinesrc:: setmediatimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360921"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="8daf0-103">Iamtimelinesrc:: setmediatimes-Methode</span><span class="sxs-lookup"><span data-stu-id="8daf0-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="8daf0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8daf0-104">\[Deprecated.</span></span> <span data-ttu-id="8daf0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8daf0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8daf0-106">Die `SetMediaTimes` -Methode legt die Start-und Startzeiten des Mediums fest.</span><span class="sxs-lookup"><span data-stu-id="8daf0-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="8daf0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8daf0-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="8daf0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8daf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8daf0-109">*Starten*</span><span class="sxs-lookup"><span data-stu-id="8daf0-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="8daf0-110">Start Zeit der Medien in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="8daf0-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="8daf0-111">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="8daf0-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="8daf0-112">Endzeit der Medien in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="8daf0-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8daf0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8daf0-113">Return value</span></span>

<span data-ttu-id="8daf0-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8daf0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8daf0-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8daf0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8daf0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8daf0-116">Remarks</span></span>

<span data-ttu-id="8daf0-117">Die Medien Zeiten sind die Beendigung und Startzeiten in Relation zur ursprünglichen Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="8daf0-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="8daf0-118">Legen Sie die Medien Zeiten immer fest, wenn Sie der Zeitachse ein Video oder eine Audioquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8daf0-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="8daf0-119">Andernfalls können Renderingprobleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="8daf0-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="8daf0-120">Die Endzeit muss nach der Startzeit liegen.</span><span class="sxs-lookup"><span data-stu-id="8daf0-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="8daf0-121">Wenn Sie einen immer noch Frame aus einer Videoquelle verwenden möchten, legen Sie für die Endzeit einen größeren Wert als die Startzeit fest, z. b. 100 Nanosekunden.</span><span class="sxs-lookup"><span data-stu-id="8daf0-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="8daf0-122">Wenn Sie auf denselben Wert festlegen, wird ein Renderingfehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="8daf0-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="8daf0-123">Wenn die Zeitachsen Dauer nicht der Medien Dauer entspricht, wird die Quelle entsprechend gestreckt oder verkleinert.</span><span class="sxs-lookup"><span data-stu-id="8daf0-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="8daf0-124">Dies bewirkt, dass der Clip langsamer oder schneller als die erstellte Rate abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="8daf0-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="8daf0-125">(In einer Audioquelle tritt die Verschiebung der Tonhöhe auf.) Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="8daf0-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="8daf0-126">Sie können die Dauer der Quelldatei angeben, indem Sie die [**setmedialength**](iamtimelinesrc-setmedialength.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8daf0-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="8daf0-127">Wenn Sie eine Zeit für das Medien Ende festlegen, die die Dauer überschreitet, verkürzt des die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="8daf0-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="8daf0-128">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8daf0-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8daf0-129">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8daf0-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8daf0-130">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8daf0-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8daf0-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8daf0-131">Requirements</span></span>



| <span data-ttu-id="8daf0-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8daf0-132">Requirement</span></span> | <span data-ttu-id="8daf0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8daf0-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8daf0-134">Header</span><span class="sxs-lookup"><span data-stu-id="8daf0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8daf0-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8daf0-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8daf0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8daf0-136">Library</span></span><br/> | <dl> <span data-ttu-id="8daf0-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="8daf0-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8daf0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8daf0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8daf0-139">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8daf0-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="8daf0-140">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="8daf0-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





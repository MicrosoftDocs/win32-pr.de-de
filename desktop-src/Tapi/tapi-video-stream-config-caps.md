---
description: Die Struktur der TAPI-Video Datenstrom-Konfigurations Obergrenze \_ \_ \_ \_ ist in der Struktur der TAPI- \_ Stream-Konfigurations Obergrenze enthalten \_ \_ , wenn der capstype-Member auf den VideoCap-Member der streamconfigcapstype-Union festgelegt ist
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: TAPI_VIDEO_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365607"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="af8c7-103">Struktur des TAPI- \_ Video Daten \_ Strom- \_ Konfigurations \_ Caps</span><span class="sxs-lookup"><span data-stu-id="af8c7-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="af8c7-104">\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af8c7-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af8c7-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="af8c7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="af8c7-106">Die Struktur der **TAPI- \_ Video Datenstrom- \_ \_ Konfigurations \_** Obergrenze ist in der Struktur der [**TAPI-Stream- \_ \_ Konfigurations \_**](tapi-stream-config-caps.md) Obergrenze enthalten, wenn der **capstype** -Member auf den **VideoCap** -Member der [**streamconfigcapstype**](streamconfigcapstype.md) -Union festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="af8c7-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="af8c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af8c7-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="af8c7-108">Member</span><span class="sxs-lookup"><span data-stu-id="af8c7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="af8c7-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af8c7-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-110">Eine benutzerfreundliche Beschreibung des audiostreamkonfigurationstyp für die Anzeige für Anwendungs Benutzer.</span><span class="sxs-lookup"><span data-stu-id="af8c7-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-111">**Videostandard**</span><span class="sxs-lookup"><span data-stu-id="af8c7-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-112">Der verwendete Video Standard.</span><span class="sxs-lookup"><span data-stu-id="af8c7-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-113">**Input size**</span><span class="sxs-lookup"><span data-stu-id="af8c7-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-114">Eingabe Größe von Frame.</span><span class="sxs-lookup"><span data-stu-id="af8c7-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-115">**Mincroppingsize**</span><span class="sxs-lookup"><span data-stu-id="af8c7-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-116">Mindestgröße für das Zuschneiden.</span><span class="sxs-lookup"><span data-stu-id="af8c7-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-117">**Maxcroppingsize**</span><span class="sxs-lookup"><span data-stu-id="af8c7-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-118">Maximale zuschneidungs Größe.</span><span class="sxs-lookup"><span data-stu-id="af8c7-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-119">**Cropgranularityx**</span><span class="sxs-lookup"><span data-stu-id="af8c7-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-120">Die Granularität für das Zuschneiden auf der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-121">**Cropgranularityy**</span><span class="sxs-lookup"><span data-stu-id="af8c7-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-122">Die Granularität für das Zuschneiden auf der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-123">**Cropalignx**</span><span class="sxs-lookup"><span data-stu-id="af8c7-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-124">Ausrichtung von Zuschneiden der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-125">**Cropaligny**</span><span class="sxs-lookup"><span data-stu-id="af8c7-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-126">Ausrichtung von y-Achsen zuschneiden.</span><span class="sxs-lookup"><span data-stu-id="af8c7-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-127">**Minoutputsize**</span><span class="sxs-lookup"><span data-stu-id="af8c7-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-128">Mindestens resultierende Größe des Videofensters.</span><span class="sxs-lookup"><span data-stu-id="af8c7-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-129">**Maxoutputsize**</span><span class="sxs-lookup"><span data-stu-id="af8c7-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-130">Maximale resultierende Größe des Videofensters.</span><span class="sxs-lookup"><span data-stu-id="af8c7-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-131">**Outputgranularityx**</span><span class="sxs-lookup"><span data-stu-id="af8c7-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-132">Die Granularität der Ausgabegröße entlang der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-133">**Outputgranularityy**</span><span class="sxs-lookup"><span data-stu-id="af8c7-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-134">Die Granularität der Ausgabegröße entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-135">**Stretchtapsx**</span><span class="sxs-lookup"><span data-stu-id="af8c7-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-136">Streckung entlang der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-137">**Stretchtapsy**</span><span class="sxs-lookup"><span data-stu-id="af8c7-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-138">Streckung entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-139">**Shrinktapsx**</span><span class="sxs-lookup"><span data-stu-id="af8c7-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-140">Verkleinern entlang der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-141">**Shrinktapsy**</span><span class="sxs-lookup"><span data-stu-id="af8c7-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-142">Verkleinern entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="af8c7-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-143">**Minframeinterval**</span><span class="sxs-lookup"><span data-stu-id="af8c7-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-144">Minimaler Video Frame Intervall.</span><span class="sxs-lookup"><span data-stu-id="af8c7-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-145">**Maxframeinterval**</span><span class="sxs-lookup"><span data-stu-id="af8c7-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-146">Maximales Video Frame Intervall.</span><span class="sxs-lookup"><span data-stu-id="af8c7-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-147">**Minbitspersecond**</span><span class="sxs-lookup"><span data-stu-id="af8c7-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-148">Minimale Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="af8c7-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="af8c7-149">**Maxbitspersecond**</span><span class="sxs-lookup"><span data-stu-id="af8c7-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="af8c7-150">Maximale Anzahl von Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="af8c7-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af8c7-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af8c7-151">Requirements</span></span>



| <span data-ttu-id="af8c7-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af8c7-152">Requirement</span></span> | <span data-ttu-id="af8c7-153">Wert</span><span class="sxs-lookup"><span data-stu-id="af8c7-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af8c7-154">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="af8c7-154">TAPI version</span></span><br/> | <span data-ttu-id="af8c7-155">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="af8c7-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="af8c7-156">Header</span><span class="sxs-lookup"><span data-stu-id="af8c7-156">Header</span></span><br/>       | <dl> <span data-ttu-id="af8c7-157"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8c7-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af8c7-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af8c7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8c7-159">**TAPI \_ - \_ streamkonfigurationscaps \_**</span><span class="sxs-lookup"><span data-stu-id="af8c7-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 





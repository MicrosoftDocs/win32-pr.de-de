---
description: Die Struktur der TAPI \_ - \_ \_ audiostreamkonfigurationscaps \_ ist in der TAPI-Struktur der Daten \_ Strom \_ Konfiguration enthalten \_ , wenn das capstype-Element auf den audiocap-Member der streamconfigcapstype-Union festgelegt ist.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354146"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="4d89f-103">Struktur der TAPI \_ - \_ Audiostream- \_ Konfigurations Ober \_ Grenzen</span><span class="sxs-lookup"><span data-stu-id="4d89f-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="4d89f-104">\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d89f-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d89f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4d89f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4d89f-106">Die Struktur der **TAPI \_ - \_ \_ audiostreamkonfigurationscaps \_** ist in der TAPI-Struktur der Daten [**\_ Strom \_ Konfiguration \_**](tapi-stream-config-caps.md) enthalten, wenn das **capstype** -Element auf den **audiocap** -Member der [**streamconfigcapstype**](streamconfigcapstype.md) -Union festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4d89f-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d89f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d89f-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="4d89f-108">Member</span><span class="sxs-lookup"><span data-stu-id="4d89f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d89f-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d89f-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-110">Eine benutzerfreundliche Beschreibung des audiostreamkonfigurationstyp für die Anzeige für Anwendungs Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4d89f-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-111">**Minimumchannels**</span><span class="sxs-lookup"><span data-stu-id="4d89f-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-112">Die Mindestanzahl von Kanälen, die dem Stream zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4d89f-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-113">**Maximumchannels**</span><span class="sxs-lookup"><span data-stu-id="4d89f-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-114">Die maximale Anzahl von Kanälen, die dem Stream zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4d89f-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-115">**Channelsgranularität**</span><span class="sxs-lookup"><span data-stu-id="4d89f-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-116">Die Granularität der Kanalanzahl.</span><span class="sxs-lookup"><span data-stu-id="4d89f-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-117">**Minimumbitspersample**</span><span class="sxs-lookup"><span data-stu-id="4d89f-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-118">Die minimale Anzahl von Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="4d89f-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-119">**Maximumbitspersample**</span><span class="sxs-lookup"><span data-stu-id="4d89f-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-120">Die maximale Anzahl von Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="4d89f-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-121">**Bitspersamplegranularität**</span><span class="sxs-lookup"><span data-stu-id="4d89f-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-122">Die Granularität der Bits pro Stichproben Werten.</span><span class="sxs-lookup"><span data-stu-id="4d89f-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-123">**Minimumsamplefrequency**</span><span class="sxs-lookup"><span data-stu-id="4d89f-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-124">Die minimale Stichproben Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="4d89f-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-125">**Maximumsamplefrequency**</span><span class="sxs-lookup"><span data-stu-id="4d89f-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-126">Die maximale Stichproben Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="4d89f-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-127">**Samplefrequkocygranularität**</span><span class="sxs-lookup"><span data-stu-id="4d89f-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-128">Die Granularität der Werte für die Stichproben Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="4d89f-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-129">**Minimumavgbytespersec**</span><span class="sxs-lookup"><span data-stu-id="4d89f-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-130">Die minimalen durchschnittlichen Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4d89f-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-131">**Maximumavgbytespersec**</span><span class="sxs-lookup"><span data-stu-id="4d89f-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-132">Die maximale durchschnittliche Anzahl von Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4d89f-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="4d89f-133">**Avgbytespersecgranularität**</span><span class="sxs-lookup"><span data-stu-id="4d89f-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="4d89f-134">Die Granularität der Bytes pro Sekunde-Werte.</span><span class="sxs-lookup"><span data-stu-id="4d89f-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d89f-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d89f-135">Requirements</span></span>



| <span data-ttu-id="4d89f-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d89f-136">Requirement</span></span> | <span data-ttu-id="4d89f-137">Wert</span><span class="sxs-lookup"><span data-stu-id="4d89f-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d89f-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4d89f-138">TAPI version</span></span><br/> | <span data-ttu-id="4d89f-139">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4d89f-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="4d89f-140">Header</span><span class="sxs-lookup"><span data-stu-id="4d89f-140">Header</span></span><br/>       | <dl> <span data-ttu-id="4d89f-141"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d89f-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d89f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d89f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d89f-143">**TAPI \_ - \_ streamkonfigurationscaps \_**</span><span class="sxs-lookup"><span data-stu-id="4d89f-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 





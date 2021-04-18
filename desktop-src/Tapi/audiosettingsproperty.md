---
description: 'Die audiosettingsproperty-Enumeration wird von den Methoden itaudiosettings:: GetRange, itaudiosettings:: Get und itaudiosettings:: Set verwendet, um anzugeben, welche audioeinstellungs Eigenschaft adressiert wird.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Audiosettingsproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368448"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="4b9d1-103">Audiosettingsproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4b9d1-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="4b9d1-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b9d1-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4b9d1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b9d1-106">Die **audiosettingsproperty** -Enumeration wird von den Methoden [**itaudiosettings:: GetRange**](itaudiosettings-getrange.md), [**itaudiosettings:: Get**](itaudiosettings-get.md)und [**itaudiosettings:: Set**](itaudiosettings-set.md) verwendet, um anzugeben, welche audioeinstellungs Eigenschaft adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b9d1-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="4b9d1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4b9d1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b9d1-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**Audiosettings \_ Signallevel**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-110">Signsettings-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**Audiosettings- \_ silencethreshold**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-112">Eigenschaft für den Ruhe Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**Audiosettings- \_ Volume**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-114">Volume-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**Audiosettings- \_ Saldo**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-116">Balance-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**Audiosettings- \_ Lautstärke**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-118">Lautstärke-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**Audiosettings- \_ Treble**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-120">Treble-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**Audiosettings- \_ Bass**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-122">Bass-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="4b9d1-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**Audiosettings \_ Mono**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="4b9d1-124">Die monaural-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4b9d1-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b9d1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b9d1-125">Requirements</span></span>



| <span data-ttu-id="4b9d1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b9d1-126">Requirement</span></span> | <span data-ttu-id="4b9d1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4b9d1-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9d1-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4b9d1-128">TAPI version</span></span><br/> | <span data-ttu-id="4b9d1-129">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4b9d1-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="4b9d1-130">Header</span><span class="sxs-lookup"><span data-stu-id="4b9d1-130">Header</span></span><br/>       | <dl> <span data-ttu-id="4b9d1-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b9d1-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9d1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b9d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9d1-133">**Itaudiosettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-134">**Itaudiosettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="4b9d1-135">**Itaudiosettings:: Set**</span><span class="sxs-lookup"><span data-stu-id="4b9d1-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 





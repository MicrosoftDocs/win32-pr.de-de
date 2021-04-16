---
title: Ändern der Tonhöhe und der Wiedergabe Rate
description: Ändern der Tonhöhe und der Wiedergabe Rate
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- Wellenform-Audiodaten, Tonhöhe
- Waveform-Audioschnittstelle, Tonhöhe
- Wellenform-Audiodatei, Wiedergabe Rate
- Waveform-Audioschnittstelle, Wiedergabe Rate
- Wellenform-Audiodaten, Ändern der Tonhöhe
- Waveform-Audioschnittstelle, Ändern der Tonhöhe
- Wellenform-Audiodatei, Ändern der Wiedergabe Rate
- Waveform-Audioschnittstelle, Ändern der Wiedergabe Rate
- Ändern der Geschwindigkeit der Waveform-Audiowiedergabe
- Ändern der Waveform-audiotonhöhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473124"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="de282-113">Ändern der Tonhöhe und der Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="de282-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="de282-114">Einige Waveform-Audioausgabegeräte können die Tonhöhe und die Wiedergabe Rate von Waveform-Audiodaten variieren.</span><span class="sxs-lookup"><span data-stu-id="de282-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="de282-115">Nicht alle Waveform-Audiogeräte unterstützen Änderungen an der Tonhöhe und der Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="de282-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="de282-116">Informationen dazu, wie Sie feststellen können, ob ein bestimmtes Waveform-Audiogerät Änderungen an der Tonhöhe und Wiedergabe Rate unterstützt, finden Sie unter [Geräte und Datentypen](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="de282-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="de282-117">Die Unterschiede zwischen dem Ändern der Tonhöhe und der Wiedergabe Rate lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="de282-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="de282-118">Das Ändern der Wiedergabe Rate wird vom Gerätetreiber durchgeführt, und es ist keine spezielle Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de282-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="de282-119">Die Samplingrate wird nicht geändert, aber der Treiber interpoliert, indem er Beispiele übersprungen oder synthegiert.</span><span class="sxs-lookup"><span data-stu-id="de282-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="de282-120">Wenn die Wiedergabe Rate z. b. um den Faktor 2 geändert wird, überspringt der Treiber alle anderen Stichproben.</span><span class="sxs-lookup"><span data-stu-id="de282-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="de282-121">Zum Ändern der Tonhöhe ist spezielle Hardware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de282-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="de282-122">Die Wiedergabe Rate und die Stichprobenrate werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="de282-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="de282-123">Windows stellt die folgenden Funktionen zum Abfragen und Festlegen von Waveform-Audiodarstellung und Wiedergabe Raten bereit.</span><span class="sxs-lookup"><span data-stu-id="de282-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="de282-124">Funktion</span><span class="sxs-lookup"><span data-stu-id="de282-124">Function</span></span>                                                 | <span data-ttu-id="de282-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de282-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="de282-126">**waveoutgetpitch**</span><span class="sxs-lookup"><span data-stu-id="de282-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="de282-127">Ruft die Tonhöhe für das angegebene Waveform-Audioausgabegerät ab.</span><span class="sxs-lookup"><span data-stu-id="de282-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="de282-128">**waveoutgetplaybackrate**</span><span class="sxs-lookup"><span data-stu-id="de282-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="de282-129">Ruft die Wiedergabe Rate für das angegebene Waveform-Audioausgabegerät ab.</span><span class="sxs-lookup"><span data-stu-id="de282-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="de282-130">**waveoutsetpitch**</span><span class="sxs-lookup"><span data-stu-id="de282-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="de282-131">Legt die Tonhöhe für das angegebene Waveform-Audioausgabegerät fest.</span><span class="sxs-lookup"><span data-stu-id="de282-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="de282-132">**waveoutsetplaybackrate**</span><span class="sxs-lookup"><span data-stu-id="de282-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="de282-133">Legt die Wiedergabe Rate für das angegebene Waveform-Audioausgabegerät fest.</span><span class="sxs-lookup"><span data-stu-id="de282-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="de282-134">Die Tonhöhe und die Wiedergabe Raten werden um einen Faktor geändert, der durch eine in einen Double Word-Wert gepackte fest Komma Zahl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="de282-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="de282-135">Die oberen 16 Bits geben den ganzzahligen Teil der Zahl an. die unteren 16 Bits geben den Bruch Teil an.</span><span class="sxs-lookup"><span data-stu-id="de282-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="de282-136">Beispielsweise wird der Wert 1,5 als 0x00018000l dargestellt.</span><span class="sxs-lookup"><span data-stu-id="de282-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="de282-137">Der Wert 0,75 wird als 0x0000c000l dargestellt.</span><span class="sxs-lookup"><span data-stu-id="de282-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="de282-138">Der Wert 1,0 (0x00010000 bis) bedeutet, dass die Tonhöhe oder Wiedergabe Rate unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="de282-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 
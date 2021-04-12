---
title: Informationen zum Beispiel-audiodsp-Plug-in
description: Informationen zum Beispiel-audiodsp-Plug-in
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Windows Media Player-Plug-ins, Beispiele
- Plug-ins, Beispiele
- Plug-Ins für die digitale Signalverarbeitung, Beispiele
- DSP-Plug-ins, Beispiele
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audiobeispiele
- DSP-Plug-ins, Audiobeispiele
- Beispiele, DSP-Plug-ins
- audiodsp-Plug-ins, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310096"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="d8697-113">Informationen zum Beispiel-audiodsp-Plug-in</span><span class="sxs-lookup"><span data-stu-id="d8697-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="d8697-114">Das Beispiel-audiodsp-Plug-in bietet eine einfache Verarbeitungs Implementierung, die die Amplitude der Audiodaten um einen vom Benutzer auf der Eigenschaften Seite bereitgestellten Faktor skaliert.</span><span class="sxs-lookup"><span data-stu-id="d8697-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="d8697-115">Das Plug-in akzeptiert Werte zwischen 0 (null) und 1.</span><span class="sxs-lookup"><span data-stu-id="d8697-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="d8697-116">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="d8697-116">The default value is 1.</span></span> <span data-ttu-id="d8697-117">Der Wert 1 hat keine Auswirkung auf den Sound. Weitere Skalierungsfaktoren sind Multiplikatoren für die Audiobeispiele.</span><span class="sxs-lookup"><span data-stu-id="d8697-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="d8697-118">Der Wert 0,5 würde beispielsweise zu einer Abnahme von 6 Dezimalstellen führen.</span><span class="sxs-lookup"><span data-stu-id="d8697-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="d8697-119">Der Wert 0 (null) führt zu einer Ruhe.</span><span class="sxs-lookup"><span data-stu-id="d8697-119">A value of zero results in silence.</span></span>

<span data-ttu-id="d8697-120">Das Beispiel-audiodsp-Plug-in funktioniert mit Stereo-oder Mono-PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="d8697-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8697-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8697-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8697-122">**Aufbau eines DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="d8697-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 





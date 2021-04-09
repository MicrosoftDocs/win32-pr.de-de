---
title: Arbeiten mit High-Resolution PCM-Audiodatei
description: Arbeiten mit High-Resolution PCM-Audiodatei
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), hochauflösende PCM-Audiodaten
- ASF (Advanced Systems Format), hochauflösende PCM-Audiodaten
- Profile, hochauflösende PCM-Audiodaten
- Codecs, hochauflösende PCM-Audiodaten
- Advanced Systems Format (ASF), PCM-Audiodatei
- ASF (Advanced Systems Format), PCM-Audiodatei
- Profile, PCM-Audiodaten
- Codecs, PCM-Audiodaten
- hochauflösende PCM-Audiodaten
- PCM-Audiodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948856"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="6d6e2-113">Arbeiten mit High-Resolution PCM-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="6d6e2-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="6d6e2-114">Einige der Eingabeformate für den Windows Media Audio 9 Professional-Codec und den Windows Media Audio 9 verlustfreien Codec sind hochauflösende PCM-Formate.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="6d6e2-115">Dabei handelt es sich um PCM-Formate mit mehr als zwei Kanälen oder mehr als 16 Bits pro Stichprobe (Audiodaten mit mehr als zwei Kanälen werden auch als Multichannel-Audiodaten bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="6d6e2-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="6d6e2-116">Diese Formate werden mit einer strukturierten Erweiterung der [**WaveFormatEx**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) -Struktur konfiguriert, die als [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="6d6e2-117">Die **WAVEFORMATEXTENSIBLE** -Struktur enthält Informationen zu den Kanälen, die in der Audiodatei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="6d6e2-118">Diese Struktur ist erforderlich, wenn hochauflösende PCM-Audiodaten verwendet werden, da einige Windows-APIs keine **WaveFormatEx** -Strukturen akzeptieren, die Werte mit hoher Auflösung enthalten.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="6d6e2-119">Hochauflösende PCM-Formate verfügen über 22 Byte erweiterte Daten, die im **CBSIZE** -Member der **WaveFormatEx** -Struktur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="6d6e2-120">Bei Windows Media-Audioformaten mit hoher Auflösung wird die **WAVEFORMATEXTENSIBLE** -Struktur nicht verwendet, aber es werden erweiterte Daten an die **WaveFormatEx** -Struktur angehängt.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="6d6e2-121">Die Windows Media-Audiocodecs unterstützen nur das Decodieren in hochauflösende PCM-Formate, wenn die Anwendung unter Windows XP oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="6d6e2-122">In früheren Versionen von Microsoft Windows decodieren die Codecs in ein Format mit maximal 16 Bits pro Stichprobe und 2 Kanälen.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="6d6e2-123">Außerdem müssen Sie angeben, dass der Codec in High-Definition PCM decodiert werden soll, indem Sie die \_ Ausgabe Einstellung g wszene ablediskreteoutput mithilfe der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode auf " **true** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="6d6e2-124">Nach dem Ausführen dieses Aufrufes werden die vom Reader aufgelisteten Ausgaben zu hoch Definitions Formaten.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="6d6e2-125">Multichannel-Audiodaten erfordern mehr Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="6d6e2-126">Weitere Informationen finden Sie unter [Lesen von Multichannel-Audioinformationen](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="6d6e2-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d6e2-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d6e2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d6e2-128">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="6d6e2-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 
---
description: Audiofunktionen
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Audiofunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522528"
---
# <a name="audio-capabilities"></a><span data-ttu-id="c9b87-103">Audiofunktionen</span><span class="sxs-lookup"><span data-stu-id="c9b87-103">Audio Capabilities</span></span>

<span data-ttu-id="c9b87-104">Für Audiofunktionen gibt [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) ein Array von Paaren von " [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) " und " [**\_ Audiostream \_ config \_ "-**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="c9b87-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="c9b87-105">Wie bei Video können Sie damit auch alle Arten von Audiofunktionen auf der PIN verfügbar machen, wie z. b. die Daten Rate und ob Mono oder Stereo unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c9b87-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="c9b87-106">Video bezogene Beispiele in Bezug auf getstreamcaps finden Sie unter [Videofunktionen](video-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="c9b87-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="c9b87-107">Angenommen, Sie unterstützen das PCM (Pulse Code Modulation)-wellenformat (wie von der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur dargestellt) bei der Stichprobenentnahme von 11.025, 22.050 und 44.100 Stichproben pro Sekunde, alles bei 8-oder 16-Bit-Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="c9b87-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="c9b87-108">In diesem Fall würden Sie zwei Struktur Paare anbieten.</span><span class="sxs-lookup"><span data-stu-id="c9b87-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="c9b87-109">Das erste Paar hätte eine **\_ Audiostream \_ config \_ -** Funktionsstruktur, die besagt, dass Sie mindestens 11.025 bis maximal 22.050 Samplings pro Sekunde mit einer Granularität von 11.025 Stichproben pro Sekunde unterstützen (die Granularität ist der Unterschied zwischen unterstützten Werten); ein 8-Bit-minimal-zu-16-Bit-Bit pro Stichprobe mit einer Granularität von 8 Bits pro Stichprobe und einem minimal-und zwei Kanal Maximum.</span><span class="sxs-lookup"><span data-stu-id="c9b87-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="c9b87-110">Der Medientyp des ersten Paars wäre das standardmäßige PCM-Format in diesem Bereich, vielleicht 22 Kilohertz (kHz), 16-Bit-Stereo.</span><span class="sxs-lookup"><span data-stu-id="c9b87-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="c9b87-111">Ihr zweites Paar wäre eine Funktion, die 44.100 für die Mindest-und höchst Anzahl von Samplings pro Sekunde anzeigt. 8-Bit-(minimal) und 16-Bit-Bits (max) pro Stichprobe mit einer Granularität von 8 Bits pro Beispiel; und das minimal-und zwei-Kanal-Maximum mit einem Kanal.</span><span class="sxs-lookup"><span data-stu-id="c9b87-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="c9b87-112">Der Medientyp wäre das standardmäßige 44 kHz-Format, vielleicht 44 kHz 16-Bit-Stereo.</span><span class="sxs-lookup"><span data-stu-id="c9b87-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="c9b87-113">Wenn Sie nicht-PCM-Wellen Formate unterstützen, kann der Medientyp, der von dieser Methode zurückgegeben wird, anzeigen, welche nicht-PCM-Formate unterstützt werden (mit einer standardmäßigen Samplingrate, Bitrate und Kanälen), und die Funktionsstruktur, die den Medientyp begleitet, kann beschreiben, welche anderen Stichproben Raten, Bitraten und Kanäle</span><span class="sxs-lookup"><span data-stu-id="c9b87-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9b87-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9b87-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b87-115">Verfügbar machen von Erfassung und Komprimierungs Formaten</span><span class="sxs-lookup"><span data-stu-id="c9b87-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 

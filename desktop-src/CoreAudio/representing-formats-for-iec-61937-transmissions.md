---
description: Dank der Zunahme der Medien Speichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten für die Übertragung von Inhalten von PCs an Geräte wie z. b. den Empfänger "HDMI" oder "Display Port" identifizieren, beschreiben und verwenden.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Darstellen von Formaten für IEC 61937-Übertragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344213"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a><span data-ttu-id="29075-103">Darstellen von Formaten für IEC 61937-Übertragungen</span><span class="sxs-lookup"><span data-stu-id="29075-103">Representing Formats for IEC 61937 Transmissions</span></span>

<span data-ttu-id="29075-104">Dank der Zunahme der Medien Speichergeräte, die komprimierte Audioformate erfordern, müssen Anwendungen eine Vielzahl von neuen codierten Audioinhalten für die Übertragung von Inhalten von PCs an Geräte wie z. b. den Empfänger "HDMI" oder "Display Port" identifizieren, beschreiben und verwenden.</span><span class="sxs-lookup"><span data-stu-id="29075-104">With the increase in media storage devices that require compressed audio formats, applications must identify, describe, and use a variety of new encoded audio content for transmitting content from PCs to devices such as HDMI or DisplayPort receiver.</span></span>

<span data-ttu-id="29075-105">Um einen codierten Audiostream darzustellen, der über eine mit IEC 61937 kompatible Schnittstelle übertragen werden soll, muss eine Anwendung Folgendes bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="29075-105">To represent an encoded audio stream to be transmitted over an IEC 61937-compatible interface, an application must provide:</span></span>

-   <span data-ttu-id="29075-106">Die Eigenschaften eines codierten Audiostreams, der übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29075-106">The characteristics of an encoded audio stream to be transmitted.</span></span>

-   <span data-ttu-id="29075-107">Die Merkmale eines decodierten Audiostreams auf dem Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="29075-107">The characteristics of a decoded audio stream on the target device.</span></span>

<span data-ttu-id="29075-108">In Windows Vista und früheren Windows-Betriebssystemen kann eine Anwendung die Qualitätsstufe eines Audioformats von der Anzahl der Kanäle, der Stichprobengröße und der Datenrate eines Audiostreams, der das Format verwendet, ableiten.</span><span class="sxs-lookup"><span data-stu-id="29075-108">In Windows Vista and earlier Windows operating systems, an application can infer the quality level of an audio format from the number of channels, the sample size, and the data rate of an audio stream that uses the format.</span></span> <span data-ttu-id="29075-109">Bei einem PCM-Format sind diese Informationen über die **nchannels**-, **nsamplespersec**-und **navgbytespersec** -Member der **WaveFormatEx** -Struktur verfügbar, die das Format angibt.</span><span class="sxs-lookup"><span data-stu-id="29075-109">For a PCM format, this information is available from the **nChannels**, **nSamplesPerSec**, and **nAvgBytesPerSec** members of the **WAVEFORMATEX** structure that specifies the format.</span></span> <span data-ttu-id="29075-110">Bei einem nicht-PCM-Format wurden diese drei Member für das Speichern von Informationen über die komprimierten Daten im Audiostream bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="29075-110">For a non-PCM format, these three members have been commandeered to store information about the compressed data in the audio stream.</span></span> <span data-ttu-id="29075-111">Folglich fehlen in der **WaveFormatEx** -Strukturinformationen über die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate des nicht-PCM-Audiostreams, nachdem der Stream dekomprimiert und wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="29075-111">Thus, the **WAVEFORMATEX** structure lacks information about the effective number of channels, sample size, and data rate of the non-PCM audio stream after the stream is decompressed and played.</span></span> <span data-ttu-id="29075-112">Basierend auf den Informationen in dieser Struktur hat ein Benutzer oder eine Anwendung möglicherweise Schwierigkeiten beim Ableiten der Qualitätsstufe des nicht-PCM-Streams.</span><span class="sxs-lookup"><span data-stu-id="29075-112">Based on the information in this structure, a user or an application might have difficulty inferring the quality level of the non-PCM stream.</span></span>

<span data-ttu-id="29075-113">**WaveFormatEx** wurde auf die **WAVEFORMATEXTENSIBLE** -Struktur erweitert, um die zusätzlichen Datenstrom Merkmale bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="29075-113">The **WAVEFORMATEX** was extended to the **WAVEFORMATEXTENSIBLE** structure to provide the extra stream characteristics.</span></span> <span data-ttu-id="29075-114">Diese Struktur ist jedoch auch nicht ausreichend, um den Stream für IEC 61937-Übertragungen zu beschreiben, da Sie einen einzelnen Satz von Merkmalen darstellen und für nicht komprimierte PCM-Daten mit mehreren Kanälen verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="29075-114">However, this structure is also not adequate in describing the stream for IEC 61937 transmissions because it was intended to represent a single set of characteristics and used for uncompressed, multi-channel PCM data.</span></span>

<span data-ttu-id="29075-115">In Windows 7 löst das Betriebssystem dieses Problem durch die Unterstützung einer neuen Struktur, **WAVEFORMATEXTENSIBLE \_ IEC61937** , die die **WAVEFORMATEXTENSIBLE** -Struktur erweitert, um zwei Sätze von audiostreammerkmalen zu speichern: das codierte Audioformat vor der Übertragung und die Eigenschaften des Audiostreams, nachdem er decodiert wurde.</span><span class="sxs-lookup"><span data-stu-id="29075-115">In Windows 7, the operating system addresses this problem by providing support for a new structure, **WAVEFORMATEXTENSIBLE\_IEC61937** which extends **WAVEFORMATEXTENSIBLE** structure to store two sets of audio stream characteristics: the encoded audio format before transmission and characteristics of the audio stream after it has been decoded.</span></span> <span data-ttu-id="29075-116">Die neue Struktur gibt explizit die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate eines nicht-PCM-Formats an.</span><span class="sxs-lookup"><span data-stu-id="29075-116">The new structure explicitly specifies the effective number of channels, sample size, and data rate of a non-PCM format.</span></span> <span data-ttu-id="29075-117">Mit diesen Informationen kann eine Anwendung die Qualitätsstufe des nicht-PCM-Streams ableiten, nachdem Sie dekomprimiert und wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="29075-117">With this information, an application can infer the quality level of the non-PCM stream after it is decompressed and played.</span></span>

<span data-ttu-id="29075-118">Die **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur wird im "ksmedia. h"-Header deklariert, der im Windows 7 SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="29075-118">The **WAVEFORMATEXTENSIBLE\_IEC61937** structure is declared in the KsMedia.h header included with the Windows 7 SDK.</span></span> <span data-ttu-id="29075-119">Der **formatext** -Member ist die **WAVEFORMATEXTENSIBLE** -Struktur, die die Merkmale des zu übertragenden Datenstroms speichert.</span><span class="sxs-lookup"><span data-stu-id="29075-119">The **FormatExt** member is the **WAVEFORMATEXTENSIBLE** structure that stores the characteristics of the stream to be transmitted.</span></span> <span data-ttu-id="29075-120">Der **formatmember der** **WAVEFORMATEXTENSIBLE** -Struktur ist die **WaveFormatEx** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="29075-120">The **Format** member of the **WAVEFORMATEXTENSIBLE** structure is the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="29075-121">Der Inhalt dieser **WaveFormatEx** und **WAVEFORMATEXTENSIBLE** gibt einer Anwendung an, ob die Struktur als **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="29075-121">The contents of this **WAVEFORMATEX** and **WAVEFORMATEXTENSIBLE** indicate to an application whether the structure can be interpreted as a **WAVEFORMATEXTENSIBLE\_IEC61937** structure.</span></span> <span data-ttu-id="29075-122">Für eine **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur:</span><span class="sxs-lookup"><span data-stu-id="29075-122">For a **WAVEFORMATEXTENSIBLE\_IEC61937** structure:</span></span>

-   <span data-ttu-id="29075-123">Der **wformattag** -Member von **WaveFormatEx** muss das Wave- \_ Format \_ Extensible ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="29075-123">The **wFormatTag** member of **WAVEFORMATEX** must contain WAVE\_FORMAT\_EXTENSIBLE (`FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE`).</span></span>

-   <span data-ttu-id="29075-124">Der **unter Format** -Member der **WAVEFORMATEXTENSIBLE** -Struktur gibt die GUID des codierten Formats an, das übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29075-124">The **SubFormat** member of the **WAVEFORMATEXTENSIBLE** structure specifies the GUID of the encoded format to be transmitted.</span></span> <span data-ttu-id="29075-125">Beispielsweise `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` gibt das Dolby Digital Plus-Format an.</span><span class="sxs-lookup"><span data-stu-id="29075-125">For example, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indicates the Dolby Digital Plus format.</span></span> <span data-ttu-id="29075-126">Informationen zu unterstützten GUIDs finden Sie unter unter Format-GUIDs.</span><span class="sxs-lookup"><span data-stu-id="29075-126">For the supported GUIDs, see SubFormat GUIDs.</span></span>

-   <span data-ttu-id="29075-127">Die Größe, die durch das **CBSIZE** -Element von WaveFormatEx angegeben wird, beträgt 34 Bytes.</span><span class="sxs-lookup"><span data-stu-id="29075-127">The size indicated by **cbSize** member of the WAVEFORMATEX is 34 bytes.</span></span> <span data-ttu-id="29075-128">(`FormatExt.Format.cbSize = 34`).</span><span class="sxs-lookup"><span data-stu-id="29075-128">(`FormatExt.Format.cbSize = 34`).</span></span> <span data-ttu-id="29075-129">Die Gesamtgröße von **WAVEFORMATEXTENSIBLE \_ IEC61937** beträgt 52 bytes.</span><span class="sxs-lookup"><span data-stu-id="29075-129">The total size of **WAVEFORMATEXTENSIBLE\_IEC61937** is 52 bytes.</span></span>

<span data-ttu-id="29075-130">Die Member **dwencodedsamplespersec**, **dwencodedchannelcount** und **dwaveragebytespersec** von **WAVEFORMATEXTENSIBLE \_ IEC61937** beschreiben die Samplingrate, die Anzahl der Kanäle und die Bitrate in Bytes des Streams des Audiostreams, nachdem er decodiert wurde.</span><span class="sxs-lookup"><span data-stu-id="29075-130">The **dwEncodedSamplesPerSec**, **dwEncodedChannelCount**, and **dwAverageBytesPerSec** members of **WAVEFORMATEXTENSIBLE\_IEC61937** describe the sampling rate, number of channels, and bit rate in bytes of the stream of the audio stream after it has been decoded.</span></span>

## <a name="subformat-guids"></a><span data-ttu-id="29075-131">Unter Format-GUIDs</span><span class="sxs-lookup"><span data-stu-id="29075-131">SubFormat GUIDs</span></span>

<span data-ttu-id="29075-132">In Windows 7 enthält der Header "ksmedia. h" Definitionen für die unter Format-GUIDs für die von CEA-861-D definierten komprimierten Audioformate.</span><span class="sxs-lookup"><span data-stu-id="29075-132">In Windows 7, the KsMedia.h header contains definitions for the SubFormat GUIDs for the compressed audio formats defined by CEA-861-D.</span></span> <span data-ttu-id="29075-133">Die GUIDs werden im unter Format-Member von **WAVEFORMATEXTENSIBLE** angegeben, der im **formatext** -Member der **WAVEFORMATEXTENSIBLE \_ IEC61937** -Struktur () angegeben wird `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` .</span><span class="sxs-lookup"><span data-stu-id="29075-133">The GUIDs are specified in the SubFormat member of the **WAVEFORMATEXTENSIBLE**, specified in the **FormatExt** member of the **WAVEFORMATEXTENSIBLE\_IEC61937** structure (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`).</span></span>

<span data-ttu-id="29075-134">Die GUIDs für die komprimierten Audioformate, die als standardmäßige IEC 61937-codierte Audioformate verfügbar sind, sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="29075-134">The GUIDs for the compressed audio formats that are available as standard IEC 61937 encoded audio formats are listed in the following table.</span></span> <span data-ttu-id="29075-135">Diese Formate ähneln den vorhandenen aktiven Codierungs-3-Formaten (AC-3) und Digital Theater Sound (DTS)-Formaten in Windows.</span><span class="sxs-lookup"><span data-stu-id="29075-135">These formats are similar to the existing Active Coding 3 (AC-3) and Digital Theater Sound (DTS) formats representations in Windows.</span></span>



| <span data-ttu-id="29075-136">CEA 861-Typ</span><span class="sxs-lookup"><span data-stu-id="29075-136">CEA 861 Type</span></span> | <span data-ttu-id="29075-137">Unter Format-GUID</span><span class="sxs-lookup"><span data-stu-id="29075-137">SubFormat GUID</span></span>                                                                                                          | <span data-ttu-id="29075-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29075-138">Description</span></span>                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="29075-139">0x00</span><span class="sxs-lookup"><span data-stu-id="29075-139">0x00</span></span>         |                                                                                                                         | <span data-ttu-id="29075-140">Verweisen Sie auf den Stream.</span><span class="sxs-lookup"><span data-stu-id="29075-140">Refer to the stream.</span></span>                         |
| <span data-ttu-id="29075-141">0x01</span><span class="sxs-lookup"><span data-stu-id="29075-141">0x01</span></span>         | <span data-ttu-id="29075-142">00000000-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-142">00000000-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-143">ksdataformat- \_ Untertyp \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="29075-143">KSDATAFORMAT\_SUBTYPE\_WAVEFORMATEX</span></span><br/>                          | <span data-ttu-id="29075-144">IEC 60958 PCM</span><span class="sxs-lookup"><span data-stu-id="29075-144">IEC 60958 PCM</span></span>                                |
| <span data-ttu-id="29075-145">0x02</span><span class="sxs-lookup"><span data-stu-id="29075-145">0x02</span></span>         | <span data-ttu-id="29075-146">00000092-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-146">00000092-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-147">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital</span><span class="sxs-lookup"><span data-stu-id="29075-147">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL</span></span><br/>              | <span data-ttu-id="29075-148">AC-3</span><span class="sxs-lookup"><span data-stu-id="29075-148">AC-3</span></span>                                         |
| <span data-ttu-id="29075-149">0x03</span><span class="sxs-lookup"><span data-stu-id="29075-149">0x03</span></span>         | <span data-ttu-id="29075-150">00000003-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-150">00000003-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-151">Ksdataformat- \_ Untertyp \_ IEC61937 \_ MPEG1</span><span class="sxs-lookup"><span data-stu-id="29075-151">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG1</span></span><br/>                       | <span data-ttu-id="29075-152">MPEG-1 (Schicht 1 & 2)</span><span class="sxs-lookup"><span data-stu-id="29075-152">MPEG-1 (Layer 1 & 2)</span></span>                         |
| <span data-ttu-id="29075-153">0x04</span><span class="sxs-lookup"><span data-stu-id="29075-153">0x04</span></span>         | <span data-ttu-id="29075-154">00000004-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-154">00000004-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-155">Ksdataformat- \_ Untertyp \_ IEC61937 \_ mpeg3</span><span class="sxs-lookup"><span data-stu-id="29075-155">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG3</span></span><br/>                       | <span data-ttu-id="29075-156">MPEG-3 (Schicht 3)</span><span class="sxs-lookup"><span data-stu-id="29075-156">MPEG-3 (Layer 3)</span></span>                             |
| <span data-ttu-id="29075-157">0x05</span><span class="sxs-lookup"><span data-stu-id="29075-157">0x05</span></span>         | <span data-ttu-id="29075-158">00000005-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-158">00000005-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-159">Ksdataformat- \_ Untertyp \_ IEC61937 \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="29075-159">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG2</span></span> <br/>                      | <span data-ttu-id="29075-160">MPEG-2 (Multichannel)</span><span class="sxs-lookup"><span data-stu-id="29075-160">MPEG-2(multichannel)</span></span>                         |
| <span data-ttu-id="29075-161">0x06</span><span class="sxs-lookup"><span data-stu-id="29075-161">0x06</span></span>         | <span data-ttu-id="29075-162">00000006-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-162">00000006-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-163">Ksdataformat- \_ Untertyp \_ IEC61937 \_ AAC</span><span class="sxs-lookup"><span data-stu-id="29075-163">KSDATAFORMAT\_SUBTYPE\_IEC61937\_AAC</span></span><br/>                         | <span data-ttu-id="29075-164">Erweiterte Audiocodierung (MPEG-2/4 AAC in ADTs)</span><span class="sxs-lookup"><span data-stu-id="29075-164">Advanced Audio Coding (MPEG-2/4 AAC in ADTS)</span></span> |
| <span data-ttu-id="29075-165">0x07</span><span class="sxs-lookup"><span data-stu-id="29075-165">0x07</span></span>         | <span data-ttu-id="29075-166">00000008-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-166">00000008-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-167">Ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS</span><span class="sxs-lookup"><span data-stu-id="29075-167">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS</span></span><br/>                         | <span data-ttu-id="29075-168">DTS</span><span class="sxs-lookup"><span data-stu-id="29075-168">DTS</span></span>                                          |
| <span data-ttu-id="29075-169">0x0A</span><span class="sxs-lookup"><span data-stu-id="29075-169">0x0a</span></span>         | <span data-ttu-id="29075-170">0000000A-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-170">0000000a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-171">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus</span><span class="sxs-lookup"><span data-stu-id="29075-171">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS</span></span><br/>        | <span data-ttu-id="29075-172">Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="29075-172">Dolby Digital Plus</span></span>                           |
| <span data-ttu-id="29075-173">0x0A</span><span class="sxs-lookup"><span data-stu-id="29075-173">0x0a</span></span>         | <span data-ttu-id="29075-174">0000010a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-174">0000010a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-175">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ Atmos</span><span class="sxs-lookup"><span data-stu-id="29075-175">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS\_ATMOS</span></span><br/> | <span data-ttu-id="29075-176">Dolby Atmos, codiert mit Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="29075-176">Dolby Atmos encoded with Dolby Digital Plus</span></span>  |
| <span data-ttu-id="29075-177">0x0f</span><span class="sxs-lookup"><span data-stu-id="29075-177">0x0f</span></span>         |                                                                                                                         | <span data-ttu-id="29075-178">Nicht verwendet reserviert</span><span class="sxs-lookup"><span data-stu-id="29075-178">Unused Reserved</span></span>                              |



 

<span data-ttu-id="29075-179">In der folgenden Tabelle sind die GUIDs für die komprimierten Audioformate aufgeführt, die in den audiobeispielpaketen mit hoher Bitrate übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="29075-179">The GUIDs for the compressed audio formats that are transmitted in high bit-rate audio sample packets are listed in the following table.</span></span>



| <span data-ttu-id="29075-180">CEA 861-Typ</span><span class="sxs-lookup"><span data-stu-id="29075-180">CEA 861 Type</span></span> | <span data-ttu-id="29075-181">Unter Format-GUID</span><span class="sxs-lookup"><span data-stu-id="29075-181">SubFormat GUID</span></span>                                                                                           | <span data-ttu-id="29075-182">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29075-182">Description</span></span>                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29075-183">0x0B</span><span class="sxs-lookup"><span data-stu-id="29075-183">0x0b</span></span>         | <span data-ttu-id="29075-184">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-184">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-185">Ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="29075-185">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/>      | <span data-ttu-id="29075-186">DTS-HD (24-Bit, 96kHz)</span><span class="sxs-lookup"><span data-stu-id="29075-186">DTS-HD (24-bit, 96Khz)</span></span>                                                                                                          |
| <span data-ttu-id="29075-187">0x0c</span><span class="sxs-lookup"><span data-stu-id="29075-187">0x0c</span></span>         | <span data-ttu-id="29075-188">0000000c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-188">0000000c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-189">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MLP</span><span class="sxs-lookup"><span data-stu-id="29075-189">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MLP</span></span><br/>   | <span data-ttu-id="29075-190">Dolby Mat 1,0:</span><span class="sxs-lookup"><span data-stu-id="29075-190">Dolby MAT 1.0:</span></span><br/> <span data-ttu-id="29075-191">Dolby TrueHD (MLP – Verlust lose Verpackung) – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle)</span><span class="sxs-lookup"><span data-stu-id="29075-191">Dolby TrueHD (MLP – Meridian Lossless Packing) – 24-bit 192KHz/up to 18 Mbps, 8 channels)</span></span> <br/> |
| <span data-ttu-id="29075-192">0x0c</span><span class="sxs-lookup"><span data-stu-id="29075-192">0x0c</span></span>         | <span data-ttu-id="29075-193">0000010c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-193">0000010c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-194">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MAT20</span><span class="sxs-lookup"><span data-stu-id="29075-194">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT20</span></span><br/> | <span data-ttu-id="29075-195">Dolby Mat 2,0:</span><span class="sxs-lookup"><span data-stu-id="29075-195">Dolby MAT 2.0:</span></span> <br/> <span data-ttu-id="29075-196">Dolby TrueHD – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle oder LPCM bis zu 24 Mbit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-196">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="29075-197">0x0c</span><span class="sxs-lookup"><span data-stu-id="29075-197">0x0c</span></span>         | <span data-ttu-id="29075-198">0000030c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-198">0000030c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-199">Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ MAT21</span><span class="sxs-lookup"><span data-stu-id="29075-199">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT21</span></span><br/> | <span data-ttu-id="29075-200">Dolby Mat 2,1:</span><span class="sxs-lookup"><span data-stu-id="29075-200">Dolby MAT 2.1:</span></span> <br/> <span data-ttu-id="29075-201">Dolby TrueHD – 24-Bit-192 kHz/bis zu 18 Mbit/s, 8 Kanäle oder LPCM bis zu 24 Mbit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-201">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="29075-202">0x0E</span><span class="sxs-lookup"><span data-stu-id="29075-202">0x0e</span></span>         | <span data-ttu-id="29075-203">00000164-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-203">00000164-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-204">Ksdataformat- \_ Untertyp \_ IEC61937 \_ WMA \_ pro</span><span class="sxs-lookup"><span data-stu-id="29075-204">KSDATAFORMAT\_SUBTYPE\_IEC61937\_WMA\_PRO</span></span><br/>     | <span data-ttu-id="29075-205">Windows Media Audio (WMA) pro</span><span class="sxs-lookup"><span data-stu-id="29075-205">Windows Media Audio (WMA) Pro</span></span>                                                                                                   |



 

<span data-ttu-id="29075-206">Der von Microsoft bereitgestellte HD-audioklassen-Treiber unterstützt PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, Matt</span><span class="sxs-lookup"><span data-stu-id="29075-206">Microsoft-provided HD Audio class driver supports PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP) formats.</span></span> <span data-ttu-id="29075-207">Die GUIDs für die komprimierten Audioformate, die nicht vom Treiber der HD-audioklasse unterstützt werden und von Drittanbieter Lösungen implementiert werden können, sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="29075-207">The GUIDs for the compressed audio formats that are not supported by the HD audio class driver and can be implemented by third-party solutions are listed in the following table.</span></span>



| <span data-ttu-id="29075-208">CEA 861-Typ</span><span class="sxs-lookup"><span data-stu-id="29075-208">CEA 861 Type</span></span> | <span data-ttu-id="29075-209">Unter Format-GUID</span><span class="sxs-lookup"><span data-stu-id="29075-209">SubFormat GUID</span></span>                                                                                              | <span data-ttu-id="29075-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29075-210">Description</span></span>                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="29075-211">0x08</span><span class="sxs-lookup"><span data-stu-id="29075-211">0x08</span></span>         | <span data-ttu-id="29075-212">00000008-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-212">00000008-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-213">Ksdataformat- \_ Untertyp \_ IEC61937 \_ ATRAC</span><span class="sxs-lookup"><span data-stu-id="29075-213">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ATRAC</span></span><br/>           | <span data-ttu-id="29075-214">Adaptive Transform-akustische Codierung (ATRAC)</span><span class="sxs-lookup"><span data-stu-id="29075-214">Adaptive Transform Acoustic Coding (ATRAC)</span></span>                                     |
| <span data-ttu-id="29075-215">0x09</span><span class="sxs-lookup"><span data-stu-id="29075-215">0x09</span></span>         | <span data-ttu-id="29075-216">00000009-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-216">00000009-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-217">Ksdataformat \_ \_ -Untertyp \_ IEC61937 \_ One \_ -Bit-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29075-217">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ONE\_BIT\_AUDIO</span></span><br/> | <span data-ttu-id="29075-218">One-Bit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="29075-218">One-Bit Audio</span></span>                                                                  |
| <span data-ttu-id="29075-219">0x0D</span><span class="sxs-lookup"><span data-stu-id="29075-219">0x0d</span></span>         | <span data-ttu-id="29075-220">0000000D-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="29075-220">0000000d-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="29075-221">Ksdataformat- \_ Untertyp \_ IEC61937 \_ DST</span><span class="sxs-lookup"><span data-stu-id="29075-221">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DST</span></span><br/>             | <span data-ttu-id="29075-222">Direct Stream Transport (DST) – Verlust lose komprimierte DSD (Direct Stream Digital).</span><span class="sxs-lookup"><span data-stu-id="29075-222">Direct Stream Transport (DST)—lossless compressed DSD (Direct Stream Digital).</span></span> |



 

## <a name="dolby-digital-plus-format"></a><span data-ttu-id="29075-223">Dolby Digital Plus-Format</span><span class="sxs-lookup"><span data-stu-id="29075-223">Dolby Digital Plus Format</span></span>

<span data-ttu-id="29075-224">Wenn Dolby Digital Plus-Inhalt über IEC 60958 übertragen wird, muss die linksamplingrate viermal so oft wie die Samplingrate des Inhalts sein.</span><span class="sxs-lookup"><span data-stu-id="29075-224">When Dolby Digital Plus content is transmitted over IEC 60958, the link-sampling rate must be four times the sampling rate of the content.</span></span> <span data-ttu-id="29075-225">Dolby Digital Plus unterstützt die Inhalts Stichproben Raten 32 kHz, 44,1 kHz und 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="29075-225">Dolby Digital Plus supports content sample rates of 32 KHz, 44.1 KHz, and 48 KHz.</span></span> <span data-ttu-id="29075-226">Schnittstellen wie z. b. "HDMI" unterstützen 128 kHz (32 kHz x 4) nicht. Daher können nur die Samplingrate für 44,1 und 48 kHz unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="29075-226">Interfaces such as HDMI do not support 128 KHz (32 KHz x 4), so only 44.1 and 48 KHz content sample rates can be supported.</span></span>

<span data-ttu-id="29075-227">Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um Dolby Digital Plus-Format mit einer Inhalts Stichproben Rate von 48 kHz darzustellen, werden im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="29075-227">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby Digital Plus format at a content sample rate of 48 KHz are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a><span data-ttu-id="29075-228">Dolby TrueHD (Matt)</span><span class="sxs-lookup"><span data-stu-id="29075-228">Dolby TrueHD (MAT)</span></span>

<span data-ttu-id="29075-229">Der Dolby TrueHD-Inhalt wird über IEC 60958 auf 176,4 kHz/8-Kanälen übertragen (die IEC 60958-Frame Rate von 705,6 kHz erfordert), um die Inhalts Stichproben Raten von 44,1, 88,2 und 176,4 kHz und 192 kHz/8-Kanälen (die eine IEC 60958-Frame Rate von 768 kHz erfordert) für die Inhalts Stichprobenrate von 48, 96 und 192.</span><span class="sxs-lookup"><span data-stu-id="29075-229">Dolby TrueHD content is transmitted over IEC 60958 at 176.4 kHz / 8 channels (requiring an IEC 60958 frame rate of 705.6 kHz) for content sample rates of 44.1, 88.2 and 176.4 kHz, and 192 kHz / 8 channels (requiring an IEC 60958 frame rate of 768 kHz) for content sample rates of 48, 96 and 192 kHz.</span></span>

<span data-ttu-id="29075-230">Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um Dolby TrueHD mit einer Inhalts Stichproben Rate von 96 kHz darzustellen, werden in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="29075-230">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby TrueHD at a content sample rate of 96 KHz are shown in the following examples.</span></span>

<span data-ttu-id="29075-231">Dolby Mat 1,0</span><span class="sxs-lookup"><span data-stu-id="29075-231">Dolby MAT 1.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="29075-232">Dolby Mat 2,0</span><span class="sxs-lookup"><span data-stu-id="29075-232">Dolby MAT 2.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="29075-233">Dolby Mat 2,1</span><span class="sxs-lookup"><span data-stu-id="29075-233">Dolby MAT 2.1</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> <span data-ttu-id="29075-234">Die Unterstützung für eine Version von Dolby Mat impliziert keine Unterstützung für Dolby Mat mit einer niedrigeren Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="29075-234">Support for one version of Dolby MAT does not imply support for Dolby MAT with a lower version number.</span></span> <span data-ttu-id="29075-235">Da Dolby Mat 2,1 abwärts kompatibel mit früheren Versionen von Dolby Mat ist, gibt ein Klassen Treiber, der Unterstützung für Dolby Mat 2,1 angibt, in der Regel auch die Unterstützung für Dolby Matt 2,0 und Dolby Matt 1,0 an, wobei für jede Version eine separate WAVEFORMATEXTENSIBLE IEC61937-Struktur verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="29075-235">Since Dolby MAT 2.1 is backwards compatible with previous versions of Dolby MAT, a class driver that indicates support for Dolby MAT 2.1 will typically also indicate support for Dolby MAT 2.0 and Dolby MAT 1.0, using a separate WAVEFORMATEXTENSIBLE\_IEC61937 structure for each version.</span></span>

 

## <a name="wma-pro"></a><span data-ttu-id="29075-236">WMA Pro</span><span class="sxs-lookup"><span data-stu-id="29075-236">WMA Pro</span></span>

<span data-ttu-id="29075-237">Der WMA pro-Audioinhalt kann in einem der vier profile codiert werden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="29075-237">WMA Pro audio content can be encoded in one of the four profiles listed in the following table.</span></span>



| <span data-ttu-id="29075-238">Profil</span><span class="sxs-lookup"><span data-stu-id="29075-238">Profile</span></span> | <span data-ttu-id="29075-239">Eigenschafts Wert</span><span class="sxs-lookup"><span data-stu-id="29075-239">Property - Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="29075-240">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29075-240">Description</span></span>                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29075-241">M0</span><span class="sxs-lookup"><span data-stu-id="29075-241">M0</span></span>      | <span data-ttu-id="29075-242">Maximale Bitrate – 192000 Bit/s</span><span class="sxs-lookup"><span data-stu-id="29075-242">Maximum bit rate – 192000 bps</span></span> <br/> <span data-ttu-id="29075-243">Maximale Samplingrate – 48 kHz</span><span class="sxs-lookup"><span data-stu-id="29075-243">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="29075-244">Maximale Anzahl von Kanälen – 2</span><span class="sxs-lookup"><span data-stu-id="29075-244">Maximum channel count – 2</span></span> <br/> <span data-ttu-id="29075-245">Maximale Puffergröße – 600 \* 1024 Bits</span><span class="sxs-lookup"><span data-stu-id="29075-245">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="29075-246">Maximale Anzahl von Samplings pro Frame – 2048</span><span class="sxs-lookup"><span data-stu-id="29075-246">Maximum samples per frame – 2048</span></span> <br/> <span data-ttu-id="29075-247">Maximale Anzahl von Bits pro Frame-655536</span><span class="sxs-lookup"><span data-stu-id="29075-247">Maximum bits per frame - 655536</span></span><br/>   | <span data-ttu-id="29075-248">Empfohlen für die Musik und das Streaming per Funk.</span><span class="sxs-lookup"><span data-stu-id="29075-248">Recommended for over-the-air music and streaming.</span></span><br/> <span data-ttu-id="29075-249">Die maximale Bitrate in einem audioframe beträgt 1536000 Bit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-249">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/>          |
| <span data-ttu-id="29075-250">M1</span><span class="sxs-lookup"><span data-stu-id="29075-250">M1</span></span>      | <span data-ttu-id="29075-251">Maximale Bitrate – 385000 Bit/s</span><span class="sxs-lookup"><span data-stu-id="29075-251">Maximum bit rate – 385000 bps</span></span> <br/> <span data-ttu-id="29075-252">Maximale Samplingrate – 48 kHz</span><span class="sxs-lookup"><span data-stu-id="29075-252">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="29075-253">Maximale Anzahl von Kanälen – 6</span><span class="sxs-lookup"><span data-stu-id="29075-253">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="29075-254">Maximale Puffergröße – 600 \* 1024 Bits</span><span class="sxs-lookup"><span data-stu-id="29075-254">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="29075-255">Maximale Anzahl von Samplings pro Frame – 4096</span><span class="sxs-lookup"><span data-stu-id="29075-255">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="29075-256">Maximale Anzahl von Bits pro Frame-131072</span><span class="sxs-lookup"><span data-stu-id="29075-256">Maximum bits per frame - 131072</span></span><br/>   | <span data-ttu-id="29075-257">Empfohlen für Filme mit Standarddefinitionen für umschließende Sounds.</span><span class="sxs-lookup"><span data-stu-id="29075-257">Recommended for surround-sound standard definition movies.</span></span><br/> <span data-ttu-id="29075-258">Die maximale Bitrate in einem audioframe beträgt 1536000 Bit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-258">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/> |
| <span data-ttu-id="29075-259">M2</span><span class="sxs-lookup"><span data-stu-id="29075-259">M2</span></span>      | <span data-ttu-id="29075-260">Maximale Bitrate – 769000 Bit/s</span><span class="sxs-lookup"><span data-stu-id="29075-260">Maximum bit rate – 769000 bps</span></span> <br/> <span data-ttu-id="29075-261">Maximale Samplingrate – 96 kHz</span><span class="sxs-lookup"><span data-stu-id="29075-261">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="29075-262">Maximale Anzahl von Kanälen – 6</span><span class="sxs-lookup"><span data-stu-id="29075-262">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="29075-263">Maximale Puffergröße – 1200 \* 1024 Bits</span><span class="sxs-lookup"><span data-stu-id="29075-263">Maximum buffer size – 1200\*1024 bits</span></span> <br/> <span data-ttu-id="29075-264">Maximale Anzahl von Samplings pro Frame – 4096</span><span class="sxs-lookup"><span data-stu-id="29075-264">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="29075-265">Maximale Anzahl von Bits pro Frame-131072</span><span class="sxs-lookup"><span data-stu-id="29075-265">Maximum bits per frame - 131072</span></span><br/>  | <span data-ttu-id="29075-266">Empfohlen für umschließende High Definition-Filme.</span><span class="sxs-lookup"><span data-stu-id="29075-266">Recommended for surround-sound high definition movies.</span></span><br/> <span data-ttu-id="29075-267">Die maximale Rate in einem audioframe beträgt 3072000 Bit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-267">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>         |
| <span data-ttu-id="29075-268">M3</span><span class="sxs-lookup"><span data-stu-id="29075-268">M3</span></span>      | <span data-ttu-id="29075-269">Maximale Bitrate – 3 Millionen Bit/s</span><span class="sxs-lookup"><span data-stu-id="29075-269">Maximum bit rate – 3000000 bps</span></span> <br/> <span data-ttu-id="29075-270">Maximale Samplingrate – 96 kHz</span><span class="sxs-lookup"><span data-stu-id="29075-270">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="29075-271">Maximale Anzahl von Kanälen – 8</span><span class="sxs-lookup"><span data-stu-id="29075-271">Maximum channel count – 8</span></span> <br/> <span data-ttu-id="29075-272">Maximale Puffergröße – 2400 \* 1024 Bits</span><span class="sxs-lookup"><span data-stu-id="29075-272">Maximum buffer size – 2400\*1024 bits</span></span> <br/> <span data-ttu-id="29075-273">Maximale Anzahl von Samplings pro Frame – 4096</span><span class="sxs-lookup"><span data-stu-id="29075-273">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="29075-274">Maximale Anzahl von Bits pro Frame-131072</span><span class="sxs-lookup"><span data-stu-id="29075-274">Maximum bits per frame - 131072</span></span><br/> | <span data-ttu-id="29075-275">Empfohlen für digitales Theater.</span><span class="sxs-lookup"><span data-stu-id="29075-275">Recommended for digital theater.</span></span><br/> <span data-ttu-id="29075-276">Die maximale Rate in einem audioframe beträgt 3072000 Bit/s.</span><span class="sxs-lookup"><span data-stu-id="29075-276">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>                               |



 

<span data-ttu-id="29075-277">Die M0-und M1-profile passen in einen 48 kHz/16 Bit/Stereo (1536000 Bit/s) IEC 60958-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="29075-277">The M0 and M1 profiles fit into a 48 KHz/16 bit/Stereo (1536000 bps) IEC 60958 stream.</span></span> <span data-ttu-id="29075-278">Die Profile m2 und M3 passen in einen IEC 60958-Stream mit 96 kHz/16 Bit/Stereo (3072000 Bit/s) an.</span><span class="sxs-lookup"><span data-stu-id="29075-278">The M2 and M3 profiles fit into a 96 KHz/16 bit/Stereo (3072000 bps) IEC 60958 stream.</span></span>

<span data-ttu-id="29075-279">Die Werte, die von einer Anwendung in der WAVEFORMATEXTENSIBLE IEC61937-Struktur festgelegt \_ werden, um WMA Pro als ein m2-Profil darzustellen, werden im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="29075-279">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent WMA Pro as an M2 profile are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a><span data-ttu-id="29075-280">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29075-280">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29075-281">Geräte Formate</span><span class="sxs-lookup"><span data-stu-id="29075-281">Device Formats</span></span>](device-formats.md)
</dt> </dl>

 

 





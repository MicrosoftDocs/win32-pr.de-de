---
description: Der Windows Media Audio-Decoder decodiert Audiostreams, die vom Windows Media Audio Encoder codiert wurden.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Windows Media Audio Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359279"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="edd91-103">Windows Media Audio Decoder</span><span class="sxs-lookup"><span data-stu-id="edd91-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="edd91-104">Der Windows Media Audio-Decoder decodiert Audiostreams, die vom [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="edd91-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="edd91-105">Der Encoder und der Decoder unterstützen drei Kategorien codierter Audiodaten: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="edd91-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="edd91-106">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="edd91-106">Class Identifier</span></span>

<span data-ttu-id="edd91-107">Der Klassen Bezeichner (CLSID) für den Windows Media Audio Decoder wird durch die Konstante **CLSID \_ cwmadecmediaobject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="edd91-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="edd91-108">Sie können eine Instanz des Audiodecoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="edd91-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="edd91-109">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="edd91-109">Input Formats</span></span>

<span data-ttu-id="edd91-110">Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Decoder unterstützten Eingabe Kategorien darstellen.</span><span class="sxs-lookup"><span data-stu-id="edd91-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="edd91-111">Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Decoder finden Sie unter [Konfigurieren der Audiodecodierung](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="edd91-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="edd91-112">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="edd91-112">Format tag constant</span></span>             | <span data-ttu-id="edd91-113">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="edd91-113">Format tag value</span></span> | <span data-ttu-id="edd91-114">Audioformat</span><span class="sxs-lookup"><span data-stu-id="edd91-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="edd91-115">Wave- \_ Format \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="edd91-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="edd91-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="edd91-116">0x0161</span></span>           | <span data-ttu-id="edd91-117">Standard Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="edd91-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="edd91-118">Wave- \_ Format \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="edd91-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="edd91-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="edd91-119">0x0162</span></span>           | <span data-ttu-id="edd91-120">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="edd91-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="edd91-121">\_ \_ wmaudioverlust im Wave-Format \_</span><span class="sxs-lookup"><span data-stu-id="edd91-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="edd91-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="edd91-122">0x0163</span></span>           | <span data-ttu-id="edd91-123">Verlust von Windows Media Audio Verlust</span><span class="sxs-lookup"><span data-stu-id="edd91-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="edd91-124">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="edd91-124">Output Formats</span></span>

<span data-ttu-id="edd91-125">Die folgende Tabelle zeigt die audioformattags, die die vom **Windows Media Audio Decoder** unterstützten Ausgabetypen darstellen.</span><span class="sxs-lookup"><span data-stu-id="edd91-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="edd91-126">Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Decoder finden Sie unter [Konfigurieren der Audiocodierung](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="edd91-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="edd91-127">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="edd91-127">Format tag constant</span></span>       | <span data-ttu-id="edd91-128">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="edd91-128">Format tag value</span></span> | <span data-ttu-id="edd91-129">Audioformat</span><span class="sxs-lookup"><span data-stu-id="edd91-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="edd91-130">PCM im Wave- \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="edd91-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="edd91-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="edd91-131">0x0001</span></span>           | <span data-ttu-id="edd91-132">PCM-Format</span><span class="sxs-lookup"><span data-stu-id="edd91-132">PCM format</span></span>                                            |
| <span data-ttu-id="edd91-133">"Wave \_ Format \_ IEEE \_ float"</span><span class="sxs-lookup"><span data-stu-id="edd91-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="edd91-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="edd91-134">0x0003</span></span>           | <span data-ttu-id="edd91-135">IEEE-Gleit Komma</span><span class="sxs-lookup"><span data-stu-id="edd91-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="edd91-136">\_erweiterbares Wave-Format \_</span><span class="sxs-lookup"><span data-stu-id="edd91-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="edd91-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="edd91-137">0xFFFE</span></span>           | <span data-ttu-id="edd91-138">PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur</span><span class="sxs-lookup"><span data-stu-id="edd91-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="edd91-139">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="edd91-139">Interfaces</span></span>

<span data-ttu-id="edd91-140">Ein Audiodecoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="edd91-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="edd91-141">Ein Windows Media Audio Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edd91-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="edd91-142">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Audiodecoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="edd91-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="edd91-143">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="edd91-143">Operating system</span></span> | <span data-ttu-id="edd91-144">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="edd91-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd91-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="edd91-145">Windows XP</span></span>       | <span data-ttu-id="edd91-146">Ein Windows Media Audio Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="edd91-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="edd91-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edd91-147">Windows Vista</span></span>    | <span data-ttu-id="edd91-148">Standardmäßig verhält sich ein Windows Media Audio Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="edd91-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="edd91-149">Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle in einem Audiodecoder abrufen, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="edd91-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="edd91-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edd91-150">Windows 7</span></span>        | <span data-ttu-id="edd91-151">Standardmäßig verhält sich ein Windows Media Audio Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="edd91-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="edd91-152">Wenn Sie eine **imftransform** -Schnittstelle für einen Audiodecoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="edd91-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="edd91-153">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edd91-153">Properties</span></span>

<span data-ttu-id="edd91-154">Der Windows Media Audio-Decoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="edd91-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="edd91-155">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="edd91-155">Property</span></span></th>
<th><span data-ttu-id="edd91-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edd91-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edd91-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="edd91-158">Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die möglicherweise am Ende der Decodierung einer Datei zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edd91-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="edd91-159">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="edd91-160">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-161">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="edd91-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edd91-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="edd91-163">Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.</span><span class="sxs-lookup"><span data-stu-id="edd91-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="edd91-164">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-164">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-165">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-166">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edd91-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="edd91-168">Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="edd91-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="edd91-169">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-169">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-170">Professionell</span><span class="sxs-lookup"><span data-stu-id="edd91-170">Professional</span></span><br />
<span data-ttu-id="edd91-171">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edd91-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="edd91-173">Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="edd91-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="edd91-174">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-174">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-175">Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-176">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edd91-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="edd91-178">Gibt an, ob der Audiodecoder Lt-Rt-Fold ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="edd91-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="edd91-179">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="edd91-180">Professional.</span><span class="sxs-lookup"><span data-stu-id="edd91-180">Professional.</span></span><br />
<span data-ttu-id="edd91-181">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edd91-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="edd91-183">Gibt die Sprecher Konfiguration auf dem Client Computer an.</span><span class="sxs-lookup"><span data-stu-id="edd91-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="edd91-184">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-184">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-185">Professional.</span><span class="sxs-lookup"><span data-stu-id="edd91-185">Professional.</span></span><br />
<span data-ttu-id="edd91-186">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edd91-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="edd91-188">Gibt die durchschnittliche Volumeebene von Audioinhalten an.</span><span class="sxs-lookup"><span data-stu-id="edd91-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="edd91-189">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-189">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-190">Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-191">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edd91-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="edd91-193">Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.</span><span class="sxs-lookup"><span data-stu-id="edd91-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="edd91-194">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-194">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-195">Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-196">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edd91-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="edd91-198">Gibt die höchste volumenbene an, die im Audioinhalt auftritt.</span><span class="sxs-lookup"><span data-stu-id="edd91-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="edd91-199">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-199">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-200">Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-201">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edd91-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="edd91-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="edd91-203">Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.</span><span class="sxs-lookup"><span data-stu-id="edd91-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="edd91-204">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="edd91-204">Windows XP and later.</span></span><br />
<span data-ttu-id="edd91-205">Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="edd91-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="edd91-206">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="edd91-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="edd91-207">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edd91-207">Requirements</span></span>



| <span data-ttu-id="edd91-208">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edd91-208">Requirement</span></span> | <span data-ttu-id="edd91-209">Wert</span><span class="sxs-lookup"><span data-stu-id="edd91-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edd91-210">Client</span><span class="sxs-lookup"><span data-stu-id="edd91-210">Client</span></span><br/> | <span data-ttu-id="edd91-211">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="edd91-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="edd91-212">Header</span><span class="sxs-lookup"><span data-stu-id="edd91-212">Header</span></span><br/> | <dl> <span data-ttu-id="edd91-213"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd91-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="edd91-214">DLL</span><span class="sxs-lookup"><span data-stu-id="edd91-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="edd91-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd91-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="edd91-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd91-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd91-217">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="edd91-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="edd91-218">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="edd91-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 





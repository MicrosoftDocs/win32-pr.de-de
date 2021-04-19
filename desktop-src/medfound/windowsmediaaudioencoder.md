---
description: 'Der Windows Media Audio Encoder codiert Audiostreams. Der Encoder unterstützt drei Kategorien codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Windows Media Audio Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361429"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="357a7-104">Windows Media Audio Encoder</span><span class="sxs-lookup"><span data-stu-id="357a7-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="357a7-105">Der Windows Media Audio Encoder codiert Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="357a7-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="357a7-106">Der Encoder unterstützt drei Kategorien codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="357a7-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="357a7-107">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="357a7-107">Class Identifier</span></span>

<span data-ttu-id="357a7-108">Der Klassen Bezeichner (CLSID) für den Windows Media Audio Encoder wird durch die Konstante **CLSID \_ cwmaencmediaobject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="357a7-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="357a7-109">Sie können eine Instanz des Audioencoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="357a7-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="357a7-110">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="357a7-110">Input Formats</span></span>

<span data-ttu-id="357a7-111">Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Encoder unterstützten Eingabe Kategorien darstellen.</span><span class="sxs-lookup"><span data-stu-id="357a7-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="357a7-112">Weitere Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Encoder finden Sie unter [Konfigurieren der Audiocodierung](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="357a7-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="357a7-113">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="357a7-113">Format tag constant</span></span>       | <span data-ttu-id="357a7-114">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="357a7-114">Format tag value</span></span> | <span data-ttu-id="357a7-115">Audioformat</span><span class="sxs-lookup"><span data-stu-id="357a7-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="357a7-116">PCM im Wave- \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="357a7-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="357a7-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="357a7-117">0x0001</span></span>           | <span data-ttu-id="357a7-118">PCM-Format</span><span class="sxs-lookup"><span data-stu-id="357a7-118">PCM format</span></span>                                            |
| <span data-ttu-id="357a7-119">"Wave \_ Format \_ IEEE \_ float"</span><span class="sxs-lookup"><span data-stu-id="357a7-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="357a7-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="357a7-120">0x0003</span></span>           | <span data-ttu-id="357a7-121">IEEE-Gleit Komma</span><span class="sxs-lookup"><span data-stu-id="357a7-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="357a7-122">\_erweiterbares Wave-Format \_</span><span class="sxs-lookup"><span data-stu-id="357a7-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="357a7-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="357a7-123">0xFFFE</span></span>           | <span data-ttu-id="357a7-124">PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur</span><span class="sxs-lookup"><span data-stu-id="357a7-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="357a7-125">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="357a7-125">Output Formats</span></span>

<span data-ttu-id="357a7-126">Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Encoder unterstützten Ausgabe Kategorien darstellen.</span><span class="sxs-lookup"><span data-stu-id="357a7-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="357a7-127">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="357a7-127">Format tag constant</span></span>             | <span data-ttu-id="357a7-128">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="357a7-128">Format tag value</span></span> | <span data-ttu-id="357a7-129">Audioformat</span><span class="sxs-lookup"><span data-stu-id="357a7-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="357a7-130">Wave- \_ Format \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="357a7-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="357a7-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="357a7-131">0x0161</span></span>           | <span data-ttu-id="357a7-132">Standard Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="357a7-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="357a7-133">Wave- \_ Format \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="357a7-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="357a7-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="357a7-134">0x0162</span></span>           | <span data-ttu-id="357a7-135">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="357a7-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="357a7-136">\_ \_ wmaudioverlust im Wave-Format \_</span><span class="sxs-lookup"><span data-stu-id="357a7-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="357a7-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="357a7-137">0x0163</span></span>           | <span data-ttu-id="357a7-138">Verlust von Windows Media Audio Verlust</span><span class="sxs-lookup"><span data-stu-id="357a7-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="357a7-139">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="357a7-139">Interfaces</span></span>

<span data-ttu-id="357a7-140">Ein audioendoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="357a7-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="357a7-141">Ein Windows Media Audio Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="357a7-142">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Audioencoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="357a7-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="357a7-143">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="357a7-143">Operating system</span></span> | <span data-ttu-id="357a7-144">Codierungs Verhalten</span><span class="sxs-lookup"><span data-stu-id="357a7-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="357a7-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="357a7-145">Windows XP</span></span>       | <span data-ttu-id="357a7-146">Ein Windows Media Audio Encoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="357a7-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="357a7-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="357a7-147">Windows Vista</span></span>    | <span data-ttu-id="357a7-148">Standardmäßig verhält sich ein Windows Media Audio Encoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="357a7-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="357a7-149">Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle in einem Audioencoder abrufen, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="357a7-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="357a7-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="357a7-150">Windows 7</span></span>        | <span data-ttu-id="357a7-151">Standardmäßig verhält sich ein Windows Media Audio Encoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="357a7-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="357a7-152">Wenn Sie eine **imftransform** -Schnittstelle für einen Audioencoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="357a7-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="357a7-153">Codierungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="357a7-153">Encoder Properties</span></span>

<span data-ttu-id="357a7-154">Der Windows Media Audio Encoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="357a7-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="357a7-155">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="357a7-155">Property</span></span></th>
<th><span data-ttu-id="357a7-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="357a7-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="357a7-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="357a7-158">Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="357a7-159">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-160">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-161">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="357a7-163">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der Spitzen Bitrate in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="357a7-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="357a7-164">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-164">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-165">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-165">Standard, Professional.</span></span><br />
<span data-ttu-id="357a7-166">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="357a7-168">Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="357a7-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="357a7-169">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-170">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-171">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-173">Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="357a7-174">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-175">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-176">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-178">Gibt an, ob die Komplexität des Codierungs Algorithmus eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="357a7-179">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-180">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-181">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-183">Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="357a7-184">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-185">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-186">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-188">Gibt an, ob vom Encoder aufgelistete Modi auf diejenigen beschränkt sind, die eine Qualitätsanforderung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="357a7-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="357a7-189">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-190">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-191">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="357a7-193">Gibt das Komplexitäts Profil des codierten Inhalts an.</span><span class="sxs-lookup"><span data-stu-id="357a7-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="357a7-194">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-194">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-195">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-196">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-198">Gibt die gewünschte Qualitätsstufe für die VBR-Codierung an.</span><span class="sxs-lookup"><span data-stu-id="357a7-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="357a7-199">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-200">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-201">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="357a7-203">Gibt an, ob der Encoder die Rausch Ersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="357a7-204">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-205">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-206">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="357a7-208">Gibt an, ob der Encoder PCM-Bereichs Beschränkung verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="357a7-209">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-210">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-211">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="357a7-213">Gibt die maximale codierte Bandbreite an, die für die bandtrunzierung im Encoder zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="357a7-214">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-215">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-216">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="357a7-218">Gibt die minimale codierte Bandbreite an, die für die Band abkürzen im Encoder zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="357a7-219">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-220">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-221">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="357a7-223">Gibt die Qualität an, mit der die minimale codierte Bandbreite zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="357a7-224">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-225">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-226">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="357a7-228">Gibt die Qualität an, mit der die maximale codierte Bandbreite zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="357a7-229">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-230">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-231">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="357a7-233">Gibt an, ob der Encoder die bandtrunzierung ausführt.</span><span class="sxs-lookup"><span data-stu-id="357a7-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="357a7-234">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-235">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-236">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="357a7-238">Gibt an, ob der Encoder den Stil der Masken Berechnung verwendet, der von Version 7 des Windows Media Audio Encoders ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="357a7-239">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-240">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-241">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="357a7-243">Gibt an, ob der Encoder die Stereobild Verarbeitung ausführt.</span><span class="sxs-lookup"><span data-stu-id="357a7-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="357a7-244">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-245">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-246">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="357a7-248">Gibt das Puffer Fenster (in Millisekunden) für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="357a7-249">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-250">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-251">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="357a7-253">Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="357a7-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="357a7-254">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-255">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-256">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-258">Gibt die Komplexität des Codierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="357a7-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="357a7-259">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-260">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-261">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="357a7-263">Gibt das Ende eines Codierungs Durchlaufs an.</span><span class="sxs-lookup"><span data-stu-id="357a7-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="357a7-264">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-264">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-265">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-265">Standard, Professional.</span></span><br />
<span data-ttu-id="357a7-266">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="357a7-268">Gibt an, ob der kerncodierer das &quot; Plus- &quot; Feature verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="357a7-269">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-270">Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-270">Professional.</span></span><br />
<span data-ttu-id="357a7-271">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="357a7-273">Gibt die maximale Latenzzeit für den Decoder in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="357a7-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="357a7-274">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-275">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-276">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="357a7-278">Gibt die maximale Latenzzeit für den Encoder in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="357a7-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="357a7-279">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-280">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-281">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="357a7-283">Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an.</span><span class="sxs-lookup"><span data-stu-id="357a7-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="357a7-284">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-285">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-286">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="357a7-288">Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an.</span><span class="sxs-lookup"><span data-stu-id="357a7-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="357a7-289">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-289">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-290">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-291">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="357a7-293">Gibt die Anzahl von Durchläufen an, die der Encoder zum Codieren des Inhalts verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="357a7-294">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-294">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-295">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-296">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="357a7-298">Gibt an, ob der Encoder durch eine Spitzen Bitrate eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="357a7-299">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-300">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-300">Standard, Professional.</span></span><br />
<span data-ttu-id="357a7-301">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="357a7-303">Gibt die bevorzugte Anzahl von Stichproben pro Frame an.</span><span class="sxs-lookup"><span data-stu-id="357a7-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="357a7-304">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-305">Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-305">Professional.</span></span><br />
<span data-ttu-id="357a7-306">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="357a7-308">Gibt an, ob der Encoder eine bevorzugte Frame Größe verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="357a7-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="357a7-309">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-310">Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-310">Professional.</span></span><br />
<span data-ttu-id="357a7-311">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="357a7-313">Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="357a7-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="357a7-314">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-314">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-315">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-315">Standard, Professional.</span></span><br />
<span data-ttu-id="357a7-316">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="357a7-318">Gibt das durchschnittliche Puffer Fenster (in Millisekunden) eines codierten Streams an.</span><span class="sxs-lookup"><span data-stu-id="357a7-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="357a7-319">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-319">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-320">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-321">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="357a7-323">Gibt das maximale Puffer Fenster (in Millisekunden) eines codierten Streams an.</span><span class="sxs-lookup"><span data-stu-id="357a7-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="357a7-324">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-324">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-325">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-326">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="357a7-328">Gibt die durchschnittliche Bitrate eines codierten Streams in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="357a7-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="357a7-329">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-329">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-330">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-331">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="357a7-333">Gibt die maximale Bitrate eines codierten Streams in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="357a7-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="357a7-334">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-334">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-335">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-336">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="357a7-338">Gibt an, ob der Encoder die VBR-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="357a7-339">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-339">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-340">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-341">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="357a7-343">Diese Eigenschaft wird derzeit nicht vom Windows Media Audio Codec verwendet.</span><span class="sxs-lookup"><span data-stu-id="357a7-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="357a7-345">Gibt die durchschnittliche Volumeebene von Audioinhalten an.</span><span class="sxs-lookup"><span data-stu-id="357a7-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="357a7-346">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-346">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-347">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-348">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="357a7-350">Gibt die höchste volumenbene an, die im Audioinhalt auftritt.</span><span class="sxs-lookup"><span data-stu-id="357a7-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="357a7-351">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-351">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-352">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-353">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="357a7-355">Gibt die durchschnittlichen Bytes pro Sekunde für VBR-codierte Audiodaten an.</span><span class="sxs-lookup"><span data-stu-id="357a7-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="357a7-356">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-356">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-357">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-358">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="357a7-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="357a7-360">Gibt an, ob der Encoder 1 WMA-Paket pro Frame liefern soll.</span><span class="sxs-lookup"><span data-stu-id="357a7-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="357a7-361">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-362">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-363">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="357a7-365">Gibt an, ob der Encoder dynamische Bereichs Steuerungsparameter generieren soll.</span><span class="sxs-lookup"><span data-stu-id="357a7-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="357a7-366">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-367">Standard, Professional, verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="357a7-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="357a7-368">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="357a7-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="357a7-370">Gibt die <strong>WaveFormatEx</strong> -Struktur an, die den audioinhaltstyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="357a7-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="357a7-371">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-371">Windows XP and later.</span></span><br />
<span data-ttu-id="357a7-372">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-372">Standard, Professional.</span></span><br />
<span data-ttu-id="357a7-373">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="357a7-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="357a7-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="357a7-375">Gibt an, ob der Encoder die S/PDIF-Echtzeitcodierung aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="357a7-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="357a7-376">Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="357a7-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="357a7-377">Professional.</span><span class="sxs-lookup"><span data-stu-id="357a7-377">Professional.</span></span><br />
<span data-ttu-id="357a7-378">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="357a7-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="357a7-379">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="357a7-379">Requirements</span></span>



| <span data-ttu-id="357a7-380">Anforderung</span><span class="sxs-lookup"><span data-stu-id="357a7-380">Requirement</span></span> | <span data-ttu-id="357a7-381">Wert</span><span class="sxs-lookup"><span data-stu-id="357a7-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="357a7-382">Client</span><span class="sxs-lookup"><span data-stu-id="357a7-382">Client</span></span><br/> | <span data-ttu-id="357a7-383">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="357a7-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="357a7-384">Header</span><span class="sxs-lookup"><span data-stu-id="357a7-384">Header</span></span><br/> | <dl> <span data-ttu-id="357a7-385"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="357a7-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="357a7-386">DLL</span><span class="sxs-lookup"><span data-stu-id="357a7-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="357a7-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="357a7-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="357a7-388">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="357a7-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357a7-389">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="357a7-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="357a7-390">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="357a7-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 





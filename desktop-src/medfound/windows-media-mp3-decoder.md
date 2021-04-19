---
description: Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Media MP3-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366877"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="b41e6-103">Windows Media MP3-Decoder</span><span class="sxs-lookup"><span data-stu-id="b41e6-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="b41e6-104">Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b41e6-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="b41e6-105">ISO/IEC 11172-3 (MPEG-1-Audiodatei) Ebene 3</span><span class="sxs-lookup"><span data-stu-id="b41e6-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="b41e6-106">ISO/IEC 13818-3 (MPEG-2-Audiodatei) Layer 3, niedrige Stichproben Häufigkeits Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b41e6-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b41e6-107">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b41e6-107">Class Identifier</span></span>

<span data-ttu-id="b41e6-108">Der Klassen Bezeichner (CLSID) für den Windows Media MP3-Decoder wird durch die Konstante **CLSID \_ CMP3DecMediaObject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b41e6-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="b41e6-109">Sie können eine Instanz des MP3-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41e6-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="b41e6-110">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b41e6-110">Interfaces</span></span>

<span data-ttu-id="b41e6-111">Ein MP3-Decoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b41e6-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="b41e6-112">Ein Windows Media MP3-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b41e6-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="b41e6-113">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Windows Media MP3-Decoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="b41e6-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="b41e6-114">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b41e6-114">Operating system</span></span> | <span data-ttu-id="b41e6-115">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="b41e6-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b41e6-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b41e6-116">Windows XP</span></span>       | <span data-ttu-id="b41e6-117">Ein Windows Media MP3-Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="b41e6-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="b41e6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b41e6-118">Windows Vista</span></span>    | <span data-ttu-id="b41e6-119">Standardmäßig verhält sich ein Windows Media MP3-Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="b41e6-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="b41e6-120">Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle auf einem Windows Media MP3-Decoder abrufen, verhält sie sich als MFT.</span><span class="sxs-lookup"><span data-stu-id="b41e6-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="b41e6-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b41e6-121">Windows 7</span></span>        | <span data-ttu-id="b41e6-122">Standardmäßig verhält sich ein Windows Media MP3-Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="b41e6-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="b41e6-123">Wenn Sie eine **imftransform** -Schnittstelle für einen Windows Media MP3-Decoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="b41e6-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="b41e6-124">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="b41e6-124">Input Formats</span></span>

<span data-ttu-id="b41e6-125">In der folgenden Tabelle wird das audioformattag angezeigt, das den vom Windows Media MP3-Decoder unterstützten Eingabetyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="b41e6-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="b41e6-126">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="b41e6-126">Format tag constant</span></span>      | <span data-ttu-id="b41e6-127">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="b41e6-127">Format tag value</span></span> | <span data-ttu-id="b41e6-128">Audioformat</span><span class="sxs-lookup"><span data-stu-id="b41e6-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="b41e6-129">Wave- \_ Format \_ MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="b41e6-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="b41e6-130">0x55</span><span class="sxs-lookup"><span data-stu-id="b41e6-130">0x55</span></span>             | <span data-ttu-id="b41e6-131">ISO MPEG Layer 3</span><span class="sxs-lookup"><span data-stu-id="b41e6-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="b41e6-132">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="b41e6-132">Output Formats</span></span>

<span data-ttu-id="b41e6-133">Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media MP3-Decoder unterstützten Ausgabetypen darstellen.</span><span class="sxs-lookup"><span data-stu-id="b41e6-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="b41e6-134">Tagkonstante formatieren</span><span class="sxs-lookup"><span data-stu-id="b41e6-134">Format tag constant</span></span>       | <span data-ttu-id="b41e6-135">Tagwert formatieren</span><span class="sxs-lookup"><span data-stu-id="b41e6-135">Format tag value</span></span> | <span data-ttu-id="b41e6-136">Audioformat</span><span class="sxs-lookup"><span data-stu-id="b41e6-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b41e6-137">PCM im Wave- \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="b41e6-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="b41e6-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="b41e6-138">0x0001</span></span>           | <span data-ttu-id="b41e6-139">PCM-Format (bei Verwendung als DMO oder MFT)</span><span class="sxs-lookup"><span data-stu-id="b41e6-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="b41e6-140">"Wave \_ Format \_ IEEE \_ float"</span><span class="sxs-lookup"><span data-stu-id="b41e6-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="b41e6-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="b41e6-141">0x0003</span></span>           | <span data-ttu-id="b41e6-142">IEEE-Gleit Komma (bei Verwendung als MFT)</span><span class="sxs-lookup"><span data-stu-id="b41e6-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="b41e6-143">\_erweiterbares Wave-Format \_</span><span class="sxs-lookup"><span data-stu-id="b41e6-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="b41e6-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="b41e6-144">0xFFFE</span></span>           | <span data-ttu-id="b41e6-145">PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur (bei Verwendung als MFT)</span><span class="sxs-lookup"><span data-stu-id="b41e6-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="b41e6-146">Der Windows Media MP3-Decoder unterstützt und listet die folgenden Ausgabemedien Typen auf.</span><span class="sxs-lookup"><span data-stu-id="b41e6-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="b41e6-147">Ein Ausgabetyp, der dieselbe Samplingrate und Anzahl von Kanälen wie der Eingabetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="b41e6-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="b41e6-148">Mono-Ausgabe für Stereo Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b41e6-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="b41e6-149">Ausgabetypen mit Bits-Tiefe von 8 und 16.</span><span class="sxs-lookup"><span data-stu-id="b41e6-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="b41e6-150">Gleit Komma Ausgabe, wenn der Decoder sich als MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="b41e6-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="b41e6-151">Der Windows Media MP3-Decoder unterstützt die folgenden Ausgabemedien Typen, aber listet sie nicht auf.</span><span class="sxs-lookup"><span data-stu-id="b41e6-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="b41e6-152">Ein Ausgabetyp mit der Hälfte der Samplingrate für den Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="b41e6-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="b41e6-153">Ein Ausgabetyp, der eine vierte Samplingrate für den Eingabetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="b41e6-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b41e6-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b41e6-154">Requirements</span></span>



| <span data-ttu-id="b41e6-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b41e6-155">Requirement</span></span> | <span data-ttu-id="b41e6-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b41e6-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b41e6-157">Client</span><span class="sxs-lookup"><span data-stu-id="b41e6-157">Client</span></span><br/> | <span data-ttu-id="b41e6-158">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="b41e6-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="b41e6-159">Header</span><span class="sxs-lookup"><span data-stu-id="b41e6-159">Header</span></span><br/> | <dl> <span data-ttu-id="b41e6-160"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41e6-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b41e6-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b41e6-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="b41e6-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b41e6-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b41e6-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b41e6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41e6-164">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="b41e6-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="b41e6-165">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="b41e6-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 





---
description: Der Microsoft MPEG-Audiodecoder ist eine synchrone Media Foundation Transformation (MFT), die das Decodieren von MPEG-audioelementaren streamformaten mithilfe der Media Foundation (MF)-Pipeline ermöglicht.
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: MPEG-Audiodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959235"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="b57df-103">MPEG-Audiodecoder</span><span class="sxs-lookup"><span data-stu-id="b57df-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="b57df-104">Der Microsoft MPEG-Audiodecoder ist eine synchrone [Media Foundation Transformation](media-foundation-transforms.md) (MFT), die das Decodieren von MPEG-audioelementaren streamformaten mithilfe der Media Foundation (MF)-Pipeline ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b57df-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="b57df-105">Der Decoder unterstützt die folgenden MPEG-Datenstrom Formate.</span><span class="sxs-lookup"><span data-stu-id="b57df-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="b57df-106">MPEG-1-Audioebenen I und II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="b57df-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="b57df-107">2.</span><span class="sxs-lookup"><span data-stu-id="b57df-107">2.</span></span> <span data-ttu-id="b57df-108">MPEG-2 rückwärtskompatibel, Ebenen I und II (ISO</span><span class="sxs-lookup"><span data-stu-id="b57df-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="b57df-109">MPEG-2 rückwärtskompatibel, Ebenen I und II (ISO/IEC 13818-3), Mono und Stereo</span><span class="sxs-lookup"><span data-stu-id="b57df-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b57df-110">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b57df-110">Class Identifier</span></span>

<span data-ttu-id="b57df-111">Der Klassen Bezeichner (CLSID) des MPEG-Audiodecoders ist **CLSID \_ msmpeer gauddecmft**, der in der Header Datei wmcodecdsp. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b57df-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="b57df-112">Eingabemedien Typen</span><span class="sxs-lookup"><span data-stu-id="b57df-112">Input Media Types</span></span>

<span data-ttu-id="b57df-113">Der MPEG-Audiodecoder unterstützt die folgenden Attribute für den Eingabe Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b57df-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="b57df-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="b57df-114">Attribute</span></span>                                                                               | <span data-ttu-id="b57df-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b57df-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57df-116">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b57df-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="b57df-117">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="b57df-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="b57df-118">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="b57df-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="b57df-119">**MF Audioformat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="b57df-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b57df-120">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="b57df-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="b57df-121">Optionale Normalerweise 1 für Mono oder 2 für Stereo, kann jedoch bis zu sechs Kanäle sein.</span><span class="sxs-lookup"><span data-stu-id="b57df-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="b57df-122">**MF \_ \_ -MT \_ - \_ audiokanalmaske**</span><span class="sxs-lookup"><span data-stu-id="b57df-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="b57df-123">Optionale Normalerweise 0x4 für Mono oder 0x3 für Stereo, kann aber auch eine der Kanalmasken sein, die bis zu 6 Kanälen zugeordnet sind (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="b57df-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="b57df-124">Wenn die Kanalmaske vorhanden ist, muss Sie mit der angegebenen Eingabe Anzahl von Kanälen konsistent sein.</span><span class="sxs-lookup"><span data-stu-id="b57df-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="b57df-125">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="b57df-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="b57df-126">Optionale Eines der folgenden: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="b57df-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="b57df-127">Wenn angegeben, muss die Eingabe Stichproben Rate eine der gültigen MPEG-Stichproben Raten sein.</span><span class="sxs-lookup"><span data-stu-id="b57df-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="b57df-128">Ausgabemedien Typen</span><span class="sxs-lookup"><span data-stu-id="b57df-128">Output Media Types</span></span>

<span data-ttu-id="b57df-129">Der MPEG-Audiodecoder unterstützt bis zu vier Ausgabemedien-Untertypen in der folgenden Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b57df-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="b57df-130">Stereo, Gleit Komma.</span><span class="sxs-lookup"><span data-stu-id="b57df-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="b57df-131">Stereo-und 16-Bit-PCM.</span><span class="sxs-lookup"><span data-stu-id="b57df-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="b57df-132">Mono, Gleit Komma Zahl (nur, wenn die Eingabe Mono oder Dual-Mono ist).</span><span class="sxs-lookup"><span data-stu-id="b57df-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="b57df-133">Mono, 16-Bit-PCM (nur, wenn die Eingabe Mono oder Dual-Mono ist).</span><span class="sxs-lookup"><span data-stu-id="b57df-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="b57df-134">Der Decoder unterstützt immer die Stereoausgabe und wird als erster Ausgabe Medientyp aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b57df-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="b57df-135">Der Decoder unterstützt die folgenden Attribute des Ausgabemedien Typs.</span><span class="sxs-lookup"><span data-stu-id="b57df-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="b57df-136">Attribut</span><span class="sxs-lookup"><span data-stu-id="b57df-136">Attribute</span></span>                                                                           | <span data-ttu-id="b57df-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b57df-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="b57df-138">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57df-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="b57df-139">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="b57df-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="b57df-140">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="b57df-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="b57df-141">**MF Audioformat \_ PCM** oder **MF Audioformat \_ float**</span><span class="sxs-lookup"><span data-stu-id="b57df-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="b57df-142">MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel</span><span class="sxs-lookup"><span data-stu-id="b57df-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="b57df-143">16 oder 32</span><span class="sxs-lookup"><span data-stu-id="b57df-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="b57df-144">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="b57df-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="b57df-145">1 oder 2</span><span class="sxs-lookup"><span data-stu-id="b57df-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="b57df-146">MF \_ \_ -MT \_ - \_ audiokanalmaske</span><span class="sxs-lookup"><span data-stu-id="b57df-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="b57df-147">0x4 für Mono oder 0x3 für Stereo</span><span class="sxs-lookup"><span data-stu-id="b57df-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="b57df-148">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="b57df-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="b57df-149">Eines der folgenden: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="b57df-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="b57df-150">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="b57df-150">Transform Attributes</span></span>

<span data-ttu-id="b57df-151">Der MPEG-Audiodecoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b57df-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="b57df-152">Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b57df-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="b57df-153">Attribut</span><span class="sxs-lookup"><span data-stu-id="b57df-153">Attribute</span></span>                                                                               | <span data-ttu-id="b57df-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b57df-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57df-155">**Codecapi \_ avdecaudiodualmono**</span><span class="sxs-lookup"><span data-stu-id="b57df-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="b57df-156">Gibt an, ob die decodierte 2-Kanal-Audiodatei Dual Mono ist.</span><span class="sxs-lookup"><span data-stu-id="b57df-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="b57df-157">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b57df-157">Read-only.</span></span> <span data-ttu-id="b57df-158">Wird von der MFT festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b57df-158">Set by the MFT.</span></span> <span data-ttu-id="b57df-159">Weitere Informationen finden Sie unter [**eavdecaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="b57df-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="b57df-160">**Codecapi \_ avdecaudiodualmonorepromode**</span><span class="sxs-lookup"><span data-stu-id="b57df-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="b57df-161">Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="b57df-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="b57df-162">Der Standardwert ist **eavdecaudiodualmonorepromode \_ left \_ Mono**.</span><span class="sxs-lookup"><span data-stu-id="b57df-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="b57df-163">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b57df-163">Read/Write.</span></span> <span data-ttu-id="b57df-164">Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b57df-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="b57df-165">Weitere Informationen finden Sie unter [**eavdecaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="b57df-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="b57df-166">**Codecapi \_ avenccommonmeanbitrate**</span><span class="sxs-lookup"><span data-stu-id="b57df-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="b57df-167">Gibt die komprimierte streambitrate an.</span><span class="sxs-lookup"><span data-stu-id="b57df-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="b57df-168">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b57df-168">Read-only.</span></span> <span data-ttu-id="b57df-169">Wird von der MFT festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b57df-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="b57df-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b57df-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57df-171">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="b57df-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 

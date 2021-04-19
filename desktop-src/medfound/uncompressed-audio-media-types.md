---
description: Nicht komprimierte audiomedientypen
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: Nicht komprimierte audiomedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371824"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="924dc-103">Nicht komprimierte audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="924dc-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="924dc-104">Legen Sie zum Erstellen eines kompletten nicht komprimierten audiotyps mindestens die folgenden Attribute für den [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="924dc-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="924dc-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="924dc-105">Attribute</span></span>                                                                                    | <span data-ttu-id="924dc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="924dc-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="924dc-107">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="924dc-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="924dc-108">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="924dc-108">Major type.</span></span> <span data-ttu-id="924dc-109">Legen Sie auf mfmediatype \_ -Audiodaten fest.</span><span class="sxs-lookup"><span data-stu-id="924dc-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="924dc-110">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="924dc-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="924dc-111">Untertyp.</span><span class="sxs-lookup"><span data-stu-id="924dc-111">Subtype.</span></span> <span data-ttu-id="924dc-112">Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="924dc-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="924dc-113">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="924dc-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="924dc-114">Anzahl der Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="924dc-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="924dc-115">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="924dc-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="924dc-116">Anzahl von Audiobeispielen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="924dc-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="924dc-117">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="924dc-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="924dc-118">Block Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="924dc-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="924dc-119">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="924dc-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="924dc-120">Die durchschnittliche Anzahl von Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="924dc-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="924dc-121">**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="924dc-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="924dc-122">Anzahl von Bits pro audiostich Probe.</span><span class="sxs-lookup"><span data-stu-id="924dc-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="924dc-123">**\_ \_ alle \_ Beispiele \_ unabhängig von MF**</span><span class="sxs-lookup"><span data-stu-id="924dc-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="924dc-124">Gibt an, ob jedes Audiosample unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="924dc-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="924dc-125">Legen Sie diese Einstellung auf **true** fest, wenn mfaudioformat \_ PCM und mfaudioformat \_ float-Formate aufweisen.</span><span class="sxs-lookup"><span data-stu-id="924dc-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="924dc-126">Außerdem sind die folgenden Attribute für einige Audioformate erforderlich.</span><span class="sxs-lookup"><span data-stu-id="924dc-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="924dc-127">Attribut</span><span class="sxs-lookup"><span data-stu-id="924dc-127">Attribute</span></span>                                                                                      | <span data-ttu-id="924dc-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="924dc-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="924dc-129">**zulässige \_ \_ \_ \_ Bits \_ pro \_ Beispiel für MF-MT-Audiodaten**</span><span class="sxs-lookup"><span data-stu-id="924dc-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="924dc-130">Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="924dc-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="924dc-131">Legen Sie dieses Attribut fest, wenn die Audiobeispiele Auffüll Zeichen aufweisen, d. –., wenn die Anzahl der gültigen Bits in den einzelnen Audiobeispielen kleiner ist als die Stichprobengröße.</span><span class="sxs-lookup"><span data-stu-id="924dc-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="924dc-132">**MF \_ \_ -MT \_ - \_ audiokanalmaske**</span><span class="sxs-lookup"><span data-stu-id="924dc-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="924dc-133">Die Zuweisung von Audiokanälen zu Sprecherpositionen.</span><span class="sxs-lookup"><span data-stu-id="924dc-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="924dc-134">Legen Sie dieses Attribut für Multichannel-Audiostreams fest, z. b. 5,1.</span><span class="sxs-lookup"><span data-stu-id="924dc-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="924dc-135">Dieses Attribut ist für Mono-oder Stereo-Audiodaten nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="924dc-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="924dc-136">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="924dc-136">Example Code</span></span>

<span data-ttu-id="924dc-137">Der folgende Code zeigt, wie Sie einen Medientyp für unkomprimiertes PCM-Audiodaten erstellen.</span><span class="sxs-lookup"><span data-stu-id="924dc-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="924dc-138">Im nächsten Beispiel wird ein codiertes Audioformat als Eingabe angenommen, und ein passender PCM-Audiotyp wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="924dc-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="924dc-139">Dieser Typ kann beispielsweise für einen Encoder oder Decoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="924dc-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="924dc-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="924dc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924dc-141">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="924dc-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 




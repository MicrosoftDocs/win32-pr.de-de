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
# <a name="uncompressed-audio-media-types"></a>Nicht komprimierte audiomedientypen

Legen Sie zum Erstellen eines kompletten nicht komprimierten audiotyps mindestens die folgenden Attribute für den [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger fest.



| Attribut                                                                                    | BESCHREIBUNG                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                                    | Der Haupttyp. Legen Sie auf mfmediatype \_ -Audiodaten fest.                                                                                       |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                           | Untertyp. Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).                                                                 |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                   | Anzahl der Audiokanäle.                                                                                                    |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)      | Anzahl von Audiobeispielen pro Sekunde.                                                                                          |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)             | Block Ausrichtung.                                                                                                             |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Die durchschnittliche Anzahl von Bytes pro Sekunde.                                                                                          |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)            | Anzahl von Bits pro audiostich Probe.                                                                                             |
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md)         | Gibt an, ob jedes Audiosample unabhängig ist. Legen Sie diese Einstellung auf **true** fest, wenn mfaudioformat \_ PCM und mfaudioformat \_ float-Formate aufweisen. |



 

Außerdem sind die folgenden Attribute für einige Audioformate erforderlich.



| Attribut                                                                                      | BESCHREIBUNG                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**zulässige \_ \_ \_ \_ Bits \_ pro \_ Beispiel für MF-MT-Audiodaten**](mf-mt-audio-valid-bits-per-sample-attribute.md) | Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel. Legen Sie dieses Attribut fest, wenn die Audiobeispiele Auffüll Zeichen aufweisen, d. –., wenn die Anzahl der gültigen Bits in den einzelnen Audiobeispielen kleiner ist als die Stichprobengröße. |
| [**MF \_ \_ -MT \_ - \_ audiokanalmaske**](mf-mt-audio-channel-mask-attribute.md)                     | Die Zuweisung von Audiokanälen zu Sprecherpositionen. Legen Sie dieses Attribut für Multichannel-Audiostreams fest, z. b. 5,1. Dieses Attribut ist für Mono-oder Stereo-Audiodaten nicht erforderlich.                       |



 

### <a name="example-code"></a>Beispielcode

Der folgende Code zeigt, wie Sie einen Medientyp für unkomprimiertes PCM-Audiodaten erstellen.


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



Im nächsten Beispiel wird ein codiertes Audioformat als Eingabe angenommen, und ein passender PCM-Audiotyp wird erstellt. Dieser Typ kann beispielsweise für einen Encoder oder Decoder festgelegt werden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> </dl>

 

 




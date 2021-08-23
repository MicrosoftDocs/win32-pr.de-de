---
description: Der Microsoft MPEG-Audiodecoder ist ein synchrones Media Foundation Transform (MFT), das das Decodieren elementarer MPEG-Audiostreamformate mithilfe der pipeline Media Foundation (MF) ermöglicht.
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: MPEG-Audiodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb908509f9c9f1c55ef7434b33d3265be875bf56443bc69c5a4cf829774bded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722280"
---
# <a name="mpeg-audio-decoder"></a>MPEG-Audiodecoder

Der Microsoft MPEG-Audiodecoder ist ein synchrones [Media Foundation Transform (MFT),](media-foundation-transforms.md) das das Decodieren elementarer MPEG-Audiostreamformate mithilfe der pipeline Media Foundation (MF) ermöglicht.

Der Decoder unterstützt die folgenden elementaren MPEG-Streamformate.

-   MPEG-1-Audioebenen I und II (ISO/IEC 11172-3). 2. MPEG-2 abwärtskompatibel, Schichten I und II (ISO)

-   MPEG-2 abwärtskompatibel, Schichten I und II (ISO/IEC 13818-3), nur Mono und Stereo

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) des MPEG-Audiodecoders ist **CLSID \_ MSMPEGAudDecMFT,** definiert in der Headerdatei wmcodecdsp.h.

## <a name="input-media-types"></a>Eingabemedientypen

Der MPEG Audio-Decoder unterstützt die folgenden Eingabemedientypattribute.



| attribute                                                                               | Wert                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                                                                                                                                                                                                                |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)              | (Optional) Normalerweise 1 für Mono oder 2 für Stereo, kann aber bis zu 6 Kanäle sein.<br/>                                                                                                                                                                                |
| [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)              | (Optional) In der Regel 0x4 für Mono oder 0x3 für Stereo, kann aber auch eine der Kanalmasken sein, die bis zu 6 Kanälen zugeordnet sind (1.3., 2.03., 1.3., 2.2., 2.1. Falls vorhanden, muss die Kanalmaske mit der angegebenen Eingabeanzahl von Kanälen konsistent sein.<br/> |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md) | (Optional) Einer der folgenden: 16000, 22050, 24000, 32000, 44100, 48000. Falls angegeben, muss die Eingabesamplingrate eine der gültigen MPEG-Samplingraten sein.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Ausgabemedientypen

Der MPEG-Audiodecoder unterstützt bis zu vier Ausgabemedienuntertypen in der folgenden Reihenfolge.

<dl> 1. Stereo, Gleitkomma.  
2. Stereo, 16-Bit-PCM.  
3. Mono, Gleitkomma (nur, wenn die Eingabe mono oder dual-mono ist).  
4. Mono, 16-Bit-PCM (nur, wenn die Eingabe mono oder dual-mono ist).  
</dl>

Der Decoder unterstützt immer die Stereoausgabe und wird als erster Ausgabemedientyp aufzählt.

Der Decoder unterstützt die folgenden Ausgabemedientypattribute.



| attribute                                                                           | Wert                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                     |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                      | Entweder **MFAudioFormat \_ PCM** oder **MFAudioFormat \_ Float**                  |
| [MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL](mf-mt-audio-bits-per-sample-attribute.md)       | 16 oder 32                                                                   |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)              | 1 oder 2                                                                     |
| [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)              | 0x4 für Mono oder 0x3 für Stereo                                             |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md) | Einer der folgenden: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Transformieren von Attributen

Der MPEG Audio-Decoder implementiert die [**DECODERTransform::GetAttributes-Methode.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Anwendungen können diese Methode verwenden, um die folgenden Attribute abzurufen oder festzulegen.



| attribute                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Gibt an, ob 2-Kanal-Audio, das decodiert wird, dual mono ist oder nicht. Schreibgeschützt. Wird vom MFT festgelegt. Weitere Informationen finden Sie unter [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert. Der Standardwert ist **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**.<br/> Lesen/Schreiben Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern. Weitere Informationen finden Sie unter [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Gibt die komprimierte Streambitrate an. Schreibgeschützt. Wird vom MFT festgelegt.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 

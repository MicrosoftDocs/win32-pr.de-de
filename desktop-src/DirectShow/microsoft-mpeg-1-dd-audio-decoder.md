---
description: 'Dieser Filter decodiert die folgenden Audioformate:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Microsoft MPEG-1/DD/AAC-Audiodecoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd20bfc2ad8a366b46ac0c0600d8cc7a8bca5abacae621e8ea7d02f5f1cb4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051250"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Microsoft MPEG-1/DD/AAC-Audiodecoder

Dieser Filter decodiert die folgenden Audioformate:

-   MPEG-1-Audioebenen I und II.
-   Abwärtskompatible MPEG-2-Audio, Ebenen I und II (ISO/IEC 13818-3), nur Mono und Stereo.
-   Advanced Audio Coding (AAC) Low Complexity (LC)-Profil.
-   High-Efficiency AAC (HE-AAC) Version 1 und Version 2.
-   Digitale Pass-Through-Systeme (DTS) für die digitale Ausgabe.
-   LPCM, nur Mono und Stereo, mit oder ohne PES-Header.
-   Dolby Digital.
-   Dolby Digital Plus, einschließlich Konvertierung von Dolby Digital Plus in Dolby Digital für die digitale Ausgabe.

> [!Note]  
> Die Microsoft-Implementierung der Dolby Digital-Technologie ist im Rahmen des Dolby Digital-Lizenzierungsprogramms auf die Verwendung durch Microsoft-Anwendungen beschränkt.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 

Die Decodierung der Formate Dolby Digital Plus, AAC und HE-AAC erfordert Windows 7. Die Decodierung von Dolby Digital oder Dolby Digital Plus wird auf Windows 7 Home Basic oder Windows 7 Starter nicht unterstützt.

In der Registrierung lautet der Anzeigename dieses Filters "Microsoft DTV-DVD Audio Decoder".



Filterinformationen

Filterschnittstellen

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Eingabepinmedientypen

In Windows Vista und höher unterstützt der Filter die folgenden Eingabetypen:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3** (siehe Hinweis 1.)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1Payload**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (siehe Hinweis 1.)
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DTS** (siehe Hinweis 2.)
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (siehe Hinweis 1.)
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (siehe Hinweis 2.)
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ DOLBY \_ AC3** (siehe Hinweis 1.)
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**

Ab Windows 7 unterstützt der Filter auch die folgenden Eingabetypen:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (siehe Hinweis 1.)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DTS2** (siehe Hinweis 2.)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DVM** (siehe Hinweis 1.)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG \_ LOAS**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (siehe Hinweis 1.)
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG \_ LOAS**

Der Eingabetyp kann sich während des Streamings dynamisch ändern.<br/> Weitere Informationen zu diesen Medientypen finden Sie unter [**Audiountertypen.**](audio-subtypes.md)<br/>

> [!Note]  
> 1. Die Microsoft-Implementierung der Dolby Digital-Technologie ist im Rahmen des Dolby Digital-Lizenzierungsprogramms auf die Verwendung durch Microsoft-Anwendungen beschränkt.

<br/>

> [!Note]  
> 2. Für DTS-Eingaben (Digital Systemen) wird nur die S/PDIF-Ausgabe unterstützt (DTS über S/PDIF). Die Audiodecodierung wird nicht unterstützt.

<br/>

Eingabe-Pin-Schnittstellen

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Medientypen des Ausgabepins

In Windows Vista und höher unterstützt der Filter die folgenden Ausgabetypen:<br/>

-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3 \_ SOLLIF** (identisch mit **KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DOLBY \_ DIGITAL**)
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ PCM**

Ab Windows 7 unterstützt der Filter auch die folgenden Ausgabetypen:<br/>

-   **MEDIATYPE \_ Audio,** **KSDATAFORMAT-UNTERTYP \_ \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ IEEE \_ FLOAT**

Ausgabe-Pin-Schnittstellen

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtern von CLSID

**CLSID \_ CMPEG2AudDecoderDS** (deklariert in wmcodecdsp.h)

Ausführbare Datei

msmpeg2adec.dll

[Verdienst](merit.md)

**VERERZUNG \_ NORMAL** – 1

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> In einer früheren Version der Dokumentation wurde angegeben, dass dieser Filter "MPEG-2-Audio" decodieren kann. Der Filter decodiert nur abwärtskompatible MPEG-2-Audiodaten.

 

## <a name="remarks"></a>Hinweise

Mono-Streams werden immer in Stereo decodiert.

Für Streams mit einer Kanalkonfiguration von mindestens zwei Lautsprechern führt der Decoder einen der folgenden Schritte aus:

-   Kombiniert bis zu sechs Kanäle mithilfe der allgemeinen 5.1-Sprecherkonfiguration.
-   Downmixes zu Stereo.

Um zwischen diesen beiden Optionen auszuwählen, verwenden Sie die [**ICodecAPI-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) um die [**AVDecCommonOutputFormat-Eigenschaft**](avdeccommonoutputformat-property.md) festzulegen, bevor Sie die Pins verbinden. Wenn die Anwendung das Filterdiagramm erstellt, kann sie alternativ den gewünschten Medientyp auf dem Ausgabepin festlegen.

### <a name="aac-decoding"></a>AAC-Decodierung

Für AAC weist der Decoder bestimmte Formateinschränkungen für die komprimierte AAC-Eingabe auf. Diese Formateinschränkungen entsprechen dem Media Foundation [**AAC-Decoder**](../medfound/aac-decoder.md)und sind im Abschnitt [**Formateinschränkungen**](../medfound/aac-decoder.md)dokumentiert.

Der DirectShow-Decoder akzeptiert auch andere Eingabetypen als der Media Foundation Decoder. Der DirectShow-Decoder unterstützt die folgenden AAC-Eingabetypen:

-   **MEDIASUBTYPE \_ RAW \_ AAC1:** Unformatierte AAC, in der Regel in AVI oder Matroska (. MKV)-Dateien.
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC:** AAC in einem Audiodatentransportstream (ADTS) für das Streaming.
-   **MEDIASUBTYPE \_ MPEG \_ LOAS:** Transportstream mit einer Synchronisierungsebene (LOAS) und einer Multiplexebene (LATM).

Der Media Foundation-Decoder unterstützt die folgenden AAC-Eingabetypen:

-   MFAudioFormat \_ AAC (identisch mit **MEDIASUBTYPE \_ MPEG \_ HEAAC)** für die MP4-Dateiwiedergabe.
-   **MEDIASUBTYPE \_ RAW \_ AAC1**.

### <a name="property-sets"></a>Eigenschaftensätze

Der Eingabepin des Decoders unterstützt die folgenden Eigenschaftensätze über [**IKsPropertySet:**](ikspropertyset.md)

-   [**DVD Copy Protection-Eigenschaftensatz**](dvd-copy-protection-property-set.md)
-   [**Ratenänderungseigenschaftensatz**](rate-change-property-set.md).

> [!Note]  
> Ab Windows 7 unterstützt der Decoder den Trickmodus über den Ratenänderungseigenschaftensatz. Sie unterstützt Wiedergaberaten im Bereich \[ von 0,501 bis 2,0, \] wobei 1,0 die normale Wiedergaberate und 2,0 die doppelte Normalrate ist.

 

### <a name="codec-properties"></a>Codeceigenschaften

Der Eingabepin des Decoders unterstützt die folgenden Eigenschaften über [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Eigenschaft                                                          | Erforderlich                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Windows Nur Vista; wird in Windows 7 oder höher nicht unterstützt. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Der Filter unterstützt die folgenden Eigenschaften über [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Eigenschaft                                                                          | Erforderlich      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (siehe Hinweis 3.) | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. Die [**AVDecCommonOutputFormat-Eigenschaft**](avdeccommonoutputformat-property.md) muss festgelegt werden, bevor der Ausgabepin des Decoders verbunden wird. Andernfalls hat die Änderung keine Auswirkungen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Audiountertypen**](audio-subtypes.md)
</dt> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**DVD-Medientypen**](dvd-media-types.md)
</dt> </dl>

 

 

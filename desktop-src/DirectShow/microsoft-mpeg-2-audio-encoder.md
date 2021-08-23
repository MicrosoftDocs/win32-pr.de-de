---
description: Der Microsoft MPEG-2 Audio Encoder-Filter codiert die MPEG-1-Audioebenen I und II, einschließlich Unterstützung für die MPEG-2 Low Sampling Frequency (LSF)-Erweiterungen.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Microsoft MPEG-2 Audio Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584120"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Microsoft MPEG-2-Audioencoder

Der Microsoft MPEG-2 Audio Encoder-Filter codiert die MPEG-1-Audioebenen I und II, einschließlich Unterstützung für die MPEG-2 Low Sampling Frequency (LSF)-Erweiterungen.

Verwenden Sie zum Codieren und Multiplexen von Audio-/Videostreams den [**Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) Encoder-Filter, der die Funktionen dieses Filters und des [**Microsoft MPEG-2 Video Encoder-Filters**](microsoft-mpeg-2-video-encoder.md) kapselt.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filterinformationen

Filterschnittstellen

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabepin-Medientypen

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**

Eingabepinschnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabepin-Medientypen

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Streamen** von **, MEDIASUBTYPE \_ MPEG2-AUDIO \_**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/>

Ausgabe-PIN-Schnittstellen

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtern der CLSID

**CLSID \_ CMPEG2EncoderAudioDS** (deklariert in wmcodecdsp.h)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**NICHT \_ \_ VERWENDEN \_**

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Hinweise

Der MPEG-2-Audioencoder kann die folgenden Ausgabearten erzeugen:

-   Elementarer Audiodatenstrom
-   Audio in einem MPEG-2-Programmstream
-   Audio in einem MPEG-2-Transportstream

Er unterstützt MPEG-1-Ebenen I- und II- und MPEG-2-Erweiterungen mit niedriger Samplinghäufigkeit (Low Sampling Frequency, LSF).

Eingabebeispiele müssen 16 Bits pro Stichprobe mit einer Audio-Samplingrate von 48, 44,1, 32, 22,05 oder 16 KHz haben. Der Encoder kann den Audiostream nicht erneutsammpeln. Die codierte Audiodatei hat die gleiche Abtastrate wie die Eingabe.

Eingabebeispiele müssen Mono oder Stereo sein. Das codierte Audio hat die Anzahl der Kanäle als Eingabe.

### <a name="limitations"></a>Einschränkungen

Der Encoder unterstützt Folgendes nicht:

-   MPEG Layer III-Audiobitstreams.
-   MPEG-2-Bitstreams für Multichannelerweiterungen.
-   MPEG-4 AAC-Bitstreams.
-   MPEG-2-Bitstreams, die nicht abwärtskompatibel (NBC) sind.
-   Generierung von paketierten elementaren Streampaketen (PES).
-   Dolby Digital-Codierung.

### <a name="codec-properties"></a>Codec-Eigenschaften

Der Filter unterstützt die folgenden Eigenschaften über [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> In einer früheren Version der Dokumentation wurden fälschlicherweise einige zusätzliche Eigenschaften aufgeführt, die nicht unterstützt werden.

 

Aus Gründen der Abwärtskompatibilität unterstützt der Filter die folgende Eigenschaft über die **IEncoderAPI-Schnittstelle:**



| Eigenschaft                 | Beschreibung                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **ENCAPIPARAM-BITRATE \_** | Entspricht [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

Es wird empfohlen, Eigenschaften in der folgenden Reihenfolge zu setzen:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Legen Sie die restlichen Eigenschaften in beliebiger Reihenfolge fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**MPEG-2-Demultiplexer-Medientypen**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 

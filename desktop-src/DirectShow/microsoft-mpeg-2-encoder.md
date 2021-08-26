---
description: Der Microsoft MPEG-2-Encoderfilter codiert MPEG-2-Audio und -Video und multiplext die Datenströme, um einen MPEG-2-Programmstream oder -Transportstream zu generieren.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Microsoft MPEG-2 Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ae7f1bd9cb8233d919689bbeb1eea496760ae1254bae88120776364528243d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051230"
---
# <a name="microsoft-mpeg-2-encoder"></a>Microsoft MPEG-2-Encoder

Der Microsoft MPEG-2-Encoderfilter codiert MPEG-2-Audio und -Video und multiplext die Datenströme, um einen MPEG-2-Programmstream oder -Transportstream zu generieren.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filterinformationen

Filterschnittstellen

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabepinmedientypen

Siehe Hinweise

Eingabe-Pin-Schnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Medientypen des Ausgabepins

Siehe Hinweise

Ausgabe-Pin-Schnittstellen

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtern von CLSID

**CLSID \_ CMPEG2EncoderDS** (deklariert in wmcodecdsp.h)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**NOT USE (NICHT \_ \_ \_ VERWENDEN)**

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Hinweise

Dieser Filter kombiniert die Codierungsfunktionen von zwei anderen Filtern:

-   [**Microsoft MPEG-2-Audioencoder**](microsoft-mpeg-2-audio-encoder.md)
-   [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md)

Außer wie bereits erwähnt unterstützt dieser Filter die gleichen Codierungsfeatures wie diese beiden Encoder.

Anfänglich verfügt der Filter über einen Eingabepin, der Audio- oder Videoeingaben akzeptieren kann. Wenn diese Stecknadel verbunden ist, erstellt der Filter einen zweiten Eingabepin. Wenn der erste Eingabepin Audiodaten empfängt, akzeptiert der zweite Eingabepin nur Videos und umgekehrt. Jeder Eingabepin unterstützt die gleichen Medientypen wie der entsprechende Encoderfilter.

Wenn nur ein Eingabepin verbunden ist, unterstützt der Filter die gleichen Ausgabetypen wie der entsprechende Audio- oder Videoencoder. Wenn beide Pins verbunden sind, unterstützt der Filter die folgenden Ausgabearten:

-   Audiovisual in einem MPEG-2-Programmstream
-   Audiovisual in einem MPEG-2-Transportstream

Diese entsprechen den folgenden Ausgabetypen:

-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**
-   **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**

Dieser Filter kann keine Multiplexstreams, die zuvor codiert wurden. Die Eingabestreams müssen unkomprimierte Audio-/Videodatenströme sein, die der Filter vor dem Multiplexing codiert. Der Multiplexstream ist auf ein Programm beschränkt, das bis zu einem Audio- und einem Videostream enthält.

### <a name="codec-properties"></a>Codeceigenschaften

Der Filter unterstützt die kombinierten Eigenschaften der Filter [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) und [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) mit folgendem Unterschied:

-   Die [**AVEncCommonMeanBitRate-Eigenschaft**](avenccommonmeanbitrate-property.md) legt die durchschnittliche Bitrate für den Videostream fest.
-   Die [**AVEncAudioMeanBitRate-Eigenschaft**](avencaudiomeanbitrate.md) legt die durchschnittliche Bitrate für den Audiostream fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 

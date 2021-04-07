---
description: Der Microsoft MPEG-2 Encoder-Filter codiert MPEG-2-Audiodaten und-Videos und multiplediert die Streams, um einen MPEG-2-Programmstream oder einen Transportstream zu generieren.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Microsoft MPEG-2 Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745968"
---
# <a name="microsoft-mpeg-2-encoder"></a>Microsoft MPEG-2-Encoder

Der Microsoft MPEG-2 Encoder-Filter codiert MPEG-2-Audiodaten und-Videos und multiplediert die Streams, um einen MPEG-2-Programmstream oder einen Transportstream zu generieren.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filter Informationen

Filter Schnittstellen

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **Iencoderapi**<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ivideoencoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabe-PIN-Medientypen

Siehe Hinweise

PIN-Eingabeschnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

Siehe Hinweise

PIN-Schnittstellen

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID Filtern

**CLSID \_ CMPEG2EncoderDS** (in wmcodecdsp. h deklariert)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**das Verdienst wird \_ \_ nicht \_ verwendet.**

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter kombiniert die Codierungs Funktionen von zwei anderen Filtern:

-   [**Microsoft MPEG-2-Audioencoder**](microsoft-mpeg-2-audio-encoder.md)
-   [**Microsoft MPEG-2-Video Encoder**](microsoft-mpeg-2-video-encoder.md)

Sofern nicht anders angegeben, unterstützt dieser Filter dieselben Codierungs Funktionen wie diese beiden Encoder.

Anfänglich hat der Filter eine Eingabe-PIN, die Audiodaten oder Videoeingaben akzeptieren kann. Wenn diese Pin verbunden ist, erstellt der Filter eine zweite Eingabe-PIN. Wenn die erste Eingabe-PIN Audiodaten empfängt, akzeptiert die zweite Eingabe-PIN nur Video und umgekehrt. Jede Eingabe-PIN unterstützt die gleichen Medientypen wie der entsprechende Codierungs Filter.

Wenn nur eine Eingabe-PIN verbunden ist, unterstützt der Filter dieselben Ausgabetypen wie der entsprechende Audio-oder Video Encoder. Wenn beide Pins verbunden sind, unterstützt der Filter die folgenden Arten der Ausgabe:

-   Audiovisualisierung in einem MPEG-2-Programmstream
-   Audiovisualisierung in einem MPEG-2-Transportstream

Diese entsprechen den folgenden Ausgabetypen:

-   **MediaType \_ Stream**, **mediasubtype \_ - \_ Programm**
-   **MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Transport**

Dieser Filter kann keine zuvor codierten Datenströme Multiplexes. Die Eingabedaten Ströme müssen unkomprimierte Audiodaten und Videos sein, die vom Filter vor Multiplexing codiert werden. Der Multiplex-Stream ist auf ein Programm beschränkt, das bis zu einen Audiostream und einen Videostream enthält.

### <a name="codec-properties"></a>Codec-Eigenschaften

Der Filter unterstützt die kombinierten Eigenschaften des [**MPEG-2-Audioencoders**](microsoft-mpeg-2-audio-encoder.md) und [**MPEG-2-Video Encoder**](microsoft-mpeg-2-video-encoder.md) -Filter mit folgendem Unterschied:

-   Mit der Eigenschaft " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md) " wird die durchschnittliche Bitrate für den Videostream festgelegt.
-   Mit der Eigenschaft " [**avencaudiomeanbitrate**](avencaudiomeanbitrate.md) " wird die durchschnittliche Bitrate für den Audiostream festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 

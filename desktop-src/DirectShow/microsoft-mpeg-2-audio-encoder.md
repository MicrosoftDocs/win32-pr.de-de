---
description: Der Microsoft MPEG-2-audioencoderfilter codiert MPEG-1-Audioebenen I und II, einschließlich der Unterstützung für die MPEG-2-LSF-Erweiterungen (Low Sampling Frequency).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Microsoft MPEG-2-Audioencoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342727"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Microsoft MPEG-2-Audioencoder

Der Microsoft MPEG-2-audioencoderfilter codiert MPEG-1-Audioebenen I und II, einschließlich der Unterstützung für die MPEG-2-LSF-Erweiterungen (Low Sampling Frequency).

Verwenden Sie zum Codieren und multiplezieren von Audio-/Videostreams den [**Microsoft MPEG-2 Encoder-**](microsoft-mpeg-2-encoder.md) Filter, der die Funktionen dieses Filters und des [**Microsoft MPEG-2-Video Encoder-**](microsoft-mpeg-2-video-encoder.md) Filters kapselt.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filter Informationen

Filter Schnittstellen

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **Iencoderapi**<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ivideoencoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabe-PIN-Medientypen

**MediaType \_ Audiodatei**, **mediasubtype \_ PCM**

PIN-Eingabeschnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

**MediaType \_ Audiodatei**, **mediasubtype \_ \_ -Audiodatei**<br/> **MediaType \_ Stream**, **mediasubtype \_ \_ -Audiodatei**<br/> **MediaType \_ Stream**, **mediasubtype \_ - \_ Programm**<br/> **MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Transport**<br/>

PIN-Schnittstellen

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID Filtern

**CLSID \_ CMPEG2EncoderAudioDS** (in wmcodecdsp. h deklariert)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**das Verdienst wird \_ \_ nicht \_ verwendet.**

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

## <a name="remarks"></a>Bemerkungen

Der MPEG-2-Audioencoder kann die folgenden Arten der Ausgabe liefern:

-   Audioelementstream
-   Audiodaten in einem MPEG-2-Programm Datenstrom
-   Audiodaten in einem MPEG-2-Transportstream

Es werden MPEG-1-Ebenen I und II und MPEG-2 Low Sampling Frequency (LSF)-Erweiterungen unterstützt.

Eingabe Beispiele müssen 16 Bits pro Beispiel mit einer audiosamplingrate von 48, 44,1, 32, 22,05 oder 16 kHz sein. Der Encoder kann den Audiostream nicht neu einspielen. die codierte Audiodatei hat dieselbe Stichprobenrate wie die Eingabe.

Eingabe Beispiele müssen Mono oder Stereo sein. Die codierte Audiodatei hat die Anzahl von Kanälen als Eingabe.

### <a name="limitations"></a>Einschränkungen

Der Encoder unterstützt Folgendes nicht:

-   MPEG Layer III-audiobitstreams.
-   MPEG-2-multikanalerweiterungs-Bitstreams.
-   MPEG-4-AAC-Bitstreams.
-   Nicht rückwärtskompatible MPEG-2-Bitstreams (NBC).
-   Generierung von Paketen, die mit packetisiert (Elementary Stream) generiert werden.
-   Dolby Digital Encoding.

### <a name="codec-properties"></a>Codec-Eigenschaften

Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

-   [**Avaudiochannelcount**](avaudiochannelcount-property.md)
-   [**Avaudiosamplerate**](avaudiosamplerate-property.md)
-   [**Avencaudiointervaldecodecode**](avencaudiointervaltoencode-property.md)
-   [**Avenccommonformateinschränkung**](avenccommonformatconstraint-property.md)
-   [**Avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)
-   [**Avencmpacodingmode**](avencmpacodingmode-property.md)
-   [**Avencmpacopyright**](avencmpacopyright-property.md)
-   [**Avencmpbetonung sType**](avencmpaemphasistype-property.md)
-   [**Avencmpenableredundancyprotection**](avencmpaenableredundancyprotection-property.md)
-   [**Avencmpalayer**](avencmpalayer-property.md)
-   [**Avencmporiginalbitstream**](avencmpaoriginalbitstream-property.md)
-   [**Avencmpaprivateuserbit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> In einer früheren Version der Dokumentation wurden nicht ordnungsgemäß einige zusätzliche Eigenschaften aufgeführt, die nicht unterstützt werden.

 

Aus Gründen der Abwärtskompatibilität unterstützt der Filter die folgende Eigenschaft über die **iencoderapi** -Schnittstelle:



| Eigenschaft                 | BESCHREIBUNG                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **"endparam"- \_ Bitrate** | Äquivalent zu " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)". |



 

Es wird empfohlen, die Eigenschaften in der folgenden Reihenfolge festzulegen:

1.  [**Avenccommonformateinschränkung**](avenccommonformatconstraint-property.md)
2.  [**Avencmpalayer**](avencmpalayer-property.md)
3.  [**Avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)
4.  [**Avencmpacodingmode**](avencmpacodingmode-property.md)

Legen Sie die restlichen Eigenschaften in beliebiger Reihenfolge fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**MPEG-2-Demultiplexer-Medientypen**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 

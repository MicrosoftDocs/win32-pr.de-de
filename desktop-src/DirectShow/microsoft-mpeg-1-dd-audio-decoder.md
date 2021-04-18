---
description: 'Dieser Filter decodiert die folgenden Audioformate:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Microsoft MPEG-1/DD/AAC-Audiodecoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338863"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Microsoft MPEG-1/DD/AAC-Audiodecoder

Dieser Filter decodiert die folgenden Audioformate:

-   MPEG-1-Audioebenen I und II.
-   Rückwärtskompatible MPEG-2-Audiodaten, Schichten I und II (ISO/IEC 13818-3), Mono und Stereo.
-   LC-Profil (Advanced audiocoding) mit geringer Komplexität.
-   High-Efficiency AAC (HE-AAC) Version 1 und Version 2.
-   Pass-Through Digital Theater Systems (DTS) für die digitale Ausgabe.
-   Nur LPCM, Mono und Stereo, mit oder ohne PES-Header.
-   Dolby Digital.
-   Dolby Digital Plus, einschließlich der Konvertierung von Dolby Digital Plus in Dolby Digital for Digital Output.

> [!Note]  
> Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 

Für das Decodieren von Dolby Digital Plus-, AAC-und HE-AAC-Formaten ist Windows 7 erforderlich. Das Decodieren von Dolby Digital oder Dolby Digital Plus wird unter Windows 7 Home Basic oder Windows 7 Starter nicht unterstützt.

In der Registrierung lautet der Anzeige Name dieses Filters "Microsoft DTV-DVD-Audiodecoder".



Filter Informationen

Filter Schnittstellen

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Eingabe-PIN-Medientypen

In Windows Vista und höher unterstützt der Filter die folgenden Eingabetypen:<br/>

-   **MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)
-   **MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1Audio**
-   **MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1Payload**
-   **MediaType \_ Audiodatei**, **mediasubtype \_ \_ -Audiodatei**
-   **MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)
-   **MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ DTS** (siehe Hinweis 2)
-   **MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**
-   **MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ \_ -Audiodatei**
-   **MediaType \_ MPEG2 \_ PES**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)
-   **MediaType \_ MPEG2 \_ PES**, **mediasubtype \_ DTS** (siehe Hinweis 2)
-   **MediaType \_ MPEG2- \_ PES**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**
-   **MediaType \_ MPEG2- \_ PES**, **mediasubtype \_ \_ -Audiodatei**
-   **MediaType \_ Stream**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)
-   **MediaType \_ Stream**, **mediasubtype \_ MPEG1Audio**
-   **MediaType \_ Stream**, **mediasubtype \_ \_ -Audiodatei**

Ab Windows 7 unterstützt der Filter auch die folgenden Eingabetypen:<br/>

-   **MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ ddplus** (siehe Hinweis 1)
-   **MediaType \_ Audiodatei**, **mediasubtype \_ DTS2** (siehe Hinweis 2)
-   **MediaType \_ Audiodatei**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**
-   **MediaType \_ Audiodatei**, **mediasubtype \_ DVM** (siehe Hinweis 1)
-   **MediaType \_ Audiodatei**, **mediasubtype \_ MPEG \_ ADTs \_ AAC**
-   **MediaType \_ Audiodatei**, **mediasubtype \_ MPEG \_ LoAs**
-   **MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1AudioPayload**
-   **MediaType \_ Audiodatei**, **mediasubtype \_ RAW \_ AAC1**
-   **MediaType \_ Stream**, **mediasubtype \_ Dolby \_ ddplus** (siehe Hinweis 1)
-   **MediaType \_ Stream**, **mediasubtype \_ MPEG \_ ADTs \_ AAC**
-   **MediaType \_ Stream**, **mediasubtype \_ MPEG \_ LoAs**

Der Eingabetyp kann beim Streaming dynamisch geändert werden.<br/> Weitere Informationen zu diesen Medientypen finden Sie unter [**audiountertypen**](audio-subtypes.md).<br/>

> [!Note]  
> 1. Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.

<br/>

> [!Note]  
> 2. Bei der Eingabe von Digital Theater Systems (DTS) werden nur die S/PDIF-Ausgabe unterstützt (DTS over s/PDIF). Audiodecodierung wird nicht unterstützt.

<br/>

PIN-Eingabeschnittstellen

[**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**"Ikspropertyset"**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

In Windows Vista und höher unterstützt der Filter die folgenden Ausgabetypen:<br/>

-   **MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3 \_ SPDIF** (identisch mit dem **ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital**)
-   **MediaType \_ Audiodatei**, **mediasubtype \_ PCM**

Ab Windows 7 unterstützt der Filter auch die folgenden Ausgabetypen:<br/>

-   **MediaType \_ Audiotyp**, **ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS**
-   **MediaType \_ Audiodatei**, **mediasubtype \_ IEEE \_ float**

PIN-Schnittstellen

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID Filtern

**CLSID \_ CMPEG2AudDecoderDS** (in wmcodecdsp. h deklariert)

Ausführbare Datei

msmpeg2adec.dll

[Verdienst](merit.md)

**Verdienst \_ NORMAL** -1

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

> [!Note]  
> In einer früheren Version der Dokumentation wurde angegeben, dass dieser Filter "MPEG-2-Audiodatei" decodieren kann. Der Filter decodiert nur abwärts kompatible MPEG-2-Audiodaten.

 

## <a name="remarks"></a>Bemerkungen

Mono-Streams werden immer in Stereo decodiert.

Für Streams mit einer Kanal Konfiguration von zwei oder mehr Referenten führt der Decoder einen der folgenden Schritte aus:

-   Up: kombiniert mit der Common 5,1-sprecherkonfiguration für sechs Kanäle.
-   Downmix auf Stereo.

Um zwischen diesen beiden Optionen auszuwählen, legen Sie mit der [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle die [**avdeccommonoutputformat**](avdeccommonoutputformat-property.md) -Eigenschaft fest, bevor Sie die Pins verbinden. Wenn die Anwendung das Filter Diagramm erstellt, kann Sie alternativ den gewünschten Medientyp in der Ausgabe-PIN festlegen.

### <a name="aac-decoding"></a>AAC-Decodierung

Bei AAC hat der Decoder bestimmte Format Einschränkungen für die komprimierte AAC-Eingabe. Diese Format Einschränkungen sind identisch mit dem Media Foundation [**AAC-Decoder**](../medfound/aac-decoder.md)und sind im Abschnitt "[**Format Einschränkungen**](../medfound/aac-decoder.md)" dokumentiert.

Der DirectShow-Decoder akzeptiert auch andere Eingabetypen als der Media Foundation Decoder. Der DirectShow-Decoder unterstützt die folgenden AAC-Eingabetypen:

-   **Mediasubtype \_ RAW \_ AAC1**: RAW AAC, in der Regel in AVI oder Matroska (. MKV-Dateien).
-   **Mediasubtype \_ MPEG \_ ADTs \_ AAC**: AAC in einem audiodatentransport-Stream (ADTs) für das Streaming.
-   **Mediasubtype \_ MPEG \_ LoAs**: Transportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).

Der Media Foundation-Decoder unterstützt die folgenden AAC-Eingabetypen:

-   MF Audioformat \_ AAC (identisch mit **mediasubtype \_ MPEG \_ heaac**) für die Wiedergabe von MP4-Dateien.
-   **Mediasubtype \_ RAW \_ AAC1**.

### <a name="property-sets"></a>Eigenschaftensätze

Die Eingabe-PIN des Decoders unterstützt die folgenden Eigenschaften Sätze über " [**ikspropertyset**](ikspropertyset.md)":

-   [**Eigenschaften Satz für den DVD-Kopierschutz**](dvd-copy-protection-property-set.md)
-   [**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md).

> [!Note]  
> Ab Windows 7 unterstützt der Decoder den Trick Modus über den Satz von Eigenschaften für die Raten Änderung. Sie unterstützt Wiedergabe Raten im Bereich von \[ 0,501 – 2,0 \] , wobei 1,0 eine normale Wiedergabe Rate und 2,0 den doppelten Standardwert ist.

 

### <a name="codec-properties"></a>Codec-Eigenschaften

Die Eingabe-PIN des Decoders unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Eigenschaft                                                          | Erforderlich                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**Avaudiochannelconfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**Avaudiochannelcount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**Avaudiosamplerate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**Avddsurroundmode**](avddsurroundmode-property.md)             | Nur Windows Vista; wird in Windows 7 oder höher nicht unterstützt. |
| [**Avdecaudiodualmono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**Avdeccommoninputformat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**Avdeccommonmeanbitrate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Eigenschaft                                                                          | Erforderlich      |
|-----------------------------------------------------------------------------------|---------------|
| [**Avdecaacdownmixmode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**Avdecaudiodualmonorepromode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**Avdeccommonoutputformat**](avdeccommonoutputformat-property.md) (siehe Hinweis 3) | Windows Vista |
| [**Avdecdddynamicrangescalehigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**Avdecdddynamicrangescalelow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**Avdecddoperationalmode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**Avdecmmcssclass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**Avdsploudnesabqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**Avdspspeakerfill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. Die [**avdeccommonoutputformat**](avdeccommonoutputformat-property.md) -Eigenschaft muss festgelegt werden, bevor die Ausgabe-PIN des Decoders verbunden ist. Andernfalls hat die Änderung keine Auswirkungen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audiountertypen**](audio-subtypes.md)
</dt> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**DVD-Medientypen**](dvd-media-types.md)
</dt> </dl>

 

 

---
description: Der Microsoft MPEG-2 Video Encoder-Filter codiert MPEG-2- und MPEG-1-Videos.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Microsoft MPEG-2 Video Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7b70b9a754aefda3158ae355eb84c24b71b7e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474716"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Microsoft MPEG-2 Video Encoder

Der Microsoft MPEG-2 Video Encoder-Filter codiert MPEG-2- und MPEG-1-Videos.

Verwenden Sie zum Codieren und Multiplexen von Audio-/Videostreams den [**Microsoft MPEG-2-Encoderfilter,**](microsoft-mpeg-2-encoder.md) der die Funktionen dieses Filters und des [**Microsoft MPEG-2-Audioencoderfilters**](microsoft-mpeg-2-audio-encoder.md) kapselt.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filterinformationen

Filterschnittstellen

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabepinmedientypen

**MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ I420**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ IYUV**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ RGB24**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ UYVY**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ YUY2**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ YV12**<br/>

Eingabe-Pin-Schnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Medientypen des Ausgabepins

**MEDIATYPE \_ Streamen** von , **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**<br/>

Ausgabe-Pin-Schnittstellen

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtern von CLSID

**CLSID \_ CMPEG2EncoderVideoDS** (deklariert in wmcodecdsp.h)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**NOT USE (NICHT \_ \_ \_ VERWENDEN)**

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Hinweise

Der MPEG-2 Video Encoder kann die folgenden Ausgabearten erzeugen:

-   Elementarer Videostream
-   Video in einem MPEG-2-Programmstream
-   Video in einem MPEG-2-Transportstream

Es unterstützt die folgenden MPEG-2-Profile und -Ebenen:



| Profil        | Ebenen                     | Hinweise                                            |
|----------------|----------------------------|----------------------------------------------------|
| Einfaches Profil | Main                       |                                                    |
| Profil: Main   | Niedrig, Main, Hoch, Hoch-1440 |                                                    |
| Hohes Profil   | Main, High, High-1440      | Keine Skalierbarkeit oder 4:2:2/4:4:4-Unterstützung (nur 4:2:0) |
| 4:2:2 Profil  | Main, High                 | Keine Skalierbarkeit oder 4:2:2-Unterstützung (nur 4:2:0)       |



 

### <a name="codec-properties"></a>Codeceigenschaften

Der Filter unterstützt die folgenden Eigenschaften über [**ICodecAPI.**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Eigenschaft                                                                                      | Standard                                                          | Unterstützte Werte                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | MPEG-2-Video                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Nicht angegeben.                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (Keine Formateinschränkung)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-Video)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (Video-CD)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9800000 (9,8 MBit/s)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7000000 (7,0 MBit/s)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1 — 100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 — 100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **eAVEncCommonRateControlMode-Qualität \_**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Nicht angegeben.                                                      | eAVEncInputVideoSystem \_ Nicht angegeben<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ NTSC<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 — 2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Framemodus                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 — 1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 Frames (36 Felder) für NTSC; Andernfalls 15 Frames (30 Felder). | 1 — 30; siehe Hinweise                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8 — 10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Hoch                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Main                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ Interlaced**<br/> **eAVEncVideoSourceScan \_ Progressive**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Identisch mit der Quelle                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Identisch mit der Quelle                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Identisch mit der Quelle                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Identisch mit der Quelle                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Identisch mit der Quelle                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) – 1          | 0 oder [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) – 1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Muss mit der Eingabebildrate identisch sein.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Identisch mit der Eingabe                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

Es wird empfohlen, Eigenschaften in der folgenden Reihenfolge zu setzen:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Legen Sie die restlichen Eigenschaften in beliebiger Reihenfolge fest. (Weitere Informationen finden Sie jedoch [unter GOP-Struktur.)](#gop-structure)

Es ist möglich, Eigenschaften während der Ausführung des Filterdiagramms zu festlegen. Es gibt eine Verzögerung von mindestens einem GOP, bevor die neuen Einstellungen wirksam werden.

### <a name="encoder-operation"></a>Encodervorgang

Beim Codieren von MPEG-1-Videos legt der Encoder automatisch den 1-Bit-Flagcode für eingeschränkte Parameter im Sequenzheader fest, wenn alle Einschränkungen erfüllt sind. **\_ \_**

Bei Bedarf rundet der Encoder die Videoeingabedimensionen auf, sodass die Ausgabevideodimensionen den MPEG-Anforderungen entsprechen. Bei progressiven Videos werden die Ausgabedimensionen auf ein Vielfaches von 16 in Breite und Höhe aufgerundet. Für Interlaced-Videos wird die Breite auf ein Vielfaches von 16 aufgerundet, und die Höhe wird auf ein Vielfaches von 32 aufgerundet. Dieser Aufrundeungsvorgang verwendet bei Bedarf Auf padding.

Wenn das Video verschachtelt ist, führt der Encoder eine automatische Telecineerkennung (3:2 Pull-Down) durch. Das Eingabevideo kann neben Geschachtelten Frames auch Feldbildpaare enthalten.

Das interne Format des Encoders ist 4:2:0 IYUV (identisch mit I420). Sie kann Farbkonvertierung aus den Videoformaten YUY2, YV12, UYCLIP und RGB-24 durchführen.

Um den Bitstream auf ein Zielformat (DVD oder VCD) zu beschränken, legen Sie die [**AVEncCommonFormatConstraint-Eigenschaft**](avenccommonformatconstraint-property.md) fest. Wenn diese Eigenschaft über einen anderen Wert als **GUID \_ AVEncCommonFormatUnSpecified** verfügt, schränkt der Encoder die MPEG-Syntax auf den wert ein, der vom Zielformat zugelassen wird.

Legen Sie für die Livecodierung die [**EIGENSCHAFT AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) auf 0 (null) fest. Dies führt dazu, dass der Encoder die Geschwindigkeit optimiert.

### <a name="encoding-modes"></a>Codierungsmodi

Der Encoder unterstützt mehrere Codierungsmodi:

-   One-Pass Constant Bit Rate (CBR).
-   Auf der 1-Pass-Qualität basierende variable Bitrate (VBR) unter Verwendung einer konstanten Schrittgröße des Quantisierungsmoduls. In diesem Modus versucht der Encoder, eine Zielqualitätsstufe bis zu einer maximalen Bitrate zu erreichen.
-   1-Pass-VBR mit eingeschränkter Spitzenlast. In diesem Modus versucht der Encoder, eine durchschnittliche Zielbitrate innerhalb bestimmter interner Grenzwerte zu erreichen.

Legen Sie zum Konfigurieren des Codierungsmodus die folgenden Eigenschaften fest:




| Modus | Eigenschaften | 
|------|------------|
| CBR | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br /><a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 
| Qualitätsbasierte VBR | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br /><a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><blockquote>[!Note]<br />In diesem Modus werden die Eigenschaften <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> und <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> nicht verwendet. Es wird davon ausgegangen, dass die mindeste Bitrate 0 (null) ist.</blockquote><br /> | 
| VBR mit maximaler Auslastung | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br /><a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br /><a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 




 

> [!Note]  
> VbR mit zwei Durchlauf wird nicht unterstützt.

 

### <a name="aspect-ratio"></a>Seitenverhältnis

Das Seitenverhältnis für die Anzeige und das Pixel-Seitenverhältnis (PAR) sind mit der folgenden Formel verknüpft:

<dl> Seitenverhältnis anzeigen = PAR × (Bildbreite/Bildhöhe)  
</dl>

Der Encoder verwendet diese Formel, um den Wert des Seitenverhältnisses für \_ \_ MPEG-1-Bitstreams oder der \_ \_ Seitenverhältnisinformationen für MPEG-2-Bitstreams zu berechnen. (Siehe ISO/IEC 11172 bzw. ISO/IEC 138181-2.)

Der Encoder versucht die folgenden Einstellungen in der folgenden Reihenfolge:

1.  Wenn die Anwendung die [**AVEncVideoPixelAspectRatio-Eigenschaft**](avencvideopixelaspectratio-property.md) zu einem beliebigen Zeitpunkt vor der Ausführung des Filterdiagramms festlegt, wird diese Eigenschaft für par verwendet.
2.  Wenn andernfalls die **Elemente dwPictAspectRatioX** und **dwPictAspectRatioY** der [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) ungleich 0 (null) sind, werden diese Elemente für das Seitenverhältnis der Anzeige verwendet, und par wird aus dem Seitenverhältnis der Anzeige berechnet.
3.  Wenn keiner dieser Werte vorhanden ist, wird als PAR 1,0 angenommen, und das Seitenverhältnis für die Anzeige wird entsprechend berechnet.

Im Livecodierungsmodus [**(AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) gleich 0) muss das Seitenverhältnis für die Anzeige entweder 4:3 oder 16:9 mit dem Standardwert 4:3 sein. Wenn das berechnete Seitenverhältnis für die Anzeige nicht 4:3 oder 16:9 ist, verwendet der Encoder den Wert 4:3.

### <a name="gop-structure"></a>GOP-Struktur

Legen Sie die folgenden Eigenschaften in der angegebenen Reihenfolge fest, um die GoP-Struktur (Group of Picture) anzugeben:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

Basierend auf diesen Einstellungen erzeugt der Encoder eine der folgenden GOP-Strukturen:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | GOP-Struktur |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) – 1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) – 1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) – 1                         | 2                                                                             | IBBPBBP...    |



 

Die GOP-Standardstruktur ist IBBPBBP... mit einer GOP-Größe von 15 Frames.

Wenn die Anwendung das Zielformat auf DVD beschränkt (über die [**AVEncCommonFormatConstraint-Eigenschaft)**](avenccommonformatconstraint-property.md) und die [**AVEncInputVideoSystem-Eigenschaft**](avencinputvideosystem-property.md) auf NTSC oder PAL festlegt, unterstützt der Encoder die folgenden GOP-Größen:



| Videosystem | Gültige GOP-Größen | GoP-Standardgröße |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 Felder)   |
| PAL          | 1-15            | 15 (30 Felder)   |



 

### <a name="codec-property-change-lists"></a>Codec-Eigenschaftenänderungslisten

Das Festlegen des Werts einer Codeceigenschaft kann den gültigen Bereich einer anderen Eigenschaft ändern. (Wenn Sie z. B. das Zielformat einschränken, wird die durchschnittliche Bitrate eingeschränkt.) Wenn die Anwendung eine Eigenschaft festlegt, überprüft der Encoder, ob andere Eigenschaften jetzt außerhalb ihres gültigen Bereichs liegen. Wenn ja, setzt der Encoder diese Eigenschaft auf den neuen Standardwert zurück. Gehen Sie wie folgt vor, um in diesem Fall Benachrichtigungen zu erhalten:

1.  Rufen Sie [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) mit dem Wert **CODECAPI \_ CHANGELISTS auf.**
2.  Verwenden Sie die [**IMediaEventEx-Schnittstelle,**](/windows/desktop/api/Control/nn-control-imediaeventex) um Ereignisse aus dem Filterdiagramm zu überwachen.
3.  Wenn sich der Bereich oder Standardwert einer Eigenschaft ändert, sendet der Encoder ein [**EC \_ CODECAPI \_ EVENT-Ereignis**](ec-codecapi-event.md) mit einer Liste geänderter Eigenschaften.

### <a name="iencoderapi-support"></a>IEncoderAPI-Unterstützung

Aus Gründen der Abwärtskompatibilität unterstützt der Filter die folgenden Eigenschaften über die **IEncoderAPI-Schnittstelle:**



| Eigenschaft                       | BESCHREIBUNG                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **ENCAPIPARAM-BITRATE \_**       | Entspricht [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **ENCAPIPARAM \_ PEAK \_ BITRATE** | Entspricht [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **\_ENCAPIPARAM-BITRATE-MODUS \_** | Entspricht [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Beim Festlegen der **Eigenschaft ENCAPIPARAM \_ BITRATE \_ MODE** werden die Werte wie folgt zugeordnet:



| **\_ENCAPIPARAM-BITRATE-MODUS \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Siehe Hinweis.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Derzeit unterstützt der MPEG-2-Videoencoder den **VariableBitRateAverage-Codierungsmodus** nicht. Wenn Sie diesen Wert festlegen, verwendet der Encoder standardmäßig CBR-Codierung (**eAVEncCommonRateControlMode \_ CBR**).

 

Beim Abrufen der **Eigenschaft ENCAPIPARAM \_ BITRATE \_ MODE** werden die Werte wie folgt zugeordnet:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **\_ENCAPIPARAM-BITRATE-MODUS \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **eAVEncCommonRateControlMode-Qualität \_**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Einschränkungen

Derzeit unterstützt der Encoder keine der folgenden Features:

-   Generierung von paketisierten elementaren Streampaketen (PES).
-   Konvertierung der Framerate. Der Eingabestream muss eine Framerate haben, die für einen MPEG-2-Bitstream gültig ist.
-   Frameratenerweiterungen für MPEG-2 (**\_ \_ Bildfrequenzerweiterung \_ n**, **\_ \_ Bildfrequenzerweiterung \_ d**).
-   Einstiegs-/Beendigungspufferpositionen (ENTRY/Exit Buffer, VBV) für einen Clip.
-   Einfügen von Zeilen-21-Daten (Informationen zur Untertitelung) in den elementaren Videodatenstrom.
-   Festlegen des **25-Bit-Zeitcodefelds \_** im GOP-Header für MPEG-2.
-   Denoise-Filter.
-   Digital Rights Management (DRM).

Der Encoder führt eine Codierungslatenz von mindestens einem GOP ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**MPEG-2-Demultiplexer-Medientypen**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 

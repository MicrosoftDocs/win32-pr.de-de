---
description: Der Microsoft MPEG-2 Video Encoder Filter codiert MPEG-2-und MPEG-1-Video.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Microsoft MPEG-2-Video Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346410"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Microsoft MPEG-2-Video Encoder

Der Microsoft MPEG-2 Video Encoder Filter codiert MPEG-2-und MPEG-1-Video.

Verwenden Sie zum Codieren und multiplezieren von Audio-/Videostreams den [**Microsoft MPEG-2 Encoder-**](microsoft-mpeg-2-encoder.md) Filter, der die Funktionen dieses Filters und des [**Microsoft MPEG-2-audioencoderfilters**](microsoft-mpeg-2-audio-encoder.md) kapselt.

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filter Informationen

Filter Schnittstellen

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**Icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **Iencoderapi**<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ivideoencoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Eingabe-PIN-Medientypen

**MediaType \_ Video**, **mediasubtype \_ I420**<br/> **MediaType \_ Video**, **mediasubtype \_ IYUV**<br/> **MediaType \_ Video**, **mediasubtype \_ RGB24**<br/> **MediaType \_ Video**, **mediasubtype \_ UYVY**<br/> **MediaType \_ Video**, **mediasubtype \_ im YUY2**<br/> **MediaType \_ Video**, **mediasubtype \_ YV12**<br/>

PIN-Eingabeschnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

**MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Video**<br/> **MediaType \_ Stream**, **mediasubtype \_ - \_ Programm**<br/> **MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Transport**<br/> **MediaType \_ Video**, **mediasubtype \_ MPEG2- \_ Video**<br/>

PIN-Schnittstellen

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID Filtern

**CLSID \_ CMPEG2EncoderVideoDS** (in wmcodecdsp. h deklariert)

Ausführbare Datei

msmpeg2enc.dll

[Verdienst](merit.md)

**das Verdienst wird \_ \_ nicht \_ verwendet.**

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

## <a name="remarks"></a>Bemerkungen

Der MPEG-2-Video Encoder kann die folgenden Arten der Ausgabe liefern:

-   Video-elementare Datenstrom
-   Video in einem MPEG-2-Programm Datenstrom
-   Video in einem MPEG-2-Transportstream

Die folgenden MPEG-2-profile und-Ebenen werden unterstützt:



| Profil        | Ebenen                     | Bemerkungen                                            |
|----------------|----------------------------|----------------------------------------------------|
| Einfaches Profil | Main                       |                                                    |
| Profil: Main   | Niedrig, Main, hoch, hoch-1440 |                                                    |
| Hohes Profil   | Main, High, High-1440      | Keine Skalierbarkeit oder 4:2:2/4:4:4-Unterstützung (nur 4:2:0) |
| 4:2:2-Profil  | Main, hoch                 | Keine Skalierbarkeit oder 4:2:2-Unterstützung (nur 4:2:0)       |



 

### <a name="codec-properties"></a>Codec-Eigenschaften

Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Eigenschaft                                                                                      | Standard                                                          | Unterstützte Werte                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Avenccodectype**](avenccodectype-property.md)                                             | MPEG-2-Video                                                     | **Codecapi- \_ GUID \_ AVEncMPEG1Video**<br/> **Codecapi- \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**Avenccommonbufferinlevel**](avenccommonbufferinlevel-property.md)                         | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**Avenccommonbufferoutlevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**Avenccommonbuffersize**](avenccommonbuffersize-property.md)                               | 12222464 Bits                                                    |                                                                                                                                                                                                                      |
| [**Avenccommonformateinschränkung**](avenccommonformatconstraint-property.md)                   | Nicht angegeben.                                                      | **Codecapi \_ GUID " \_ avenccommonformatunspezifiziert** " (keine Format Einschränkung)<br/> **Codecapi \_ GUID \_ avenccommonformatdvd \_ V** (DVD-Video)<br/> **Codecapi \_ GUID \_ avenccommonformatvcd** (Video-CD)<br/> |
| [**Avenccommonmaxbitrate**](avenccommonmaxbitrate-property.md)                               | 9,8 Millionen (9,8 MS/Sekunde)                                       |                                                                                                                                                                                                                      |
| [**Avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)                             | 7 Millionen (7,0 ms/Sekunde)                                       |                                                                                                                                                                                                                      |
| [**Avenccommonminbitrate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**Avenccommonmultipassmode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**Avenccommonquality**](avenccommonquality-property.md)                                     | 100                                                              | 1 – 100                                                                                                                                                                                                              |
| [**Avenccommonqualityvsspeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 – 100                                                                                                                                                                                                              |
| [**Avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eavenccommonratecontrolmode- \_ CBR**<br/> **eavenccommonratecontrolmode \_ peakeinschräninedvbr**<br/> **eavenccommonratecontrolmode- \_ Qualität**<br/>                                                   |
| [**Avencinputvideosystem**](avencinputvideosystem-property.md)                               | Nicht angegeben.                                                      | eavencinputvideosystem \_ nicht angegeben<br/> eavencinputvideosystem- \_ PAL<br/> eavencinputvideosystem- \_ NTSC<br/>                                                                                        |
| [**Avencmpvdefaultbpicturecount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 – 2                                                                                                                                                                                                                |
| [**Avencmpvframefieldmode**](avencmpvframefieldmode-property.md)                             | Frame Modus                                                       |                                                                                                                                                                                                                      |
| [**Avencmpvgenerateheadercqdispext**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**Avencmpvgenerateheaderationqext**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**Avencmpvgopopen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**Avencmpvgopsinabl**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 – 1                                                                                                                                                                                                                |
| [**Avencmpvgopsize**](avencmpvgopsize-property.md)                                           | 18 Frames (36 Felder) für NTSC; 15 Frames (30 Felder) andernfalls. | 1 – 30; siehe Hinweise                                                                                                                                                                                                  |
| [**Avencmpvintradcprecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8 – 10                                                                                                                                                                                                               |
| [**Avencmpvlevel**](avencmpvlevel-property.md)                                               | High                                                             |                                                                                                                                                                                                                      |
| [**Avencmpvprofile**](avencmpvprofile-property.md)                                           | Main                                                             |                                                                                                                                                                                                                      |
| [**Avencvideodefaultupperfielddominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**Avencvideoforcesourcescantype**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eavencvideosourcescan \_ Interlacing**<br/> **eavencvideosourcescan \_ progressiv**<br/>                                                                                                                   |
| [**Avencvideoinputchromaresolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eavencvideochromaresolution \_ 420** (4:2:0)<br/> **eavencvideochromaresolution \_ sameassource**<br/>                                                                                                     |
| [**Avencvideoinputchromasubsampling**](avencvideoinputchromasubsampling-property.md)         | Identisch mit Quelle                                                   |                                                                                                                                                                                                                      |
| [**Avencvideoinputcolornominalrange**](avencvideoinputcolornominalrange-property.md)         | Identisch mit Quelle                                                   |                                                                                                                                                                                                                      |
| [**Avencvideoinputcolorprimaries**](avencvideoinputcolorprimaries-property.md)               | Identisch mit Quelle                                                   |                                                                                                                                                                                                                      |
| [**Avencvideoinputcolortransferfunction**](avencvideoinputcolortransferfunction-property.md) | Identisch mit Quelle                                                   |                                                                                                                                                                                                                      |
| [**Avencvideoinputcolortransfermatrix**](avencvideoinputcolortransfermatrix-property.md)     | Identisch mit Quelle                                                   |                                                                                                                                                                                                                      |
| [**Avencvideomaxkeyframedistance**](avencvideomaxkeyframedistance-property.md)               | [**Avencmpvgopsize**](avencmpvgopsize-property.md) -1          | 0 oder [**avencmpvgopsize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
| [**Avencvideonooffieldstococode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**Avencvideooutputchromaresolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eavencvideochromaresolution \_ 420** (4:2:0)<br/> **eavencvideochromaresolution \_ sameassource**<br/>                                                                                                     |
| [**Avencvideooutputframerate**](avencvideooutputframerate-property.md)                       |                                                                  | Muss mit der Eingabe Frame Rate identisch sein.                                                                                                                                                                            |
| [**Avencvideooutputscantype**](avencvideooutputscantype-property.md)                         | Identisch mit der Eingabe                                                    | **eavencvideooutputscan \_ sameasinput**                                                                                                                                                                               |
| [**Avencvideopixelaspectratio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

Es wird empfohlen, die Eigenschaften in der folgenden Reihenfolge festzulegen:

1.  [**Avenccommonformateinschränkung**](avenccommonformatconstraint-property.md)
2.  [**Avenccodectype**](avenccodectype-property.md)
3.  [**Avencmpvprofile**](avencmpvprofile-property.md)
4.  [**Avencmpvlevel**](avencmpvlevel-property.md)
5.  [**Avencinputvideosystem**](avencinputvideosystem-property.md)

Legen Sie die restlichen Eigenschaften in beliebiger Reihenfolge fest. (Siehe [GOP-Struktur](#gop-structure)).

Beim Ausführen des Filter Diagramms können Eigenschaften festgelegt werden. Es gibt eine Verzögerung von mindestens einem GOP, bevor die neuen Einstellungen wirksam werden.

### <a name="encoder-operation"></a>Codierungs Vorgang

Beim Codieren von MPEG-1-Videos legt der Encoder automatisch den Flag-Code mit eingeschränkten 1-Bit- **\_ Parametern \_** im Sequence-Header fest, wenn alle Einschränkungen erfüllt sind.

Bei Bedarf rundet der Encoder die Eingabe Video Dimensionen auf, sodass die Ausgabevideo Dimensionen den MPEG-Anforderungen entsprechen. Bei progressivem Video werden die Ausgabe Dimensionen in "width" und "Height" auf ein Vielfaches von 16 aufgerundet. Für das Video mit Zeilen Sprung wird die Breite auf ein Vielfaches von 16 aufgerundet, und die Höhe wird auf ein Vielfaches von 32 aufgerundet. Dieser aufrundungs Vorgang verwendet nach Bedarf Auffüll Zeichen.

Wenn das Video mit einem Zeilen Sprung verknüpft ist, führt der Encoder die automatische telecine-Erkennung (3:2-pulldownvorgang) aus. Das Eingabe Video kann neben Zeilen Sprung Paaren auch feldbildpaare enthalten.

Das interne Codierungsformat ist 4:2:0 IYUV (identisch mit I420). Sie kann eine Farbkonvertierung aus im YUY2-, YV12-, UYVY-und RGB-24-Videoformaten durchführen.

Um den Bitstrom auf ein Zielformat (DVD oder VCD) zu beschränken, legen Sie die Eigenschaft " [**avenccommonformateinschränkungs**](avenccommonformatconstraint-property.md) " fest. Wenn diese Eigenschaft einen anderen Wert als **GUID \_ avenccommonformatunspezifiziert** hat, schränkt der Encoder die MPEG-Syntax auf die vom Zielformat zugelassene ein.

Legen Sie für die Live Codierung die Eigenschaft " [**avenccommonqualityvsspeed**](avenccommonqualityvsspeed-property.md) " auf 0 (null) fest. Dies bewirkt, dass der Encoder die Geschwindigkeit optimiert.

### <a name="encoding-modes"></a>Codierungs Modi

Der Encoder unterstützt mehrere Codierungs Modi:

-   Konstante Bitrate (CBR) mit einer Pass-Through.
-   Qualitäts basierte bidirektionelle Bitrate (VBR) mit einem Wert für die Schrittgröße des Konstanten quantifizers. In diesem Modus versucht der Encoder, eine Ziel Qualitätsstufe bis zu einer maximalen Bitrate einzuhalten.
-   VBR mit einer Pass-Through-Spitzen Einschränkung. In diesem Modus versucht der Encoder, eine durchschnittliche Zielbitrate innerhalb bestimmter interner Grenzwerte zu erzielen.

Legen Sie zum Konfigurieren des Codierungs Modus die folgenden Eigenschaften fest:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Eigenschaften</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>Avenccommonratecontrolmode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>Avenccommonqualityvsspeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>Avenccommonmeanbitrate</strong></a><br/></td>
</tr>
<tr class="even">
<td>Qualitäts basierter VBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>Avenccommonratecontrolmode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>Avenccommonquality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>Avenccommonmaxbitrate</strong></a><br/>
<blockquote>
[!Note]<br />
In diesem Modus werden die Eigenschaften " <a href="avenccommonmeanbitrate-property.md"><strong>avenccommonmeanbitrate</strong></a> " und " <a href="avenccommonminbitrate-property.md"><strong>avenccommonminbitrate</strong></a> " nicht verwendet. Es wird davon ausgegangen, dass die minimale Bitrate NULL ist.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>VBR mit hoher Auslastung</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>Avenccommonratecontrolmode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>Avenccommonmultipassmode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>Avenccommonminbitrate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>Avenccommonmaxbitrate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>Avenccommonmeanbitrate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Zwei-Pass-VBR werden nicht unterstützt.

 

### <a name="aspect-ratio"></a>Seitenverhältnis

Das Anzeige Seitenverhältnis und das Pixel Seitenverhältnis (par) werden durch die folgende Formel verknüpft:

<dl> Seitenverhältnis anzeigen = par × (Bildbreite/Bildhöhe)  
</dl>

Der Encoder verwendet diese Formel, um den Wert des PEL \_ \_ -Seitenverhältnisses für MPEG-1-Bitstreams oder Seiten \_ Verhältnis \_ Informationen für MPEG-2-Bitstreams zu berechnen. (Siehe ISO/IEC 11172 bzw. ISO/IEC 138181-2.)

Der Encoder versucht die folgenden Einstellungen in der angegebenen Reihenfolge:

1.  Wenn die Anwendung die Eigenschaft " [**avencvideopixelaspectratio**](avencvideopixelaspectratio-property.md) " zu einem beliebigen Zeitpunkt vor dem Ausführen des Filter Diagramms festlegt, wird diese Eigenschaft für den Wert "par" verwendet.
2.  Wenn die Member **dwpictaspectratiox** und **dwpictaspectratioy** der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur nicht 0 (null) sind, werden diese Elemente für das Anzeige Seitenverhältnis verwendet, und der Wert wird aus dem Anzeige Seitenverhältnis berechnet.
3.  Wenn keiner dieser Werte vorhanden ist, wird davon ausgegangen, dass der Wert 1,0 ist, und das Seitenverhältnis der Anzeige wird entsprechend berechnet.

Im Live Encoding-Modus ([**avenccommonqualityvsspeed**](avenccommonqualityvsspeed-property.md) gleich null) muss das Seitenverhältnis der Anzeige entweder 4:3 oder 16:9 und den Standardwert 4:3 aufweisen. Wenn das berechnete Anzeige Seitenverhältnis nicht 4:3 oder 16:9 ist, verwendet der Encoder den Wert 4:3.

### <a name="gop-structure"></a>GOP-Struktur

Legen Sie die folgenden Eigenschaften in der angegebenen Reihenfolge fest, um die Gruppe der Bilds (GOP) anzugeben:

1.  [**Avencmpvgopsize**](avencmpvgopsize-property.md)
2.  [**Avencvideomaxkeyframedistance**](avencvideomaxkeyframedistance-property.md)
3.  [**Avencmpvdefaultbpicturecount**](avencmpvdefaultbpicturecount-property.md)

Basierend auf diesen Einstellungen erzeugt der Encoder eine der folgenden GOP-Strukturen:



| [**Avencvideomaxkeyframedistance**](avencvideomaxkeyframedistance-property.md) | [**Avencmpvdefaultbpicturecount**](avencmpvdefaultbpicturecount-property.md) | GOP-Struktur |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**Avencmpvgopsize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**Avencmpvgopsize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | Ibpbp...      |
| [**Avencmpvgopsize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | Ibbpbbp...    |



 

Die standardmäßige GOP-Struktur ist ibbpbbp... mit einer GOP-Größe von 15 Frames.

Wenn die Anwendung das Zielformat auf DVD einschränkt (über die Eigenschaft " [**avenccommonformateinschränkung**](avenccommonformatconstraint-property.md) ") und die Eigenschaft " [**avencinputvideosystem**](avencinputvideosystem-property.md) " auf "NTSC" oder "PAL" festlegt, unterstützt der Encoder die folgenden GOP-Größen:



| Video System | Gültige GOP-Größen | Standard-GOP-Größe |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 Felder)   |
| PAL          | 1-15            | 15 (30 Felder)   |



 

### <a name="codec-property-change-lists"></a>Änderungslisten für Codec-Eigenschaften

Wenn Sie den Wert einer Codec-Eigenschaft festlegen, kann der gültige Bereich einer anderen Eigenschaft geändert werden. (Durch Einschränkung des Ziel Formats wird beispielsweise die durchschnittliche Bitrate eingeschränkt.) Wenn die Anwendung eine Eigenschaft festlegt, prüft der Encoder, ob andere Eigenschaften nun außerhalb des gültigen Bereichs liegen. Wenn dies der Fall ist, setzt der Encoder diese Eigenschaft auf den neuen Standardwert zurück. Gehen Sie folgendermaßen vor, um Benachrichtigungen zu empfangen:

1.  Rufen Sie [**icodecapi:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) mit dem Wert **codecapi \_ changelists** auf.
2.  Verwenden Sie die [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle zum Überwachen von Ereignissen aus dem Filter Diagramm.
3.  Wenn sich der Bereich oder der Standardwert einer Eigenschaft ändert, sendet der Encoder ein [**EC \_ codecapi- \_ Ereignis**](ec-codecapi-event.md) Ereignis mit einer Liste von geänderten Eigenschaften.

### <a name="iencoderapi-support"></a>Iencoderapi-Unterstützung

Aus Gründen der Abwärtskompatibilität unterstützt der Filter die folgenden Eigenschaften über die **iencoderapi** -Schnittstelle:



| Eigenschaft                       | BESCHREIBUNG                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **"endparam"- \_ Bitrate**       | Äquivalent zu " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)".         |
| **\_Top-Bitrate für "endparam" \_** | Äquivalent zu " [**avenccommonmaxbitrate**](avenccommonmaxbitrate-property.md)".           |
| **encapiparam- \_ Bitrate- \_ Modus** | Entspricht dem Wert von " [**avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md)". |



 

Beim Festlegen der **encapiparam- \_ Bitrate- \_ Modus** -Eigenschaft werden die Werte wie folgt zugeordnet:



| **encapiparam- \_ Bitrate- \_ Modus** | [**Avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eavenccommonratecontrolmode- \_ CBR**                                      |
| **Variablebitrateaverage**     | Siehe Hinweis.                                                                 |
| **Variablebitratepeak**        | **eavenccommonratecontrolmode \_ peakeinschräninedvbr**                       |



 

> [!Note]  
> Derzeit unterstützt der MPEG-2-Video Encoder den **variablebitrateaverage** -Codierungs Modus nicht. Wenn Sie diesen Wert festlegen, wird der Encoder standardmäßig auf die CBR-Codierung (**eavenccommonratecontrolmode \_ CBR**) festgelegt.

 

Beim erhalten der **encapiparam- \_ Bitrate- \_ Modus** -Eigenschaft werden die Werte wie folgt zugeordnet:



| [**Avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md) | **encapiparam- \_ Bitrate- \_ Modus** |
|---------------------------------------------------------------------------|--------------------------------|
| **eavenccommonratecontrolmode- \_ CBR**                                      | **ConstantBitRate**            |
| **eavenccommonratecontrolmode- \_ Qualität**                                  | **Variablebitratepeak**        |
| **eavenccommonratecontrolmode \_ peakeinschräninedvbr**                       | **Variablebitratepeak**        |



 

### <a name="limitations"></a>Einschränkungen

Der Encoder unterstützt derzeit keines der folgenden Features:

-   Generierung von Paketen, die mit packetisiert (Elementary Stream) generiert werden.
-   Konvertierung von Frame Raten. Der Eingabestream muss eine Frame Rate aufweisen, die für einen MPEG-2-Bitstream gültig ist.
-   Frameraten Erweiterungen für MPEG-2 (**Frame \_ Raten \_ Erweiterung \_ n**, **Frame \_ Raten \_ Erweiterung \_ d**).
-   Position des Einstiegs-/Beendigungs Puffers (VBV) für einen Clip.
-   Einfügen von Zeilen 21-Daten (Closed Caption Information) in den elementaren Videodaten Strom.
-   Festlegen des 25-Bit- **Zeit \_ Code** Felds im GOP-Header für MPEG-2.
-   Bezeichnet den Filter.
-   Digital Rights Management (DRM).

Der Encoder führt eine Codierungs Latenz von mindestens einem GOP ein.

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

 

 

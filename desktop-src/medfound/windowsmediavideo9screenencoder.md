---
description: Der Windows Media Video 9-Bildschirm Encoder ist für das Codieren sequenzieller Screenshots von Computermonitoren optimiert.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Media Video 9-Bildschirm Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370755"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Media Video 9-Bildschirm Encoder

Der Windows Media Video 9-Bildschirm Encoder ist für das Codieren sequenzieller Screenshots von Computermonitoren optimiert.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Video 9-Bildschirm Encoder wird durch die Konstante **CLSID \_ CMSSCEncMediaObject2** dargestellt. Sie können eine Instanz des Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-types"></a>Eingabetypen

Die folgenden Eingabetypen werden vom Bildschirm Encoder der Version 9 unterstützt, wenn dieser als DirectX-Medienobjekt (DMO) verwendet wird.

-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ ARGB32
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB555
-   Mediasubtype \_ RGB8

Die folgenden Eingabetypen werden vom Bildschirm Encoder der Version 9 unterstützt, wenn dieser als Media Foundation Transformation (MFT) verwendet wird.

-   MF-Format \_ RGB24
-   MF-Format \_ RGB32
-   MF-Format \_ ARGB32
-   MF-Format \_ RGB565
-   MF-Format \_ RGB555
-   MF-Format \_ RGB8

## <a name="output-types"></a>Ausgabetypen

Der aus vier Zeichen bestehende Code (FourCC) für Windows Media Video Bildschirm codierten Inhalt der Version 9 ist "MSS2".

Die folgenden Ausgabetypen werden vom Bildschirm Encoder der Version 9 unterstützt.

-   Mediasubtype \_ MSS2

## <a name="encoder-properties"></a>Codierungs Eigenschaften

Der Windows Media Video 9-Bildschirm Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Gibt den Aufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern der komprimierten Inhalte verwendet wird.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Gibt die Anzahl der vom Codec codierten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>abgelöst.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Gibt die Komplexität des Encoder-Algorithmus an.<br/> <dl> Windows Vista und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Gibt das Ende eines Codierungs Durchlaufs an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Veraltet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP und höher. Lese-/Schreibzugriff.<br/> Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Gibt QP an. Mögliche Werte sind 1,0 bis 31,0.<br/> <dl> Windows Vista und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>Die Menge an Inhalt in Millisekunden, die in den Modell Puffer passen kann.<br/> <dl> Windows XP und höher<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Ein Bildschirm Codierungs Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als MFT (Media Foundation Transform) verwendet werden kann.

Ein Bildschirm Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Bildschirm Encoder als DMO oder MFT verhält.



| Betriebssystem            | Codierungs Verhalten                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media-Bildschirm Encoder verhält sich immer als DMO.                                                                                             |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Bildschirm Encoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle auf einem Bildschirm Encoder abrufen, verhält sie sich wie eine MFT. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> <dt>

[Verwenden des Windows Media Video 9-Bildschirm Codecs](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media Video 9-Bildschirm Decoder](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 





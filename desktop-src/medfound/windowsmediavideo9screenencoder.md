---
description: Der Windows Media Video 9 Screen Encoder ist für die Codierung sequenzieller Screenshots von Computermonitoren optimiert.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Media Video 9 Screen Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6d9fbe59671d978fb7374acbbc8ed1d8e9ea5afded0154242c4d1ccb4df3d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713140"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Media Video 9 Screen Encoder

Der Windows Media Video 9 Screen Encoder ist für die Codierung sequenzieller Screenshots von Computermonitoren optimiert.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Video 9 Screen-Encoder wird durch die Konstante **CLSID \_ CMSSCEncMediaObject2 dargestellt.** Sie können eine Instanz des Encoders erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="input-types"></a>Eingabetypen

Die folgenden Eingabetypen werden vom Screen-Encoder der Version 9 unterstützt, wenn er als DirectX Media Object (DMO.

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Die folgenden Eingabetypen werden vom Screen-Encoder der Version 9 unterstützt, wenn er als Media Foundation Transform (MFT) verwendet wird.

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>Ausgabetypen

Der vier zeichenbasierte Code (FOURCC) für Windows Media Video Screen Version 9-codierten Inhalt ist "MSS2".

Die folgenden Ausgabetypen werden vom Screen-Encoder der Version 9 unterstützt.

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>Encodereigenschaften

Der Windows Media Video 9 Screen-Encoder unterstützt die folgenden Eigenschaften.



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
<td>Gibt den Mehraufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern des komprimierten Inhalts verwendet wird.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Gibt das Pufferfenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable Bit Rate) mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG) an.</a><br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Gibt das Pufferfenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable Bit Rate) mit seiner Spitzenbitrate (angegeben durch <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX) an.</a><br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Gibt an, ob der codierte Videobitstream mit jedem Keyframe einen Puffer-Fullness-Wert enthält.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Gibt die Anzahl von Videoframes an, die vom Codec codiert werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Gibt die Anzahl von Videoframes an, die vom Codec codiert werden, die tatsächlich Daten enthalten.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX.</a><br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Gibt die Komplexität des Encoderalgorithmus an.<br/> <dl> Windows Vista und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Gibt eine numerische Darstellung des Kompromisses zwischen Bewegungsglättung und Bildqualität in der Codecausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Gibt die Anzahl von Videoframes an, die während der Codierung gelöscht werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Gibt das Ende eines Codierungspasses an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Gibt den FOURCC an, der den encoder identifiziert, den Sie verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Gibt die maximale Zeit in Millisekunden zwischen Keyframes in der Codecausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Veraltet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Gibt die maximale Anzahl von Durchläufen an, die vom Codec unterstützt werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP und höher. Lese-/Schreibzugriff.<br/> Gibt die Anzahl der Durchläufe an, die der Codec zum Codieren des Inhalts verwendet.<br/> <dl> Windows XP und höher.<br />
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
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable-Bit-Rate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Gibt die Spitzenbitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable-Bit-Rate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Gibt die Anzahl der Videoframes an, die während des Codierungsprozesses an den Encoder übergeben werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Gibt an, ob der Codec die VBR-Codierung (Variable Bit Rate) verwendet.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Gibt den tatsächlichen Qualitätsgrad für die qualitätsbasierte (1-Pass)-VBR-Codierung (Variable Bit Rate) an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>Die Menge an Inhalt in Millisekunden, die in den Modellpuffer passen kann.<br/> <dl> Windows XP und höher,<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Gibt die Anzahl der Videoframes an, die übersprungen wurden, da sie Duplikate vorheriger Frames waren.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Ein Bildschirmencoder-Objekt macht die **IMediaObject-Schnittstelle** verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die **BERTRANSFORM-Schnittstelle** verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Bildschirmencoder verhält sich wie ein DMO MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Bildschirmencoder als DMO MFT verhält.



| Betriebssystem            | Encoderverhalten                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media Screen-Encoder verhält sich immer wie ein DMO.                                                                                             |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media Screen-Encoder wie ein DMO. Wenn Sie eine **BENUTZEROBERFLÄCHETransform-Schnittstelle** auf einem Bildschirmencoder erhalten, verhält sie sich wie ein MFT. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> <dt>

[Verwenden des Windows Media Video 9-Bildschirmcodecs](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media Video 9-Bildschirmdecoder](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 





---
description: Der Windows Media Video 7/8-Encoder implementiert frühere Versionen des Windows Media Video Encoders.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Windows Media Video 7/8-Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359799"
---
# <a name="windows-media-video-78-encoder"></a>Windows Media Video 7/8-Encoder

Der Windows Media Video 7/8-Encoder implementiert frühere Versionen des Windows Media Video Encoders.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Video 7/8-Encoder ist **CLSID \_ cwmvxencmediaobject**. Sie können eine Instanz des Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="interfaces"></a>Schnittstellen

Ein Video Encoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Video Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Video Encoder als DMO oder MFT verhält.



| Betriebssystem            | Codierungs Verhalten                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media-Video Encoder verhält sich immer als DMO.                                                                                                                |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Video Encoder als DMO. Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle für einen Video Encoder erhalten, verhält sie sich wie eine MFT. |



 

## <a name="input-formats"></a>Eingabeformate

Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als DMO fungiert.

-   mediasubtype \_ IYUV
-   Mediasubtype \_ I420
-   Mediasubtype \_ YV12
-   Mediasubtype \_ NV11
-   Mediasubtype \_ NV12
-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   mediasubtype \_ yvyu
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB555
-   Mediasubtype \_ RGB8
-   mediasubtype- \_ Foto

Der Windows Media Video Encoder unterstützt die folgenden Eingabemedien-Untertypen, wenn er als MFT fungiert.

-   MF-Format ( \_ IYUV)
-   MF-Format \_ I420
-   MF-Format \_ YV12
-   MF-Format \_ NV11
-   MF-Format \_ NV12
-   MF-Format \_ im YUY2
-   MF-Format ( \_ UYVY)
-   Mfvideoformat \_ yvyu
-   MF-Format \_ RGB32
-   MF-Format \_ RGB24
-   MF-Format \_ RGB565
-   MF-Format \_ RGB555
-   MF-Format \_ RGB8
-   mediasubtype- \_ Foto

## <a name="output-formats"></a>Ausgabeformate

In der folgenden Tabelle sind die vier Zeichen Codes (fourccs) für die vom Windows Media Video 7/8-Encoder unterstützten Ausgabetypen aufgeführt.



| Category              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | "WMV1" |
| Windows Media Video 8 | "WMV2" |



 

## <a name="properties"></a>Eigenschaften

Der Windows Media Video 7/8-Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Gibt den Aufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern der komprimierten Inhalte verwendet wird.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Gibt die durchschnittliche Frame Rate von Videoinhalten in Frames pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Gibt die Anzahl der vom Codec codierten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>abgelöst.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Gibt die Komplexität des Encoder-Algorithmus an.<br/> <dl> Windows Vista und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Gibt die Geräte Konformitäts Vorlage an, der der codierte Inhalt entspricht.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Gibt das Ende eines Codierungs Durchlaufs an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Gibt an, ob die Codec-Ausgabe mit Zeilen Sprung dargestellt werden soll.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Gibt QP an.<br/> <dl> Windows Vista und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-Variable-Bitrate (VBR) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Gibt den Umfang des Inhalts in Millisekunden an, der in den Modell Puffer passen kann.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.<br/> <dl> Windows XP und höher.<br />
Schreibgeschützt<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> <dt>

[Video Untertyp-GUIDs](video-subtype-guids.md)
</dt> </dl>

 

 

---
description: Der Windows Media Video 9-Encoder codiert Videostreams.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Media Video 9-Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370756"
---
# <a name="windows-media-video-9-encoder"></a>Windows Media Video 9-Encoder

Der Windows Media Video 9-Encoder codiert Videostreams. Der Encoder unterstützt die folgenden vier Kategorien codierter Ausgaben.

-   Windows Media Video 9 einfaches Profil
-   Windows Media Video 9 Hauptprofil
-   Erweiterte profile Windows Media Video 9
-   Windows Media Video 9,1-Image

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Video Encoder wird durch die Konstante **CLSID \_ CWMV9EncMediaObject** dargestellt. Sie können eine Instanz des Video Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.

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

In der folgenden Tabelle werden die vier Zeichen Codes (fourccs) angezeigt, die den Kategorien der codierten Ausgabe entsprechen.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Media Video 9 einfaches Profil   | "WMV3"                                   |
| Windows Media Video 9 Hauptprofil     | "WMV3"                                   |
| Erweiterte profile Windows Media Video 9 | "WVC1"                                   |
| Windows Media Video 9,1-Image          | "Wmvp" für 9,1, "WVP2" für 9,1 Version 2 |



 

Um zwischen einfachem Profil und Hauptprofil zu unterscheiden, legen Sie die Eigenschaft [**mfpkey \_ decodercomplexityangeforderten**](mfpkey-decodercomplexityrequestedproperty.md) fest.

## <a name="properties"></a>Eigenschaften

Der Windows Media Video 9-Encoder unterstützt die folgenden Eigenschaften.



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
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Gibt die durchschnittliche Frame Rate von Videoinhalten in Frames pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der durchschnittlichen Bitrate (angegeben durch <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Gibt das Codierungs Muster an, das am Anfang einer Gruppe von Bildern verwendet werden soll.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Gibt die Anzahl der vom Codec codierten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
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
Einfaches Profil, Hauptprofil. Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Gibt den Typ der Optimierung an, der für den erweiterten profilcodec von Windows Media Video 9 verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Schreiben.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Nicht verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Gibt die Geräte Konformitäts Vorlage an, der der codierte Inhalt entspricht.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Gibt die Anzahl der während der Codierung gelöschten Videorahmen an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Gibt das Ende eines Codierungs Durchlaufs an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Gibt eine Zwischenrahmen Höhe für codiertes Video an.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Gibt eine zwischen Rahmenbreite für codiertes Video an.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Veraltet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Gibt an, ob der Encoder zum Löschen von Frames berechtigt ist.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Gibt an, ob die Codec-Ausgabe mit Zeilen Sprung dargestellt werden soll.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Nicht verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Gibt die Typen von Videoinformationen an, die bei Bewegungs Suchvorgängen verwendet werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Gibt den in Bewegungs suchen verwendeten Bereich an.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Gibt die Anzahl der Threads an, die der Codec für die Codierung verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Gibt die maximale Anzahl von durch den Codec unterstützten Durchläufen an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Gibt die Anzahl von Durchläufen an, die vom Codec zum Codieren des Inhalts verwendet werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Gibt an, ob der Encoder für doppelte Frames Dummy-Frame-Einträge im Bitdaten Strom erzeugt.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Gibt QP an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Gibt an, ob der Encoder die RD-basierte unter Pixel-MV-Suche verwendet. <br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Gibt für die Neucodierung von Segmenten die Puffergröße an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Gibt für die Neucodierung von Segmenten die Dauer des zu codierenden Segments an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Gibt für die Neucodierung von Segmenten den quantifizer des Frames vor dem Start Segment an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Gibt bei der Neucodierung von Segmenten die Größe des Start Puffers an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-Variable-Bitrate (VBR) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videorahmen an, die während des Codierungs Vorgangs an den Encoder übermittelt werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Gibt an, ob der Codec die VBR-Codierung (Variable-Bit-Rate) verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Gibt den Umfang des Inhalts in Millisekunden an, der in den Modell Puffer passen kann.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Gibt für die Neucodierung von Segmenten die privaten Codec-Daten der Datei an, die erneut codiert wird.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Gibt den Typ der Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videorahmen an, die übersprungen wurden, weil Sie Duplikate vorheriger Frames waren.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
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
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> </dl>

 

 

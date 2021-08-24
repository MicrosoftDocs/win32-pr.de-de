---
description: Der Windows Media Video 9-Encoder codiert Videostreams.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Media Video 9 Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d3d3e7feb06cfbe9e9149fd9fd55d76ecf5abe2fbe0d6eea6ac961a0561ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398240"
---
# <a name="windows-media-video-9-encoder"></a>Windows Media Video 9 Encoder

Der Windows Media Video 9-Encoder codiert Videostreams. Der Encoder unterstützt die folgenden vier Kategorien der codierten Ausgabe.

-   Windows Media Video 9 – einfaches Profil
-   Windows Media Video 9-Hauptprofil
-   Windows Media Video 9 Advanced Profile
-   Windows Media Video 9.1 Image

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Video Encoder wird durch die Konstante **CLSID \_ CWMV9EncMediaObject dargestellt.** Sie können eine Instanz des Videoencoder erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="interfaces"></a>Schnittstellen

Ein Videoencoder-Objekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**BERTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Videoencoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Videoencoder als DMO MFT verhält.



| Betriebssystem            | Encoderverhalten                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media Video Encoder verhält sich immer wie DMO.                                                                                                                |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Videoencoder wie ein DMO. Wenn Sie eine [**BERTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) für einen Videoencoder erhalten, verhält sie sich wie ein MFT. |



 

## <a name="input-formats"></a>Eingabeformate

Der Windows Media Video Encoder unterstützt die folgenden Eingabemedienuntertypen, wenn er als DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UY WIE
-   MEDIASUBTYPE \_ YVINNEN
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

Der Windows Media Video Encoder unterstützt die folgenden Eingabemedienuntertypen, wenn er als MFT agiert.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UY WIES
-   MFVideoFormat \_ YVVIDEO
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

## <a name="output-formats"></a>Ausgabeformate

In der folgenden Tabelle sind die Vier-Zeichen-Codes (FOURCCs) aufgeführt, die den Kategorien der codierten Ausgabe entsprechen.



| Kategorie                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Media Video 9 – einfaches Profil   | "WMV3"                                   |
| Windows Media Video 9-Hauptprofil     | "WMV3"                                   |
| Windows Media Video 9 Advanced Profile | "WVC1"                                   |
| Windows Media Video 9.1 Image          | "WMVP" für 9.1, "WVP2" für Version 9.1, Version 2 |



 

Um zwischen einfachem Profil und Hauptprofil zu unterscheiden, legen Sie die [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED-Eigenschaft**](mfpkey-decodercomplexityrequestedproperty.md) fest.

## <a name="properties"></a>Eigenschaften

Der Windows Media Video 9-Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Gibt den Mehraufwand in Bytes pro Paket an, der für den Container erforderlich ist, der zum Speichern des komprimierten Inhalts verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Gibt die durchschnittliche Bildfrequenz von Videoinhalten in Frames pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Gibt das Pufferfenster eines eingeschränkten VBR-Streams (Variable Bit Rate) in Millisekunden mit der durchschnittlichen Bitrate an (angegeben <a href="mfpkey-ravgproperty.md"><strong>durch MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Gibt die Deltaerhöhung zwischen dem Bildquantisierer des Ankerrahmens und dem Bildquantisierer des B-Frames an.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Gibt das Pufferfenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable Bit Rate) mit seiner Spitzenbitrate (angegeben durch <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX) an.</strong></a><br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Gibt an, ob der codierte Videobitstream mit jedem Keyframe einen Puffer-Fullness-Wert enthält.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Gibt das Codierungsmuster an, das am Anfang einer Gruppe von Bildern verwendet werden soll.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Gibt die Anzahl von Videoframes an, die vom Codec codiert werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Gibt die Anzahl von Videoframes an, die vom Codec codiert werden, die tatsächlich Daten enthalten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Diese Eigenschaft wird durch <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Gibt die Komplexität des Encoderalgorithmus an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil. Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Gibt den Typ der Optimierung an, der für den Windows Media Video 9 Advanced Profile-Codec verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreiben.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Gibt eine numerische Darstellung des Kompromisses zwischen Bewegungsglättung und Bildqualität in der Codecausgabe an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Wird nicht verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Gibt die Gerätekonformitätsvorlage an, der der codierte Inhalt entspricht.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Gibt die Gerätekonformitätsvorlage an, die Sie für die Videocodierung verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Gibt die Methode an, die zum Codieren der Bewegungsvektorinformationen verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Gibt an, ob der Codec den Rauschfilter bei der Codierung verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Gibt die gewünschte Qualitätsstufe für die qualitätsbasierte (1-Durch-) VBR-Codierung (Variable Bit Rate) an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Gibt die Anzahl von Videoframes an, die während der Codierung gelöscht werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Gibt das Ende eines Codierungspasses an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Gibt eine zwischengeschaltete Framehöhe für codiertes Video an.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Gibt eine zwischengeschaltete Framebreite für codiertes Video an.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Gibt an, ob der Codec die Medianfilterung während der Codierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Gibt den FOURCC an, der den encoder identifiziert, den Sie verwenden möchten.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Veraltet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Gibt an, ob der Encoder Frames ablegen darf.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Gibt an, ob die Codecausgabe als Interlacing verwendet wird.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Gibt die maximale Zeit in Millisekunden zwischen Keyframes in der Codecausgabe an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Wird nicht verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Gibt die Anzahl der Frames nach dem aktuellen Frame an, die der Codec vor dem Codieren des aktuellen Frames auswertet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Gibt an, ob der Codec den In-Loop-Deblockierungsfilter während der Codierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Gibt die Kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblockmodus verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Gibt die Methode an, die für den Bewegungsabgleich verwendet werden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Gibt die Arten von Videoinformationen an, die in Bewegungssuchvorgängen verwendet werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Gibt den bereich an, der bei Bewegungssuchen verwendet wird.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Gibt an, ob der Codec versuchen soll, laute Rahmenränder zu erkennen und zu entfernen.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Gibt die Anzahl bidirektionaler Vorhersageframes (B-Frames) an.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Gibt die Anzahl der Threads an, die der Codec für die Codierung verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Gibt die maximale Anzahl von Durchläufen an, die vom Codec unterstützt werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Gibt die Anzahl von Durchläufen an, die der Codec zum Codieren des Inhalts verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Gibt an, ob der Codec bei der Codierung eine konservative Wahrnehmungsoptimierung verwenden soll.<br/> <dl> Windows XP und höher.<br />
Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Gibt an, ob der Encoder Dummyframeeinträge im Bitstream für doppelte Frames erzeugt.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Gibt QP an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Gibt an, bis zu welchem Grad der Codec den effektiven Farbbereich des Videos reduzieren soll.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die VBR-Codierung (Variable-Bit-Rate) mit zwei Durchlaufwerten verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Gibt an, ob der Encoder die RD-basierte MV-Suche auf Subpixeln verwendet. <br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Gibt für die Neucodierung von Segmenten die Puffergröße an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Für die Segment-Neucodierung gibt die Dauer des neu codierten Segments an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Für die Segment-Neucodierung gibt den Quantizer des Frames vor dem Startsegment an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Für die Segment-Neucodierung gibt die Fullness des Startpuffers an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Gibt die Spitzenbitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-Variable-Bit-Rate (VBR) verwendet wird.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videoframes an, die während des Codierungsprozesses an den Encoder übergeben werden.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Gibt an, ob der Codec die VBR-Codierung (Variable Bit Rate) verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Gibt den tatsächlichen Qualitätsgrad für die qualitätsbasierte (1-Pass)-VBR-Codierung (Variable Bit Rate) an.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Gibt an, ob der Codec die Optimierung der Videoskalierung verwendet.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Gibt die Menge an Inhalt in Millisekunden an, die in den Modellpuffer passen kann.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Für die Segment-Neucodierung gibt die privaten Codecdaten der Datei an, die erneut codiert wird.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Gibt den Typ der Logik an, die der Codec zum Erkennen von Interlacing-Quellvideos verwendet.<br/> <dl> Windows XP und höher.<br />
Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Gibt die Anzahl der Videoframes an, die übersprungen wurden, da sie Duplikate vorheriger Frames waren.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Schreibgeschützt<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> </dl>

 

 

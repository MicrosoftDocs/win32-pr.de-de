---
description: DirectShow-Beispiele
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb99271821fcef80b66b379b29bd42de0505011fd47c8dfee208e6f00b007208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821165"
---
# <a name="directshow-samples"></a>DirectShow-Beispiele

Die DirectShow-Beispiele sind im Windows [SDK enthalten.](https://msdn.microsoft.com/windows/aa904949.aspx) Sie befinden sich unter dem Pfad \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

In der folgenden Tabelle sind alle DirectShow-Beispiele aufgeführt, die im Windows SDK bereitgestellt werden. Anweisungen zum Erstellen der Beispiele finden Sie in der Dokumentation im Windows SDK.

Wenn es zusätzliche Dokumentation für ein Beispiel gibt, ist die erste Spalte dieser Tabelle damit verknüpft.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispiel</th>
<th>Bereich</th>
<th>Beschreibung</th>
<th>Zusätzliche Abhängigkeiten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">DirectShow-Basisklassen</a></td>
<td>Basisklassenbibliothek</td>
<td>C++-Klassen und Hilfsfunktionen, die für die Implementierung von DirectShow-Filtern entwickelt wurden.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">AmCap-Beispiel</a></td>
<td>Erfassung</td>
<td>Videoaufnahmeanwendung.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">DVApp-Beispiel</a></td>
<td>Erfassung</td>
<td>Dv-Erfassungsanwendung (Digital Video).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">PlayCap-Beispiel</a></td>
<td>Erfassung</td>
<td>Einfache Erfassungsanwendung.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO Demobeispiel</a></td>
<td>DMO</td>
<td>Streams Audiodaten aus einer WAV-Datei über einen Audioeffekt DMO.</td>
<td>DirectX SDK</td>
</tr>
<tr class="even">
<td>DVD-Beispiel</td>
<td>DVD</td>
<td>Veranschaulicht die grundlegende DVD-Wiedergabe und -Navigation sowie erweiterte Features wie Verwaltung auf Elternebene, Lesezeichen, Synchronisierung und Befehlssynchronisierung.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">InfTee-Filterbeispiel</a></td>
<td>Filter, sonstige</td>
<td>Beispielimplementierung des <a href="infinite-pin-tee-filter.md">Filters Infinite Pin Tee.</a></td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Beispiel für Metronomfilter</a></td>
<td>Filter, sonstige</td>
<td>Zeigt, wie eine Verweisuhr implementiert wird.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">BEISPIEL FÜR PSI-Parserfilter</a></td>
<td>Filter, sonstige</td>
<td>Empfängt PSI-Tabellen (Program Specific Information) aus einem MPEG-2-Transportstream und extrahiert Programminformationen.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Beispiel für Dumpfilter</a></td>
<td>Filter, Renderer</td>
<td>Schreibt Medienbeispiele in eine Textdatei.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>SampVid-Filter</td>
<td>Filter, Renderer</td>
<td>Videorendererfilter.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Beispiel für Bereichsfilter</a></td>
<td>Filter, Renderer</td>
<td>Zeigt Sounddaten als Wellenformen an.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Beispiel für asynchrone Filter</a></td>
<td>Filter, Quelle</td>
<td>Dateilesefilter, der progressiven Download unterstützt.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Beispiel für Den Ballfilter</a></td>
<td>Filter, Quelle</td>
<td>Videoquellenfilter, der ein Bild einer Bouncing-Kugel erzeugt.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Beispiel für Pushquellenfilter</a></td>
<td>Filter, Quelle</td>
<td>Quellfilter, die die folgenden Daten als Videostream bereitstellen: eine einzelne Bitmap, eine Gruppe von Bitmaps, eine Kopie des aktuellen Desktopbilds.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Synth-Filterbeispiel</a></td>
<td>Filter, Quelle</td>
<td>Quellfilter, der Audio waveforms generiert. In diesem Beispiel wird die dynamische Graph-Entwicklung veranschaulicht.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">EZRGB24-Filterbeispiel</a></td>
<td>Filter, Transformieren</td>
<td>Bildverarbeitungsfilter.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Gargle-Filterbeispiel</a></td>
<td>Filter, Transformieren</td>
<td>Filter für Audioeffekt.</td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">WavDest-Filterbeispiel</a></td>
<td>Filter, Transformieren</td>
<td>Schreibt einen Audiostream in eine WAV-Datei.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">DMOEnum-Beispiel</a></td>
<td>verschiedene gefährliche Stoffe</td>
<td>Zeigt, wie <a href="directx-media-objects.md">DirectX-Medienobjekte (DMOs)</a> aufzählt werden.</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Mapper-Beispiel</a></td>
<td>verschiedene gefährliche Stoffe</td>
<td>Zeigt, wie Der <a href="filter-mapper.md">Filter-Mapper verwendet wird,</a> um Filter in der Registrierung zu suchen.</td>

</tr>
<tr class="even">
<td>SysEnum-Beispiel</td>
<td>verschiedene gefährliche Stoffe</td>
<td>Veranschaulicht die Verwendung des <a href="system-device-enumerator.md">Systemgeräte-Enumerators</a> zum Aufzählen von Geräten und Filtern.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">CutScene-Beispiel</a></td>
<td>Wiedergabe</td>
<td>Gibt eine Videodatei im Vollbildmodus wieder.</td>

</tr>
<tr class="even">
<td>DDrawXCL-Beispiel</td>
<td>Wiedergabe</td>
<td>Gibt Videos im exklusiven DirectDraw-Vollbildmodus mithilfe der <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo-Schnittstelle</strong></a> auf dem <a href="overlay-mixer-filter.md">Overlay-Mixer</a> wieder.</td>

</tr>
<tr class="odd">
<td>DShowPlayer-Beispiel</td>
<td>Wiedergabe</td>
<td>Videowiedergabeanwendung.</td>

</tr>
<tr class="even">
<td>EVRPlayer-Beispiel</td>
<td>Wiedergabe</td>
<td>Veranschaulicht die Verwendung des DirectShow EVR-Filters.
<blockquote>
[!Note]<br />
Erfordert Windows Vista oder höher.
</blockquote>
<br/> <br/> Dieses Beispiel ist im Windows SDK für Windows Server 2008 oder höher verfügbar.<br/></td>
<td>strmbase.lib</td>
</tr>
<tr class="odd">
<td>Texture3D9-Beispiel</td>
<td>Wiedergabe</td>
<td>Zeichnet Videos auf einer Microsoft DirectX 9.0-Texturoberfläche.</td>
<td>strmbase.lib, DirectX SDK</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Tickerbeispiel</a></td>
<td>VMR-9</td>
<td>Verwendet VMR-9 zum Mischen von Video und Text.</td>

</tr>
<tr class="odd">
<td>VMR9Allocator-Beispiel</td>
<td>VMR-9</td>
<td>Implementiert einen benutzerdefinierten Allocator-Presenter für VMR-9.</td>
<td>strmbase.lib</td>
</tr>
<tr class="even">
<td>VMR9Compositor-Beispiel</td>
<td>VMR-9</td>
<td>Implementiert einen benutzerdefinierten Mixer für VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">VMRPlayer-Beispiel</a></td>
<td>VMR-9</td>
<td>Verwendet VMR-9, um ein oder zwei ausgeführte Videos und ein statisches Image zu kombinieren.</td>

</tr>
<tr class="even">
<td>Wasserzeichenbeispiel</td>
<td>VMR-9</td>
<td>Blendet eine statische Bitmap während der Wiedergabe mithilfe von VMR-9 in ein Video ein.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Beispiel ohne Fenster</a></td>
<td>VMR-9</td>
<td>Veranschaulicht den fensterlosen Modus in VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Zusätzliche Abhängigkeiten

Einige Beispiele sind mit der DirectShow-Basisklassenbibliothek verknüpft. Um diese Beispiele zu erstellen, müssen Sie zuerst die Basisklassenbibliothek erstellen. Weitere Informationen finden Sie unter [DirectShow-Basisklassen.](directshow-base-classes.md) Die Basisklassenbibliothek ist für alle Beispielfilter erforderlich.

Einige beispiele erfordern zusätzlich zum Windows SDK auch das DirectX SDK. Zum Erstellen dieser Beispiele müssen Sie das DirectX SDK installieren und die Umgebungsvariable %DXSDK \_ DIR% auf ihren DirectX SDK-Installationspfad festlegen.

Viele der DirectShow-Beispiele verwenden eine Reihe allgemeiner Header und Quelldateien, die sich im Directrory \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow Common \\ befinden. Wenn Sie einen Beispielordner in ein anderes Verzeichnis kopieren, stellen Sie sicher, dass Sie auch den Ordner Common kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Buildumgebung](setting-up-the-build-environment.md)
</dt> </dl>

 

 





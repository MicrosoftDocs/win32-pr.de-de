---
description: DirectShow-Beispiele
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f58c10615aaaa4305a30934e32ef9b11efb18c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522544"
---
# <a name="directshow-samples"></a>DirectShow-Beispiele

Die DirectShow-Beispiele sind im [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)enthalten. Sie befinden sich unter dem Pfad \[ SDK Root \] \\ Samples \\ Multimedia \\ DirectShow.

In der folgenden Tabelle werden alle DirectShow-Beispiele aufgelistet, die in der Windows SDK bereitgestellt werden. Anweisungen zum Erstellen der Beispiele finden Sie in der Dokumentation, die im Windows SDK bereitgestellt wird.

Wenn eine zusätzliche Dokumentation für ein Beispiel vorhanden ist, wird in der ersten Spalte der Tabelle eine Verknüpfung mit der Tabelle angezeigt.



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
<th>BESCHREIBUNG</th>
<th>Zusätzliche Abhängigkeiten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">DirectShow-Basisklassen</a></td>
<td>Basisklassen Bibliothek</td>
<td>C++ Klassen und Hilfsfunktionen, die für die Implementierung von DirectShow-Filtern entwickelt wurden.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Amcap-Beispiel</a></td>
<td>Erfassung</td>
<td>Video Erfassungs Anwendung.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Dvapp-Beispiel</a></td>
<td>Erfassung</td>
<td>Digital Video (DV) Capture-Anwendung.</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Playcap-Beispiel</a></td>
<td>Erfassung</td>
<td>Einfache Erfassungs Anwendung.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO-Demo Beispiel</a></td>
<td>DMO</td>
<td>Streamt Audiodaten aus einer WAV-Datei über einen Audioeffekt-DMO.</td>
<td>DirectX SDK</td>
</tr>
<tr class="even">
<td>DVD-Beispiel</td>
<td>DVD</td>
<td>Veranschaulicht die grundlegende DVD-Wiedergabe und-Navigation sowie erweiterte Funktionen wie die Verwaltung auf Jugendebene, Lesezeichen, Karaoke und Befehls Synchronisierung.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Beispiel für einen inftee-Filter</a></td>
<td>Filter, Sonstiges</td>
<td>Beispiel Implementierung des Filters für die <a href="infinite-pin-tee-filter.md">unbegrenzte Pin</a> .</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Metronome-Filter Beispiel</a></td>
<td>Filter, Sonstiges</td>
<td>Zeigt, wie eine Referenzuhr implementiert wird.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Beispiel für PSI-Parser-Filter</a></td>
<td>Filter, Sonstiges</td>
<td>Empfängt Programm spezifische Informationstabellen (PSI) aus einem MPEG-2-Transportstream und extrahiert Programminformationen.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Dumpfilterbeispiel</a></td>
<td>Filter, Renderer</td>
<td>Schreibt die empfangene Medien Beispiele in eine Textdatei.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td>Sampvid-Filter</td>
<td>Filter, Renderer</td>
<td>Videorenderer-Filter.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Bereich Filter Beispiel</a></td>
<td>Filter, Renderer</td>
<td>Zeigt Audiodaten als Wellenformen an.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Beispiel für Async-Filter</a></td>
<td>Filter, Quelle</td>
<td>Datei Leser Filter, der progressiven Download unterstützt.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Beispiel für Ball Filter</a></td>
<td>Filter, Quelle</td>
<td>Der Video Quell Filter, der ein Bild eines Sprung-Balls erzeugt.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Beispiel für Push-Quell Filter</a></td>
<td>Filter, Quelle</td>
<td>Quell Filter, die die folgenden Daten als Videostream bereitstellen: eine einzelne Bitmap, eine Gruppe von Bitmaps, eine Kopie des aktuellen Desktop Bilds.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Beispiel für einen Synthesizer</a></td>
<td>Filter, Quelle</td>
<td>Quell Filter, der audiowaveforms generiert. In diesem Beispiel wird die dynamische Diagramm Bildung veranschaulicht.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">EZRGB24 Filter-Beispiel</a></td>
<td>Filter, Transformation</td>
<td>Bild Verarbeitungs Filter.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Gargle-Filter Beispiel</a></td>
<td>Filter, Transformation</td>
<td>Audioeffekt-Filter.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Beispiel für einen wavdest-Filter</a></td>
<td>Filter, Transformation</td>
<td>Schreibt einen Audiostream in eine WAV-Datei.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Dmuerum-Beispiel</a></td>
<td>Verschiedenes</td>
<td>Zeigt, wie Sie <a href="directx-media-objects.md">DirectX Media Objects</a> (DMOs) aufzählen.</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Mapper-Beispiel</a></td>
<td>Verschiedenes</td>
<td>Zeigt, wie Sie mit dem <a href="filter-mapper.md">Filter-Mapper</a> Filter in der Registrierung suchen.</td>

</tr>
<tr class="even">
<td>Sysenum-Beispiel</td>
<td>Verschiedenes</td>
<td>Veranschaulicht die Verwendung des <a href="system-device-enumerator.md">Enumerators "System Geräte</a> " zum Auflisten von Geräten und filtern.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Beispiel für Cutscene</a></td>
<td>Wiedergabe</td>
<td>Gibt eine Videodatei im Vollbildmodus wieder.</td>

</tr>
<tr class="even">
<td>Ddrawxcl-Beispiel</td>
<td>Wiedergabe</td>
<td>Gibt Video in DirectDraw exklusiv im Vollbildmodus mit der <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>iddrawexclmodevideo</strong></a> -Schnittstelle auf dem <a href="overlay-mixer-filter.md">Überlagerungs-Mischungs</a> Filter wieder.</td>

</tr>
<tr class="odd">
<td>Dshowplayer-Beispiel</td>
<td>Wiedergabe</td>
<td>Video Wiedergabe Anwendung.</td>

</tr>
<tr class="even">
<td>Evrplayer-Beispiel</td>
<td>Wiedergabe</td>
<td>Veranschaulicht, wie der DirectShow-EVR-Filter verwendet wird.
<blockquote>
[!Note]<br />
Erfordert Windows Vista oder höher.
</blockquote>
<br/> <br/> Dieses Beispiel ist im Windows SDK für Windows Server 2008 oder höher verfügbar.<br/></td>
<td>"ermbase. lib"</td>
</tr>
<tr class="odd">
<td>Texture3D9-Beispiel</td>
<td>Wiedergabe</td>
<td>Zeichnet Videos auf einer Microsoft DirectX 9,0-Textur Oberfläche.</td>
<td>"ermbase. lib", DirectX SDK</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Ticker-Beispiel</a></td>
<td>VMR-9</td>
<td>Verwendet VMR-9 zum Mischen von Video und Text.</td>

</tr>
<tr class="odd">
<td>VMR9Allocator-Beispiel</td>
<td>VMR-9</td>
<td>Implementiert einen benutzerdefinierten zuordnerpresenter für VMR-9.</td>
<td>"ermbase. lib"</td>
</tr>
<tr class="even">
<td>VMR9Compositor-Beispiel</td>
<td>VMR-9</td>
<td>Implementiert einen benutzerdefinierten Mixer für VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Vmrplayer-Beispiel</a></td>
<td>VMR-9</td>
<td>Verwendet VMR-9 zum Mischen von einem oder zwei laufenden Videos und ein statisches Bild.</td>

</tr>
<tr class="even">
<td>Wasserzeichen Beispiel</td>
<td>VMR-9</td>
<td>Mischt eine statische Bitmap bei der Wiedergabe mit VMR-9 in ein Video ein.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Fensterlose Stichprobe</a></td>
<td>VMR-9</td>
<td>Veranschaulicht den fensterlosen Modus in VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Zusätzliche Abhängigkeiten

Einige der Beispiele verknüpfen mit der DirectShow-Basisklassen Bibliothek. Um diese Beispiele zu erstellen, müssen Sie zunächst die Basisklassen Bibliothek erstellen. Weitere Informationen finden Sie unter [DirectShow-Basisklassen](directshow-base-classes.md). Die Basisklassen Bibliothek ist für alle Beispiel Filter erforderlich.

Einige Beispiele erfordern zusätzlich zum Windows SDK auch das DirectX SDK. Zum Erstellen dieser Beispiele müssen Sie das DirectX SDK installieren und die Umgebungsvariable% dxsdk \_ dir% auf Ihren DirectX SDK-Installationspfad festlegen.

Viele der DirectShow-Beispiele verwenden eine Reihe allgemeiner Header und Quelldateien, die sich in den Haupt \[ \] \\ Beispielen für \\ Multimedia \\ DirectShow von \\ directrory SDK befinden. Wenn Sie einen Beispiel Ordner in ein anderes Verzeichnis kopieren, stellen Sie sicher, dass Sie auch den gemeinsamen Ordner kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Buildumgebung](setting-up-the-build-environment.md)
</dt> </dl>

 

 





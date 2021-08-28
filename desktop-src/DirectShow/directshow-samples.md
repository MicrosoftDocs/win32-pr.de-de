---
description: DirectShow-Beispiele
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87687905d53f91339202af2b08bffa79902e100d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467357"
---
# <a name="directshow-samples"></a>DirectShow-Beispiele

Die DirectShow-Beispiele sind im Windows [SDK enthalten.](https://msdn.microsoft.com/windows/aa904949.aspx) Sie befinden sich unter dem Pfad \[ SDK Root Samples Multimedia \] \\ \\ \\ DirectShow.

In der folgenden Tabelle sind alle DirectShow-Beispiele aufgeführt, die im Windows SDK bereitgestellt werden. Anweisungen zum Erstellen der Beispiele finden Sie in der Dokumentation im Windows SDK.

Wenn es zusätzliche Dokumentation für ein Beispiel gibt, ist die erste Spalte dieser Tabelle damit verknüpft.




| Beispiel | Bereich | BESCHREIBUNG | Zusätzliche Abhängigkeiten | 
|--------|------|-------------|-------------------------|
| <a href="directshow-base-classes.md">DirectShow-Basisklassen</a> | Basisklassenbibliothek | C++-Klassen und Hilfsfunktionen, die für die Implementierung von DirectShow-Filtern entwickelt wurden. | 
| <a href="amcap-sample.md">AmCap-Beispiel</a> | Erfassung | Videoaufnahmeanwendung. | strmbase.lib | 
| <a href="dvapp-sample.md">DVApp-Beispiel</a> | Erfassung | Dv-Erfassungsanwendung (Digital Video). | 
| <a href="playcap-sample.md">PlayCap-Beispiel</a> | Erfassung | Einfache Erfassungsanwendung. | 
| <a href="dmo-demo-sample.md">DMO Demobeispiel</a> | DMO | Streams audio data from a WAV file through an audio effect DMO. | DirectX SDK | 
| DVD-Beispiel | DVD | Veranschaulicht die grundlegende DVD-Wiedergabe und -Navigation sowie erweiterte Features wie Verwaltung auf Elternebene, Lesezeichen, Synchronisierung und Befehlssynchronisierung. | 
| <a href="inftee-filter-sample.md">InfTee-Filterbeispiel</a> | Filter, sonstige | Beispielimplementierung des <a href="infinite-pin-tee-filter.md">Filters Infinite Pin Tee.</a> | strmbase.lib | 
| <a href="metronome-filter-sample.md">Beispiel für Metronomfilter</a> | Filter, sonstige | Zeigt, wie eine Verweisuhr implementiert wird. | strmbase.lib | 
| <a href="psi-parser-filter-sample.md">BEISPIEL FÜR PSI-Parserfilter</a> | Filter, sonstige | Empfängt PSI-Tabellen (Program Specific Information) aus einem MPEG-2-Transportstream und extrahiert Programminformationen. | strmbase.lib | 
| <a href="dump-filter-sample.md">Beispiel für Dumpfilter</a> | Filter, Renderer | Schreibt Medienbeispiele in eine Textdatei. | strmbase.lib | 
| SampVid-Filter | Filter, Renderer | Videorendererfilter. | strmbase.lib | 
| <a href="scope-filter-sample.md">Beispiel für Bereichsfilter</a> | Filter, Renderer | Zeigt Sounddaten als Wellenformen an. | strmbase.lib | 
| <a href="async-filter-sample.md">Beispiel für asynchrone Filter</a> | Filter, Quelle | Dateilesefilter, der progressiven Download unterstützt. | strmbase.lib | 
| <a href="ball-filter-sample.md">Beispiel für Den Ballfilter</a> | Filter, Quelle | Videoquellenfilter, der ein Bild einer Bouncing-Kugel erzeugt. | strmbase.lib | 
| <a href="push-source-filters-sample.md">Beispiel für Pushquellenfilter</a> | Filter, Quelle | Quellfilter, die die folgenden Daten als Videostream bereitstellen: eine einzelne Bitmap, eine Gruppe von Bitmaps, eine Kopie des aktuellen Desktopbilds. | strmbase.lib | 
| <a href="synth-filter-sample.md">Synth-Filterbeispiel</a> | Filter, Quelle | Quellfilter, der Audio waveforms generiert. In diesem Beispiel wird die dynamische Graph-Entwicklung veranschaulicht. | strmbase.lib | 
| <a href="ezrgb24-filter-sample.md">EZRGB24-Filterbeispiel</a> | Filter, Transformieren | Bildverarbeitungsfilter. | strmbase.lib | 
| <a href="gargle-filter-sample.md">Gargle-Filterbeispiel</a> | Filter, Transformieren | Filter für Audioeffekt. | strmbase.lib | 
| <a href="wavdest-filter-sample.md">WavDest-Filterbeispiel</a> | Filter, Transformieren | Schreibt einen Audiostream in eine WAV-Datei. | strmbase.lib | 
| <a href="dmoenum-sample.md">DMOEnum-Beispiel</a> | Sonstiges | Zeigt, wie <a href="directx-media-objects.md">DirectX-Medienobjekte (DMOs)</a> aufzählt werden. | 
| <a href="mapper-sample.md">Mapper-Beispiel</a> | Sonstiges | Zeigt, wie Der <a href="filter-mapper.md">Filter-Mapper verwendet wird,</a> um Filter in der Registrierung zu suchen. | 
| SysEnum-Beispiel | Sonstiges | Veranschaulicht die Verwendung des <a href="system-device-enumerator.md">Systemgeräte-Enumerators</a> zum Aufzählen von Geräten und Filtern. | 
| <a href="cutscene-sample.md">CutScene-Beispiel</a> | Wiedergabe | Gibt eine Videodatei im Vollbildmodus wieder. | 
| DDrawXCL-Beispiel | Wiedergabe | Gibt Videos im exklusiven DirectDraw-Vollbildmodus mithilfe der <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo-Schnittstelle</strong></a> auf dem <a href="overlay-mixer-filter.md">Overlay-Mixer</a> wieder. | 
| DShowPlayer-Beispiel | Wiedergabe | Videowiedergabeanwendung. | 
| EVRPlayer-Beispiel | Wiedergabe | Veranschaulicht die Verwendung des DirectShow EVR-Filters.<blockquote>[!Note]<br />Erfordert Windows Vista oder höher.</blockquote><br /><br /> Dieses Beispiel ist im Windows SDK für Windows Server 2008 oder höher verfügbar.<br /> | strmbase.lib | 
| Texture3D9-Beispiel | Wiedergabe | Zeichnet Video auf einer Microsoft DirectX 9.0-Texturoberfläche. | strmbase.lib, DirectX SDK | 
| <a href="ticker-sample.md">Tickerbeispiel</a> | VMR-9 | Verwendet VMR-9, um Video und Text zu mischen. | 
| VMR9Allocator-Beispiel | VMR-9 | Implementiert einen benutzerdefinierten Allocator-Presenter für VMR-9. | strmbase.lib | 
| VMR9Compositor-Beispiel | VMR-9 | Implementiert einen benutzerdefinierten Mixer für VMR-9. | 
| <a href="vmrplayer-sample.md">VMRPlayer-Beispiel</a> | VMR-9 | Verwendet VMR-9, um ein oder zwei ausgeführte Videos und ein statisches Image zu mischen. | 
| Beispiel für Wasserzeichen | VMR-9 | Blendt eine statische Bitmap während der Wiedergabe mithilfe von VMR-9 in ein Video ein. | 
| <a href="windowless-sample.md">Beispiel ohne Fenster</a> | VMR-9 | Veranschaulicht den fensterlosen Modus in VMR-9. | 




 

## <a name="additional-dependencies"></a>Zusätzliche Abhängigkeiten

Einige beispiele sind mit der DirectShow-Basisklassenbibliothek zu verknüpfen. Um diese Beispiele zu erstellen, müssen Sie zuerst die Basisklassenbibliothek erstellen. Weitere Informationen finden Sie unter [DirectShow-Basisklassen.](directshow-base-classes.md) Die Basisklassenbibliothek ist für alle Beispielfilter erforderlich.

Einige der Beispiele erfordern zusätzlich zum Windows SDK auch das DirectX SDK. Um diese Beispiele zu erstellen, müssen Sie das DirectX SDK installieren und die Umgebungsvariable %DXSDK DIR% auf den Installationspfad Ihres \_ DirectX SDK festlegen.

Viele der DirectShow-Beispiele verwenden eine Reihe von allgemeinen Headern und Quelldateien, die sich im DirectShow Common-Beispiel für directrory \[ SDK Root Samples Multimedia \] \\ \\ \\ \\ befinden. Wenn Sie einen Beispielordner in ein anderes Verzeichnis kopieren, stellen Sie sicher, dass Sie auch den Ordner Common kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Buildumgebung](setting-up-the-build-environment.md)
</dt> </dl>

 

 





---
description: DVD-Anwendungen
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341849"
---
# <a name="dvd-applications"></a>DVD-Anwendungen

DirectShow stellt eine Komponente namens " [DVD Navigator](dvd-navigator-filter.md) Source Filter" bereit, die DVD-Navigationsaufgaben in C++ vereinfacht. Der DVD-Navigator bietet alle Funktionen, die Sie auf einem eigenständigen DVD-Player mit vollem Funktionsumfang finden, sowie zusätzliche Funktionen, die für die Wiedergabe von DVDs auf persönlichen Computern spezifisch sind. Mit dem DVD-Navigator können C++-und Skriptentwickler mit voll funktionsfähigen DVD-Anwendungen erstellen, ohne auf die DVD-Spezifikation zu verweisen. Der DVD-Navigator übernimmt in Verbindung mit den decoderfiltern auch die regionale Verwaltung und den Schutz vor Urheberrechten (CSS-und analoger Kopierschutz) und isoliert die Anwendungsentwickler von diesen Details.

Der Filter für den DVD-Navigator funktioniert auf einem gesamten DVD-Video Volume, das aus den Dateien im Verzeichnis "Video TS" besteht \_ . Im Gegensatz zu den meisten DirectShow-Quell filtern, die mit einzelnen Streams oder Dateien arbeiten, verwendet der DVD-Navigator die DVD-Video Struktur von Titeln, Kapiteln und Zeit Codes. Entwickler, die einzelne MPEG-2-Dateien in DirectShow wiedergeben möchten, sollten den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) anstelle des DVD-Navigator-Filters verwenden. Weitere Informationen finden Sie [unter MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md) .

> [!Note]  
> Zum Abspielen von DVDs muss der Benutzer über einen MPEG-2-Decoder verfügen.

 

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Features der DVD-Unterstützung in DirectShow](dvd-support-features-in-directshow.md)
-   [DVD-Grundlagen](dvd-basics.md)
-   [Entwickeln des DVD-Filter Diagramms](building-the-dvd-filter-graph.md)
-   [Abrufen der DVD-Schnittstellen Zeiger](obtaining-the-dvd-interface-pointers.md)
-   [DVD-Befehle](dvd-commands.md)
-   [Identifizieren gültiger DVD-Vorgänge](identifying-valid-dvd-operations.md)
-   [Synchronisieren von DVD-Befehlen](synchronizing-dvd-commands.md)
-   [Datenfluss im DVD-Navigator](data-flow-in-the-dvd-navigator.md)
-   [Behandeln von DVD-Ereignis Benachrichtigungen](handling-dvd-event-notifications.md)
-   [Arbeiten mit DVD-Menüs](working-with-dvd-menus.md)
-   [Audiodaten Ströme](audio-and-subpicture-streams.md)
-   [Erzwingen von Eltern Verwaltungsebenen](enforcing-parental-management-levels.md)
-   [Speichern und Wiederherstellen von dvdstate-Objekten](saving-and-restoring-dvdstate-objects.md)
-   [Arbeiten mit DVD-Text Zeichenfolgen](working-with-dvd-text-strings.md)
-   [Wiedergabe von Karaoke-Audiostreams](playing-karaoke-audio-streams.md)
-   [Behandlung von Disc-ejections](handling-disc-ejections.md)
-   [Erweiterungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Konfiguration des DVD-Filter Diagramms](dvd-filter-graph-configuration.md)
-   [Verknüpfungen zu C++-DVD-Referenzseiten](shortcuts-to-c-dvd-reference-pages.md)

Verweise auf die Entwicklung von DVD/MPEG2-Decodern finden Sie unter [DVD-decoderentwicklung in DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 




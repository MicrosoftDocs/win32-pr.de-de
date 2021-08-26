---
description: DVD-Anwendungen
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102960"
---
# <a name="dvd-applications"></a>DVD-Anwendungen

DirectShow stellt eine Komponente namens [DVD Navigator-Quellfilter](dvd-navigator-filter.md) bereit, die DVD-Navigationsaufgaben in C++ vereinfacht. Der DVD-Navigator verfügt über alle Funktionen, die Sie in einem eigenständigen DVD-Player mit vollem Funktionsumfang finden, sowie zusätzliche Funktionen, die speziell für die Wiedergabe von DVDs auf PCs spezifisch sind. Mit dem DVD-Navigator können C++- und Skriptentwickler dvd-Anwendungen mit vollem Funktionsumfang erstellen, ohne auf die DVD-Spezifikation zu verweisen. Der DVD-Navigator kümmert sich in Abstimmung mit den Decoderfiltern auch um die regionale Verwaltung und den Urheberrechtsschutz (CSS und analoger Kopierschutz), der Anwendungsentwickler von diesen Details abkoordiniert.

Der DVD Navigator-Filter funktioniert über ein gesamtes DVD-Video Volume, das aus den Dateien im Verzeichnis VIDEO \_ TS besteht. Im Gegensatz zu den meisten DirectShow-Quellfiltern, die mit einzelnen Streams oder Dateien funktionieren, verwendet der DVD-Navigator die DVD-Video Struktur von Titeln, Kapiteln und Zeitcodes. Entwickler, die einzelne MPEG-2-Dateien in DirectShow wiedergeben möchten, sollten den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) anstelle des DVD Navigator-Filters verwenden. Weitere Informationen finden Sie [unter MPEG-2-Unterstützung in DirectShow.](mpeg-2-support-in-directshow.md)

> [!Note]  
> Um DVDs wiedergeben zu können, muss der Benutzer über einen MPEG-2-Decoder verfügen.

 

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [DVD-Unterstützungsfunktionen in DirectShow](dvd-support-features-in-directshow.md)
-   [DVD-Grundlagen](dvd-basics.md)
-   [Erstellen der DVD-Filter-Graph](building-the-dvd-filter-graph.md)
-   [Abrufen der DVD-Schnittstellenzeiger](obtaining-the-dvd-interface-pointers.md)
-   [DVD-Befehle](dvd-commands.md)
-   [Identifizieren gültiger DVD-Vorgänge](identifying-valid-dvd-operations.md)
-   [Synchronisieren von DVD-Befehlen](synchronizing-dvd-commands.md)
-   [Daten Flow im DVD-Navigator](data-flow-in-the-dvd-navigator.md)
-   [Behandeln von DVD-Ereignisbenachrichtigungen](handling-dvd-event-notifications.md)
-   [Arbeiten mit DVD-Menüs](working-with-dvd-menus.md)
-   [Audio und Subpicture Streams](audio-and-subpicture-streams.md)
-   [Erzwingen der Verwaltungsebenen von Eltern](enforcing-parental-management-levels.md)
-   [Speichern und Wiederherstellen von DvdState-Objekten](saving-and-restoring-dvdstate-objects.md)
-   [Arbeiten mit DVD-Textzeichenfolgen](working-with-dvd-text-strings.md)
-   [Wiedergeben von Audio Streams](playing-karaoke-audio-streams.md)
-   [Behandeln von Auswerfen von Datenträgern](handling-disc-ejections.md)
-   [Verbesserungen bei der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [KONFIGURATION DES DVD-Filters Graph](dvd-filter-graph-configuration.md)
-   [Verknüpfungen zu C++-DVD-Referenzseiten](shortcuts-to-c-dvd-reference-pages.md)

Verweise zur DVD/MPEG2-Decoderentwicklung finden Sie unter [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 




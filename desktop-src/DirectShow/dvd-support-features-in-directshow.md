---
description: Features der DVD-Unterstützung in DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Features der DVD-Unterstützung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035af51bbe44ec8dcc95f199c502b71d37d834f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345402"
---
# <a name="dvd-support-features-in-directshow"></a>Features der DVD-Unterstützung in DirectShow

Die Funktionalität des [DVD-Navigator](dvd-navigator-filter.md) -Filters wird über zwei Schnittstellen verfügbar gemacht, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), die die "Set"-Methoden für den DVD-Navigator bereitstellt, und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), die die "Get"-Methoden bereitstellt.

Der DVD-Navigator unterstützt die folgenden Features:

-   Karaoke-Unterstützung: Sie können eine DVD-Karaoke-Anwendung mit dem DVD-Navigator schreiben. (Hierfür ist ein kompatibler Decoder erforderlich.)
-   Vereinfachter Zugriff auf DVD-Text Informations Zeichenfolgen: der DVD-Navigator analysiert diese Zeichen folgen und ermöglicht Anwendungen das einfache auflisten, identifizieren und Abrufen dieser Zeichen folgen.
-   Audiovolumensteuerung über [ **ibasicaudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Unterstützung für das Anpassen des Verhaltens des DVD-Navigators, wenn der Befehl zum Beenden ausgegeben wird: Anwendungen können den DVD-Navigator anweisen, beim Neustart des Filter Diagramms von der aktuellen Position fortzufahren, oder die Wiedergabe vom Anfang der CD aus auszuführen.
-   Unterstützung von Digital Theater Systems (DTS) und der Unterstützung von Dynamic Digital Sound (SDDS) von Dynamic. DTS-und SDDS-Audiodatenströme werden vom DVD-Navigator erkannt und an den Audiodecoder übermittelt. (Ein Drittanbieter-DTS-kompatibler oder SDDS-kompatibler Decoder ist erforderlich, um die Audiodatei zu decodieren und wiederzugeben.)
-   Verbesserte Unterstützung für Änderungen auf Jugendebene: der DVD-Navigator ermöglicht es einer Anwendung, Änderungs Befehle auf Jugendebene von der Festplatte zu akzeptieren, abzulehnen oder zu ignorieren.
-   Erweiterte Optionen zum Verwalten des Status des DVD-Navigators und Synchronisieren von Befehlen
-   Unterstützung für Frame-Step, Frame-genaues Suchen und umgekehrte Wiedergabe. Diese Features erfordern einen Video Decoder, der Sie unterstützt.
-   Die Möglichkeit, die aktuelle Position in einem Titel zu speichern und zu einem beliebigen Zeitpunkt zurückzukehren.
-   Vereinfachte Unterstützung von Zeit Ereignissen in nicht sequenziellen PGC-Titeln: bei nicht sequenziellen PGC-Titeln leitet der DVD-Navigator die rohzeit Code Informationen an die Anwendung weiter.
-   Zeit Code Informationen. Anstelle des Binary Coded Decimal (BCD)-Formats kann die [**DVD- \_ hmsf- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) Struktur verwendet werden. **DVD \_ Der hmsf- \_ Timecode** enthält problemlos zugriffene Member für Stunden, Minuten, Sekunden und Frames und kann in einen **ulong**-Wert umgewandelt werden.
-   Die Möglichkeit, zu steuern, ob das Filter Diagramm nach einem Suchvorgang geleert wird: die Diagramm Puffer können zu einem beliebigen Zeitpunkt bis zu einigen Sekunden Videos enthalten. Sie können das Diagramm anweisen, die Wiedergabe des gepufferten Videos nach einer Suche abzuschließen, oder direkt am neuen Speicherort zu spielen.
-   Die Möglichkeit, Werte in allgemeinen Parameter Registern festzulegen: ein erweitertes Feature für diejenigen, die mit der DVD-Spezifikation vertraut sind, die erweiterte Funktionalität implementieren möchten.
-   Die Möglichkeit, numerische Festplatten Bezeichner zu generieren, die für alle praktischen Zwecke eindeutig sind

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Welchen Hintergrund benötige ich zum Schreiben einer DVD-Anwendung?

Alle Anwendungsentwickler sollten eine grundlegende Vertrautheit mit den Funktionen von DVD-Technologie haben, wie z. b. Jugend Verwaltungsebenen, mehreren Audio-und teilbildstreams und Winkel Blöcken. In den [DVD-Grundlagen](dvd-basics.md) werden die einzelnen Features kurz beschrieben. Ausführlichere Beschreibungen sind in Veröffentlichungen von Drittanbietern verfügbar. Sie müssen nicht auf die DVD-Spezifikation verweisen, es sei denn, Sie beabsichtigen, erweiterte Funktionen zu implementieren, die über den Befehlssatz der Anlage J hinausgehen

C/C++-Entwickler, die DirectShow verwenden, sollten mit com-Client Programmiertechniken vertraut sein, z. b. das Erstellen von COM-Objekten und das Abrufen und Freigeben von com Möglicherweise benötigen Sie auch allgemeine Kenntnisse über Filter Diagramm Vorgänge, da Sie möglicherweise direkt auf das Diagramm zugreifen und es bearbeiten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 




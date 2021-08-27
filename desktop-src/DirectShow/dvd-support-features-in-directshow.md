---
description: DVD-Unterstützungsfeatures in DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: DVD-Unterstützungsfeatures in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107900"
---
# <a name="dvd-support-features-in-directshow"></a>DVD-Unterstützungsfeatures in DirectShow

Die Funktionalität des [DVD-Navigatorfilters](dvd-navigator-filter.md) wird über die beiden Schnittstellen [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)verfügbar gemacht, die die "set"-Methoden für den DVD-Navigator und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)zur Verfügung stellen, die die Get-Methoden zur Verfügung stellen.

Der DVD-Navigator unterstützt die folgenden Features:

-   Unterstützung von Dvd: Sie können eine DVD-Dvd-Anwendung mithilfe des DVD-Navigators schreiben. (Dies erfordert einen kompatiblen Decoder.)
-   Vereinfachter Zugriff auf DVD-Textinformationszeichenfolgen: Der DVD-Navigator analysiert diese Zeichenfolgen und ermöglicht Anwendungen das einfache Aufzählen, Identifizieren und Abrufen dieser Zeichenfolgen.
-   Audio-Lautstärkesteuerung über [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Unterstützung für das Anpassen des Verhaltens des DVD-Navigators, wenn der Befehl Beenden ausgegeben wird: Anwendungen können den DVD-Navigator anweisen, entweder beim Neustart des Filterdiagramms vom aktuellen Speicherort aus weiter zu starten oder die Wiedergabe vom Anfang des Datenträgers aus zu starten.
-   Unterstützung von DIGITAL DIGITAL SYSTEMS -Audio (DTS) und SdDS-Audio (Dynamic Digital Sound). DTS- und SDDS-Audiostreams werden vom DVD-Navigator erkannt und an den Audiodecoder übergeben. (Ein DTS-kompatibler oder SDDS-kompatibler Decoder eines Drittanbieters ist erforderlich, um die Audiodaten zu decodieren und wieder zu spielen.)
-   Verbesserte Unterstützung für Änderungen auf Elternebene: Der DVD-Navigator ermöglicht einer Anwendung das Akzeptieren, Ablehnen oder Ignorieren von Änderungsbefehlen auf Elternebene vom Datenträger.
-   Erweiterte Optionen zum Verwalten des Status des DVD-Navigators und zum Synchronisieren von Befehlen
-   Unterstützung für Frameschritte, framegenaue Such- und Umgekehrte Wiedergabe. Diese Features erfordern einen Videodecoder, der sie unterstützt.
-   Die Möglichkeit, den aktuellen Speicherort in einem Titel zu speichern und jederzeit an ihn zurückzukehren.
-   Vereinfachte Unterstützung für Zeitereignisse in nicht sequenziellen PGC-Titeln: Bei nicht sequenziellen PGC-Titeln leitet der DVD-Navigator die Unformatierten Zeitcodeinformationen an die Anwendung weiter.
-   Zeitcodeinformationen. Die [**\_ HMSF-TIMECODE-Struktur \_**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) der DVD kann statt des Binärformats für codierte Dezimalzahlen (Binary Coded Decimal, BCD) verwendet werden. **DVD \_ HMSF \_ TIMECODE** enthält einfach zugängliche Member für Stunden, Minuten, Sekunden und Frames und kann in bzw. aus **einem ULONG--Code umge castiert werden.**
-   Die Möglichkeit, zu steuern, ob das Filterdiagramm nach einem Suchvorgang geleert wird: Die Graphpuffer können zu einem bestimmten Zeitpunkt bis zu ein paar Sekunden Video enthalten. Sie können den Graphen anweisen, die Wiedergabe des gepufferten Videos nach einer Suche zu beenden oder sofort an der neuen Position zu spielen.
-   Die Möglichkeit zum Festlegen von Werten in allgemeinen Parameterregistern: Ein erweitertes Feature für diejenigen, die mit der DVD-Spezifikation vertraut sind und erweiterte Funktionen implementieren möchten.
-   Die Möglichkeit, numerische Datenträgerbezeichner zu generieren, die für alle praktischen Zwecke eindeutig sind

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Welchen Hintergrund muss ich zum Schreiben einer DVD-Anwendung haben?

Alle Anwendungsentwickler sollten über grundlegende Vertrautheit mit den Features der DVD-Technologie verfügen, z. B. auf Ebene der Elternverwaltung, mehreren Audio- und Unterbildstreams und Winkelblöcken. [In den DVD-Grundlagen](dvd-basics.md) wird jedes dieser Features kurz beschrieben. Vollständigere Beschreibungen finden Sie in Drittanbieterveröffentlichungen. Sie müssen nicht auf die DVD-Spezifikation verweisen, es sei denn, Sie beabsichtigen, erweiterte Features über den Anhang J-Befehlssatz hinaus zu implementieren.

C/C++-Entwickler, die DirectShow verwenden, sollten mit COM-Clientprogrammierungstechniken wie dem Erstellen von COM-Objekten und dem Abrufen und Freigeben von COM-Schnittstellenze0ern vertraut sein. Möglicherweise benötigen Sie auch allgemeine Kenntnisse zu Filterdiagrammvorgängen, da Sie möglicherweise direkt auf den Graphen zugreifen und ihn bearbeiten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 




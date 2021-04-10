---
description: Datenfluss für Filter Entwickler
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Datenfluss für Filter Entwickler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041298"
---
# <a name="data-flow-for-filter-developers"></a>Datenfluss für Filter Entwickler

In diesem Abschnitt wird ausführlich beschrieben, wie Daten durch das Filter Diagramm verschoben werden. Der Schwerpunkt liegt auf dem lokalen Speicher Transport mithilfe der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -oder [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle. Es ist für Entwickler gedacht, die eigene benutzerdefinierte Filter schreiben. Eine allgemeine Einführung in die Verarbeitung von Daten Flüssen durch Microsoft DirectShow finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).

Viele Daten durchlaufen ein Filter Diagramm. Es fällt ungefähr in zwei Kategorien: Mediendaten und Steuerungsdaten. Im Allgemeinen werden Mediendaten nach unten durchlaufen, und Steuerungsdaten werden im Upstream übertragen. Zu den Mediendaten gehören Video Frames, Audiobeispiele, MPEG-Pakete usw., die einen Stream bilden, aber auch Leerungs Befehle, Dateiende-Benachrichtigungen und andere Daten, die mit dem Stream übertragen werden. Steuerungsdaten sind nicht Teil des Mediendaten Stroms. Beispiele für Steuerungsdaten sind Qualitäts Steuerungsanforderungen und Such Befehle.

Dieser Abschnitt enthält die folgenden Artikel:

-   [Bereitstellung von Beispielen](delivering-samples.md)
-   [Verarbeiten von Daten](processing-data.md)
-   [Streamende-Benachrichtigungen](end-of-stream-notifications.md)
-   [Neue Segmente](new-segments.md)
-   [Lak](flushing.md)
-   [Diejenigen](seeking.md)
-   [Dynamische Format Änderungen](dynamic-format-changes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualitäts Steuerungs Verwaltung](quality-control-management.md)
</dt> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




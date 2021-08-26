---
description: DirectShow-Videoerfassungsfilter
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow-Videoerfassungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cafe2815376ddb2a099c309228ba1bf24ae9315f305edb7312b88dd1196f82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966330"
---
# <a name="directshow-video-capture-filters"></a>DirectShow-Videoerfassungsfilter

Erfassungsfilter in DirectShow verfügen über einige Features, die sie von anderen Arten von Filtern unterscheiden. Obwohl [der Capture Graph Builder](capture-graph-builder.md) viele der Details ausblendet, ist es eine gute Idee, diesen Abschnitt zu lesen, um ein allgemeines Verständnis von DirectShow-Erfassungsdiagrammen zu erhalten.

**Anheften von Kategorien**

Ein Erfassungsfilter verfügt häufig über zwei oder mehr Ausgabepins, die die gleiche Art von Daten liefern, z. B. einen Vorschaupin und einen Aufnahmepin. Daher sind Medientypen keine gute Möglichkeit, die Stecknadeln zu unterscheiden. Stattdessen unterscheiden sich die Stecknadeln durch ihre Funktionalität, die mithilfe einer GUID identifiziert wird, die als *Stecknadelkategorie bezeichnet wird.*

Eine Diskussion über das Abfragen von Pins für ihre Kategorie finden Sie unter [Working with Pin Categories](working-with-pin-categories.md). Für die meisten Anwendungen müssen Sie Pins jedoch nicht direkt abfragen. Stattdessen übernehmen verschiedene [**ICaptureGraphBuilder2-Methoden**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Parameter, die die Pinkategorie angeben, für die der Betrieb durchgeführt werden soll. Der Capture Graph Builder sucht automatisch den richtigen Pin.

**Vorschau von Pins und Erfassungspins**

Einige Videoaufnahmegeräte verfügen über separate Ausgabepins für Vorschau und Erfassung. Der Vorschaupin wird verwendet, um Videos auf dem Bildschirm zu rendern, während der Aufnahmepin verwendet wird, um Videos in eine Datei zu schreiben.

Ein Vorschaupin und ein Aufnahmepin haben die folgenden Unterschiede:

-   Ein Vorschaupin löscht Frames nach Bedarf, um den Durchsatz auf dem Erfassungspin zu erhalten.
-   Jeder Frame eines Aufnahmepins wird mit dem Zeitstempel der Streamzeit versehen, zu der der Frame erfasst wurde. Ein Vorschaupin nimmt keinen Zeitstempel für die von ihm zu liefernden Beispiele vor.

Der Grund dafür, dass Vorschauframes keine Zeitstempel haben, ist, dass das Filterdiagramm eine geringe Latenz in den Stream einfing. Wenn die Erfassungszeit als Präsentationszeit verwendet wird, behandelt der Videorenderer jedes Beispiel als etwas spät. Dies kann dazu führen, dass der Videorenderer Frames verdrungen, während er versucht, den Aufholbedarf zu finden. Durch das Entfernen der Zeitstempel wird sichergestellt, dass der Renderer jedes Beispiel beim Eintreffen zeigt, ohne Frames zu löschen.

Die Pinkategorie für Vorschaupins ist PIN \_ CATEGORY \_ PREVIEW. Die Kategorie für Erfassungspins ist PIN \_ CATEGORY \_ CAPTURE.

**Videoport-Pins**

Ein Videoport ist eine Hardwareverbindung zwischen einem Videogerät (z. B. einem analogen TV-Tuner) und der Grafikkarte. Mit einem Videoport kann das Gerät Videodaten direkt an die Grafikkarte senden. Das Video wird auf dem Bildschirm mithilfe einer Hardwareüberlagerung angezeigt. Ein Videoport kann ein tatsächliches Kabel sein, das zwei Geräte auf separaten Karten verbindet. Oder es kann sich um eine festverkabelte Verbindung auf derselben Karte geben.

Der Vorteil eines Videoports ist, dass das Video direkt in den Videospeicher übergeht, ohne dass die CPU arbeitet. Videoports haben jedoch einige Nachteile:

-   Ein Videoport verwendet während der Erfassung immer die Überlagerungsoberfläche, unabhängig davon, ob Sie eine Vorschau des Videos anzeigen möchten.
-   Das Kippen zwischen Frames erfolgt automatisch, wodurch es schwierig ist, den Flip mit anderen Videovorgängen zu synchronisieren.

Wenn ein Aufnahmegerät einen Videoport verwendet, verfügt der Erfassungsfilter über einen Videoportanschluss und nicht über einen Vorschaupin. Die Pinkategorie für Videoportpins ist PIN \_ CATEGORY \_ VIDEOPORT.

Jeder Erfassungsfilter verfügt über mindestens einen Aufnahmepin. Darüber hinaus kann es einen Vorschaupin oder einen Videoportanschluss geben, aber nie beides. Filter können über mehrere Aufnahmepins und Vorschaupins verfügen, die jeweils einen separaten Medientyp bereitstellen. Daher kann ein einzelner Filter einen Videoaufnahmepin, einen Pin für die Videovorschau, einen Audioaufnahmepin und einen Audiovorschaupin haben. (Es gibt jedoch nichts, was einem Videoport für Audiodaten entspricht.)

**WDM-Upstreamfilter**

Windows Treibermodellgeräte (WDM) erfordern möglicherweise einige zusätzliche Filter vor dem Erfassungsfilter. Diese Filter umfassen Folgendes:

-   [TV Tuner Filter](tv-tuner-filter.md). Steuert die Optimierung für analoge TV-Tuner.
-   [TV-Audiofilter](tv-audio-filter.md). Steuert Audioeinstellungen für analoge TV-Tuner.
-   [Analog Video Crossbar Filter](analog-video-crossbar-filter.md). Leitet Video- und Audiosignale über das Hardwaregerät weiter. Beispielsweise kann ein Gerät über mehrere Eingaben verfügen, z. B. S-Video und zusammengesetztes Video. Mit dem Kreuzleistenfilter kann die Anwendung die Eingabe auswählen.

Obwohl es sich hierbei um separate Filter in DirectShow handelt, stellen sie in der Regel dasselbe Hardwaregerät dar. Jeder Filter steuert eine andere Funktion des Geräts. Die Filter sind durch Stecknadeln verbunden, aber keine Mediendaten werden über die Stecknadelverbindungen bewegt. Aus diesem Grund stellen die Stecknadeln dieser Filter keine Verbindung durch Festlegen eines Medientyps wieder. Stattdessen verwenden sie GUID-Werte, die als *mittel bezeichnet werden.* Mittlere GUIDs werden für einen bestimmten Geräte-Minitreiber eindeutig definiert. Beispielsweise unterstützen der FILTER TV Tuner und der Video Capture-Filter für dieselbe TV-Karte das gleiche Medium, wodurch die Anwendung das Diagramm ordnungsgemäß erstellen kann.

In der Praxis werden diese Filter automatisch dem Diagramm hinzugefügt, solange Sie **ICaptureGraphBuilder2** zum Erstellen Ihrer Erfassungsdiagramme verwenden. Eine ausführlichere Erläuterung finden Sie unter [WDM-Klassentreiberfilter](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Videoaufnahme in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 




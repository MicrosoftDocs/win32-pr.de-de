---
description: DirectShow-Video Erfassungs Filter
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow-Video Erfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480875"
---
# <a name="directshow-video-capture-filters"></a>DirectShow-Video Erfassungs Filter

Erfassungs Filter in DirectShow verfügen über einige Funktionen, die Sie von anderen Arten von Filtern unterscheiden. Obwohl der [Erfassungs Diagramm](capture-graph-builder.md) -Generator viele der Details verbirgt, empfiehlt es sich, diesen Abschnitt zu lesen, um ein allgemeines Verständnis von DirectShow-Erfassungs Diagrammen zu erhalten.

**PIN-Kategorien**

Ein Erfassungs Filter verfügt häufig über zwei oder mehr Ausgabe Pins, die dieselbe Art von Daten bereitstellt, z. –. eine Vorschau-PIN und eine Aufzeichnungs-PIN. Aus diesem Grund sind Medientypen keine gute Methode, um die Pins zu unterscheiden. Stattdessen werden die Pins durch ihre Funktionalität unterschieden, die mithilfe einer GUID identifiziert wird, die als *Pin-Kategorie* bezeichnet wird.

Eine Erläuterung zum Abfragen von Pins für Ihre Kategorie finden Sie unter [Arbeiten mit PIN-Kategorien](working-with-pin-categories.md). Bei den meisten Anwendungen müssen Pins jedoch nicht direkt abgefragt werden. Stattdessen verwenden verschiedene [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Methoden Parameter, die die anzuarbeitende Pin-Kategorie angeben. Der Erfassungs Diagramm-Generator wird automatisch nach der richtigen PIN fest.

**Pins für Vorschau und Erfassung**

Einige Video Erfassungsgeräte verfügen über separate Ausgabe Pins für Vorschau und Erfassung. Die Vorschau-PIN wird zum Rendering von Videos auf dem Bildschirm verwendet, während die Erfassungs-PIN zum Schreiben von Videos in eine Datei verwendet wird.

Eine Vorschau-PIN und eine Aufzeichnungs-PIN haben die folgenden Unterschiede:

-   Eine Vorschau-Pin löscht Frames nach Bedarf, um den Durchsatz auf der Erfassungs-Pin aufrechtzuerhalten.
-   Jedem Frame aus einer Aufzeichnungs-PIN wird ein Zeitstempel mit der streamzeit angezeigt, zu der der Rahmen aufgezeichnet wurde. Eine Vorschau-Pin hat keine Zeitstempel für die von ihr bereitgestellten Beispiele.

Der Grund dafür, dass Vorschau Rahmen nicht über Zeitstempel verfügen, besteht darin, dass das Filter Diagramm eine kleine Menge an Latenz in den Datenstrom einführt. Wenn die Erfassungs Zeit als Präsentationszeit verwendet wird, behandelt der Videorenderer jede Stichprobe als etwas spät. Dies kann bewirken, dass der Videorenderer Frames abfängt, während er versucht, den Vorgang zu wiederholen. Durch das Entfernen der Zeitstempel wird sichergestellt, dass der Renderer die einzelnen Beispiele beim Eintreffen anzeigt, ohne Frames zu verwerfen.

Die PIN-Kategorie für Vorschau Pins ist Pin \_ Category \_ Preview. Die Kategorie für Erfassungs Pins ist die Erfassung der PIN- \_ Kategorie \_ .

**VideoPort-Pins**

Ein Videoport ist eine Hardware Verbindung zwischen einem Videogerät (z. b. einem analogen TV-Tuner) und der Grafikkarte. Ein Videoport ermöglicht dem Gerät das Senden von Videodaten direkt an die Grafikkarte. Das Video wird auf dem Bildschirm mithilfe einer Hardware Überlagerung angezeigt. Ein Videoport kann ein tatsächliches Kabel sein, das zwei Geräte auf separaten Karten verbindet. oder es handelt sich möglicherweise um eine hart verdrahtete Verbindung auf derselben Karte.

Der Vorteil eines Video Anschlusses besteht darin, dass das Video direkt in den Videospeicher übergeht, ohne dass die CPU funktioniert. Allerdings haben videports einige Nachteile:

-   Ein Videoport verwendet immer die Überlagerungs Oberfläche während der Erfassung, unabhängig davon, ob Sie das Video in der Vorschau anzeigen möchten.
-   Das Kippen zwischen Frames erfolgt automatisch, wodurch es schwierig wird, das Kippen mit anderen Video Vorgängen zu synchronisieren.

Wenn ein Aufzeichnungsgerät einen Videoport verwendet, hat der Erfassungs Filter anstelle einer Vorschau-Pin eine Videoport-PIN. Die PIN-Kategorie für Videoport Pins lautet "Pin \_ Category \_ Videoport".

Jeder Erfassungs Filter hat mindestens eine Erfassungs-PIN. Außerdem verfügt er möglicherweise über eine Vorschau-PIN oder eine Videoport-PIN, aber nicht beides. Filter können über mehrere Erfassungs Pins und Vorschau Pins verfügen, von denen jeder einen separaten Medientyp bereitstellt. Daher kann ein einzelner Filter eine Video Erfassungs-PIN, eine Video Vorschau-PIN, eine audioerfassungs-PIN und eine Audiovorschau-Pin enthalten. (Es gibt jedoch nichts, was einem Videoport für Audiodaten entspricht.)

**WDM-Upstream-Filter**

Für Windows-Treibermodell-Geräte (WDM) sind möglicherweise einige zusätzliche Filter für den Erfassungs Filter erforderlich. Diese Filter umfassen Folgendes:

-   [TV-Tuner-Filter](tv-tuner-filter.md). Steuert die Optimierung für analoge TV-Tuner.
-   [TV-Audiofilter](tv-audio-filter.md). Steuert die Audioeinstellungen für analoge TV-Tuner.
-   Der [Querbalken Filter für die analoge Video](analog-video-crossbar-filter.md)-. Leitet Video-und Audiosignale über das Hardware Gerät weiter. Ein Gerät kann z. b. über mehrere Eingaben verfügen, z. b. S-Video und zusammengesetztes Video. Der Querbalken Filter ermöglicht der Anwendung, die Eingabe auszuwählen.

Obwohl es sich hierbei um separate Filter in DirectShow handelt, stellen Sie in der Regel dasselbe Hardware Gerät dar. Jeder Filter steuert eine andere Funktion des Geräts. Die Filter sind durch Pins verbunden, aber keine Mediendaten werden über die PIN-Verbindungen verschoben. Daher wird durch das Einrichten eines Medientyps keine Verbindung mit den Pins dieser Filter hergestellt. Stattdessen werden GUID-Werte namens " *Mediums*" verwendet. Mittlere GUIDs sind für einen bestimmten Geräte-Mini Treiber eindeutig definiert. Beispielsweise unterstützen der TV-Tuner-Filter und der Video Erfassungs Filter für die gleiche TV-Karte beide das gleiche Medium, das es der Anwendung ermöglicht, das Diagramm ordnungsgemäß zu erstellen.

Wenn Sie **ICaptureGraphBuilder2** verwenden, um die Erfassungs Diagramme zu erstellen, werden diese Filter in der Praxis automatisch dem Diagramm hinzugefügt. Eine ausführlichere Erläuterung finden Sie unter [WDM-Klassen Treiber Filter](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Video Erfassung in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 




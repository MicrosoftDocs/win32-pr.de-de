---
description: Sequencer-Quell Ereignisse
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Sequencer-Quell Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347029"
---
# <a name="sequencer-source-events"></a>Sequencer-Quell Ereignisse

Wenn die [Sequencer-Quelle](sequencer-source.md) eine Sequenz von Dateien wieder gibt, sendet die Medien Sitzung im Allgemeinen alle Ereignisse, die während der normalen Wiedergabe gesendet werden und in [Medien Sitzungs Ereignissen](media-session-events.md)aufgeführt sind. Die Anwendung ruft diese Ereignisse mithilfe der [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medien Sitzung ab.

Außerdem gibt es einige Ereignisse, die für Wiedergabelisten Segmente spezifisch sind.



| Ereignis                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menewpresentation](menewpresentation.md)                                                              | Signalisiert der Anwendung, die nächste Topologie vorab auszusetzen.<br/> Um einen nahtlosen Übergang zwischen zwei aufeinander folgenden Präsentationen zu ermöglichen, lädt die Sequencer-Quelle die nächste Topologie im voraus. Obwohl die aktive Topologie immer noch abgespielt wird, sendet die Sequencer-Quelle dieses Ereignis für die nächste Topologie, solange eine nachfolgende Topologie in der Quelle verfügbar ist.<br/> Diese Ereignisdaten für dieses Ereignis sind der Präsentations Deskriptor für die nächste Topologie. Die Anwendung ist für das Festlegen der entsprechenden Topologie in der Medien Sitzung zuständig, wie in [Verwenden der Sequencer-Quelle](using-the-sequencer-source.md)beschrieben.<br/> |
| [Meendof presentationsegment](meendofpresentationsegment.md)                                            | Die Sequencer-Quelle löst dieses Ereignis aus, wenn die Medien Sitzung die Wiedergabe des aktuellen Segments abgeschlossen hat, wenn auf dieses Segment ein anderes Segment folgt. (Wenn es sich beim aktuellen Segment um das letzte Segment handelt, löst die Sequencer-Quelle stattdessen das [meendof Presentation](meendofpresentation.md) -Ereignis aus.)<br/> Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter. In der Regel empfängt die Anwendung [meendof presentationsegment](meendofpresentationsegment.md) , nachdem die Medien Sitzung mit der Verarbeitung des nächsten Segments begonnen hat, während die Medien senken weiterhin die Beispiele für das vorherige Segment liefern.<br/>                            |
| [Mesessiontopologystatus](mesessiontopologystatus.md), wobei die **\_ topostatus- \_ Senke \_** der Status-MF gewechselt ist. | Die Medien Sitzung löst dieses Ereignis aus, wenn es in der Sequencer-Quelle einen Übergang zur nächsten Topologie durchführt und die Wiedergabe der vorherigen Topologie durch Medien senken abgeschlossen wurde. Dieses Ereignis enthält einen Zeiger auf die nächste Topologie.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Beispiel 1: Wiedergabe ohne überspringen

Wenn die Sequencer-Quelle beteiligt ist, kann die Anzahl der Ereignisse, die Sie aus der Medien Sitzung erhalten, verwirrend sein, besonders weil Ereignisse, die einem Segment zugeordnet sind, häufig mit Ereignissen für das nächste Segment verschachtelt werden.

Im ersten Beispiel werden in der Anwendung drei Segmente, S1, S2 und S3 in die Warteschlange eingereiht. Das dritte Segment weist das **\_ Letzte Flag von sequencertopologyflags** auf, um zu signalisieren, dass es das letzte Segment in der Sequenz ist. Das Segment, dem jedes Ereignis entspricht, wird in Klammern angegeben. Die [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Aufrufe der Anwendung werden ebenfalls aufgelistet, um die Reihenfolge der Vorgänge zu verdeutlichen.

-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S1)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **MF \_ topostatus \_ Ready** (S1)
-   [Menewpresentation](menewpresentation.md) (S2-Vorabversion)
-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **die \_ \_ \_ Quelle "topostatus wurde gestartet** " (Start von S1)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S2)
-   [Meendof presentationsegment](meendofpresentationsegment.md) (Ende S1)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): Es wurde ein **MF \_ topostatus \_ beendet** (S1)
-   [Mesessiontopologystatus](mesessiontopologystatus.md)- **\_ \_ Senke \_** (Übergang zu S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **MF \_ topostatus \_ Ready** (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **die \_ \_ \_ Quelle "topostatus wurde gestartet** " (Start von S2)
-   [Menewpresentation](menewpresentation.md) (S3-Vorabversion)
-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S3)
-   [Meendof presentationsegment](meendofpresentationsegment.md) (Ende von S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): Es wurde ein **MF- \_ topostatus \_ beendet** (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md)- **\_ \_ Senke \_** (Übergang in S3)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **MF \_ topostatus \_ Ready** (S3)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **die \_ \_ \_ Quelle "topostatus wurde gestartet** " (Start von S3)
-   [Meendof Presentation](meendofpresentation.md) (Ende von S3; letztes Segment)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): das **MF- \_ topostatus wurde \_ beendet** .
-   [Mesessionend](mesessionended.md)

Diese Liste enthält nicht jedes Ereignis, das Sie möglicherweise erhalten. (Beispielsweise wird das Ereignis [mesessioncapabilitieschangiausgelassen](mesessioncapabilitieschanged.md) , das immer dann gesendet wird, wenn sich die Sitzungs Funktionen ändern. Eine Anwendung empfängt in der Regel mehrere mesessioncapabilitieschangsereignisse während einer Präsentation.) Bei den hier aufgeführten Ereignissen handelt es sich um die Ereignisse, die den Übergang von einem Segment zum nächsten veranschaulichen. Die wichtigsten Ereignisse sind [menewpresentation](menewpresentation.md), die der Anwendung die Vorabversion der nächsten Topologie signalisieren, und [meendofpresentationsegment](meendofpresentationsegment.md), das das Ende eines Segments signalisiert (mit Ausnahme des letzten Segments).

Da Ereignisse in Media Foundation asynchron sind und nicht mit Methoden Aufrufen serialisiert werden, kann die genaue Reihenfolge variieren. Beispielsweise können Sie die " **MF \_ topostatus \_ Started \_** "-Quelle für S1 erhalten, bevor die Anwendung die [**settopologie**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) für S2 aufruft.

Außerdem erhalten Sie möglicherweise nicht jedes Ereignis, das hier aufgeführt ist. Die Ereignisse [meendof Presentation](meendofpresentation.md) und [mesessionend](mesessionended.md) werden z. b. nicht gesendet, es sei denn, das letzte Segment hat das **\_ Letzte Flag sequencertopologyflags** .

Schließlich gibt diese Liste nicht den Zeitverlauf an. Die Zeit zwischen "Start von S1" und "Ende der S1" ist die gesamte Dauer von S1, die je nach Quelle einige Sekunden oder viele Stunden betragen kann.

## <a name="example-2-playback-with-segment-skipping"></a>Beispiel 2: Wiedergabe mit Segment übersprungen

In diesem Beispiel werden die gleichen Segmente von der Anwendung in die Warteschlange eingereiht, während das Segment 1 wiedergegeben wird. In diesem Fall werden die folgenden Ereignisse gesendet:

-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S1)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **MF \_ topostatus \_ Ready** (S1)
-   [Menewpresentation](menewpresentation.md) (S2-Vorabversion)
-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **die \_ \_ \_ Quelle "topostatus wurde gestartet** " (Start von S1)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S2)
-   Anwendungs Aufrufe [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (überspringen zu S3)
-   [Menewpresentation](menewpresentation.md) (S3-Vorabversion)
-   Anwendungs Aufrufe [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [Mesessionstarted](mesessionstarted.md)
-   [Meendof presentationsegment](meendofpresentationsegment.md) (S1 abgebrochen)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): Es wurde ein **MF \_ topostatus \_ beendet** (S1)
-   [Mesessiontopologyset](mesessiontopologyset.md) (S3)
-   [Mesessiontopologystatus](mesessiontopologystatus.md)- **\_ \_ Senke \_** (Übergang zu S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **MF \_ topostatus \_ Ready** (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): die Quelle "in der **MF \_ topostatus \_ gestartet \_** " (S2)
-   [Meendof presentationsegment](meendofpresentationsegment.md) (S2 abgebrochen)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): Es wurde ein **MF- \_ topostatus \_ beendet** (S2)
-   [Mesessiontopologystatus](mesessiontopologystatus.md)- **\_ \_ Senke \_** (Übergang in S3)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **topostatus \_ Ready** (S3)
-   [Mesessiontopologystatus](mesessiontopologystatus.md): **die \_ \_ \_ Quelle "topostatus gestartet** " (S3)

Wenn die Anwendung überspringen mit Segment 3 [**beginnt**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , bricht die Sequencer-Quelle Segment 1 ab, das noch abgespielt wird. Das [meendof presentationsegment](meendofpresentationsegment.md) -Ereignis für dieses Segment enthält das von der [**MF- \_ Ereignis \_ Quell \_ Topologie \_ abgebrochene**](mf-event-source-topology-canceled-attribute.md) Attribut, das angibt, dass das Segment beendet wurde, weil es abgebrochen wurde. Da das Segment 2 bereits vorab ausgeführt wird, wird dieses Segment gestartet, aber sofort abgebrochen. Das meendof presentationsegment-Ereignis für Segment 2 enthält auch das Attribut der **MF- \_ Ereignis \_ Quell \_ Topologie, das \_ abgebrochen** wurde. Die Sitzung kann dann zu Segment 3 wechseln und Sie normal wiedergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die Sequencer-Quelle](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 





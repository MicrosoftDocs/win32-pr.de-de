---
description: Präsentations Uhr
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Präsentations Uhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61ad02537a2591c681db78721376651f7854ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130489"
---
# <a name="presentation-clock"></a>Präsentations Uhr

Die *Präsentations Uhr* ist ein Objekt, das die Uhrzeit für eine Präsentation generiert. Die von der Präsentations Uhr gemeldete Zeit wird als *Präsentationszeit* bezeichnet. Alle Streams in einer Präsentation werden mit der Präsentationszeit synchronisiert. Die Präsentations Uhr zeigt die folgenden Schnittstellen an.



| Schnittstelle                                            | BESCHREIBUNG                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMF presentationclock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Primäre Schnittstelle für die Verwendung der Präsentations Uhr. |
| [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Steuert die Taktrate.                            |
| [**IMF-Timer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Stellt einen Timer-Rückruf bereit.                          |
| [**Nicht Herunterfahren**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Fährt die Präsentations Uhr herunter.                  |



 

Medien senken verwenden die Präsentationszeit, um den Zeitpunkt für das renderingmuster zu planen. Wenn eine Medien Senke ein neues Beispiel empfängt, ruft Sie den Zeitstempel aus dem Beispiel ab und rendert das Beispiel zum Zeitpunkt der festgelegten Zeit oder so nah wie möglich. Da alle Medien senken in einer Topologie dieselbe Präsentations Uhr verwenden, werden mehrere Streams (z. b. Audiodaten und Videos) synchronisiert. Medienquellen und-Transformationen verwenden nicht die Präsentationszeit, da Sie nicht planen, wann Stichproben geliefert werden sollen. Stattdessen werden immer dann Beispiele erzeugt, wenn die Pipeline ein neues Beispiel anfordert.

Wenn Sie die Medien Sitzung für die Wiedergabe verwenden, verarbeitet die Medien Sitzung alle Details zum Erstellen der Präsentations Uhr, zum Auswählen einer Zeit Quelle und zum Benachrichtigen der Medien senken. Die Anwendung kann die Präsentations Uhr verwenden, um die aktuelle Präsentationszeit während der Wiedergabe abzurufen, aber andernfalls werden keine Methoden auf der Präsentations Uhr aufgerufen.

## <a name="clock-time-and-clock-states"></a>Uhrzeit-und Uhrzeitangabe

Um die aktuelle Uhrzeit von der Präsentations Uhr abzurufen, wenden Sie [**imfpresentationclock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime)an. Uhrzeiten sind immer in 100-Nanosecond-Einheiten, sodass eine Sekunde 10 Millionen (10 ^ 7) Ticks ist. Dies entspricht einer Häufigkeit von 10 MHz.

Die Präsentations Uhr hat drei Zustände: "wird ausgeführt", "angehalten" und "beendet".

-   Um die Uhr auszuführen, nennen Sie [**imfpresentationclock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). Die **Start** -Methode gibt die Startzeit der Uhr an. Während der Uhr ausgeführt wird, wird die Uhrzeit von der Startzeit um die aktuelle Taktrate erhöht.
-   Um die Uhr anzuhalten, nennen Sie [**imfpresentationclock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Während die Uhr angehalten wird, wird die Uhrzeit nicht fortgesetzt, und [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) gibt die Zeit zurück, zu der die Uhr angehalten wurde.
-   Um die Uhr anzuhalten, nennen Sie [**imfpresentationclock:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Wenn die Uhr angehalten wird, wird die Uhrzeit nicht fortgesetzt, und [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) gibt 0 (null) zurück.

Standardmäßig wird die Uhr um 1,0 erhöht. Dies bedeutet 1 Tick pro 100 nanoseconds. Um die Rate zu ändern, mit der die Uhr fortschreitet, Fragen Sie die Präsentationszeit nach der [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle ab, und nennen Sie [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

-Objekte können Benachrichtigungen über Zustandsänderungen (einschließlich Änderungs Raten Änderungen) von der Präsentations Uhr empfangen. Um Benachrichtigungen zu empfangen, implementieren Sie die [**imfclockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle, und nennen Sie [**imfpresentationclock:: addclockstaatink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) auf der Präsentations Uhr. Vor dem Herunterfahren wird [**imfpresentationclock:: removeclockstaatink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) aufgerufen, um die Registrierung des Objekts aufzuheben. Medien senken verwenden diesen Mechanismus zum Empfangen von Benachrichtigungen von der Uhr.

## <a name="presentation-times"></a>Präsentations Zeiten

Eine Medien Senke versucht, die einzelnen Stichproben so zu planen, dass das Beispiel zur richtigen Zeit oder so nah wie möglich an der richtigen Zeit gerendert wird. Die folgenden Definitionen gelten:

-   *Präsentationszeit.* Der Zeitpunkt, zu dem ein Beispiel gerendert werden soll. Die Zeit wird in Einheiten von 100 Nanosekunden angegeben.
-   *Medien Zeit.* Zeit relativ zum Anfang des Inhalts. Wenn eine Videodatei z. b. 10 Sekunden lang ist, hat der Punkt in der Hälfte der Datei eine Medien Zeit von 5 Sekunden.
-   *Zeitstempel.* Die für ein Medien Beispiel markierte Zeit. Um den Zeitstempel abzurufen, wenden Sie [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime)an. Wenn eine Medienquelle eine Stichprobe erstellt, legt Sie den Zeitstempel auf die Medien Zeit fest. Die Medien Sitzung übersetzt den Zeitstempel in Präsentationszeit.

Standardmäßig sind die Zeit-und Präsentationszeit des Mediums identisch, z. b. Wenn ein Videorahmen 5 Sekunden in der Quelldatei angezeigt wird, sind die Medien Zeit und die Präsentationszeit jeweils 5 Sekunden. Wenn Sie die [Sequencer-Quelle](sequencer-source.md)verwenden, ist das Zeit Steuerungsmodell etwas komplizierter, um reibungslose Übergänge zwischen Segmenten zu ermöglichen. Weitere Informationen zum Zeit Steuerungsmodell der Sequencer-Quelle finden Sie unter [Sequenz Präsentations Zeiten](sequence-presentation-times.md).

Die Medienquelle legt den Zeitstempel immer auf die Medien Zeit fest. Wenn die Präsentationszeit nicht an der Medien Zeit ausgerichtet ist, werden die Zeitstempel in den Medien Beispielen von der Medien Sitzung konvertiert. Wenn die Senke ein Beispiel empfängt, wurde der Zeitstempel des Beispiels in die Präsentationszeit konvertiert. Die Senke plant die Stichprobe für die aktuelle Uhrzeit der Präsentations Uhr. (Raten lose senken stellen eine Ausnahme dar, da Sie die Präsentationszeit ignorieren.)

Wenn die Anwendung an einer neuen Position sucht, startet die Medien Sitzung die Präsentations Uhr zum angegebenen suchzeitpunkt neu. Wenn die Anwendung z. b. die 5-Sekunden-Position in der Datei sucht, wird die Uhr von der Medien Sitzung um 5 Sekunden gestartet. Die Medienquelle liefert möglicherweise Beispiele mit einem etwas früheren Zeitstempel, wenn die Suchzeit nicht auf eine Keyframe-Grenze fällt. Dies ist erforderlich, damit die Decoder alle Frames decodieren können. In der Medien Sitzung werden Stichproben gelöscht oder getestet, bevor Sie die Medien senken erreichen, um die angeforderte Suchzeit abzugleichen. Wenn die Suchzeit beispielsweise 5 Sekunden beträgt, kann das erste Audiobeispiel um 4,5 Sekunden beginnen. Die Medien Sitzung schneidet die ersten 0,5 Sekunden aus dem ersten decodierten Audiobeispiel ab.

## <a name="creating-the-presentation-clock"></a>Erstellen der Präsentations Uhr

Um die Präsentations Uhr zu erstellen, rufen Sie [**mfkreatepresentationclock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock)auf. Um die Uhr herunterzufahren, Fragen Sie die [**imfshutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) -Schnittstelle ab, und nennen Sie [**imfshutdown:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). Der Aufrufer von **mfcreatepresentationclock** ist für das Aufrufen von **Shutdown** verantwortlich. in den meisten Fällen ist dies die Medien Sitzung und nicht die Anwendung.

## <a name="presentation-time-sources"></a>Präsentationszeit Quellen

Trotz des Namens implementiert die Präsentations Uhr nicht tatsächlich eine Uhr. Stattdessen werden die Uhrzeiten von einem anderen Objekt abgerufen, das als *Präsentationszeit Quelle* bezeichnet wird. Die Zeit Quelle kann ein beliebiges Objekt sein, das exakte Takt Einheiten generiert und die [**IMF presentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) -Schnittstelle verfügbar macht. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das die Beziehung zwischen der Präsentations Uhr und der Präsentationszeit Quelle anzeigt](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Wenn die Präsentations Uhr erstmalig erstellt wird, verfügt sie nicht über eine Zeit Quelle. Um die Zeit Quelle festzulegen, müssen Sie [**imfpresentationclock:: settimesource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) mit einem Zeiger auf die [**imfpresentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) -Schnittstelle der Zeit Quelle aufrufen. Eine Zeit Quelle unterstützt die gleichen Zustände wie die Präsentations Uhr (wird ausgeführt, angehalten und beendet) und muss die [**imbodstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle implementieren. Die Präsentations Uhr verwendet diese Schnittstelle, um die Zeit Quelle zu benachrichtigen, wenn der Zustand geändert werden soll. Auf diese Weise stellt die Zeit Quelle die Takt Ticks bereit, aber die Präsentations Uhr initiiert Zustandsänderungen in der Uhr.

Einige Medien senken haben Zugriff auf eine exakte Uhr und machen daher die [**imfpresentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) -Schnittstelle verfügbar. Insbesondere kann der audiorenderer die Frequenz der Soundkarte als Uhr verwenden. Bei der Audiowiedergabe ist es nützlich, wenn der audiorenderer als Zeit Quelle fungiert, damit das Video mit der Audiowiedergabe Rate synchronisiert wird. Dies führt im Allgemeinen zu besseren Ergebnissen als bei der Anpassung der Audiodaten an eine externe Uhr.

Media Foundation bietet auch eine Präsentationszeit Quelle basierend auf der Systemuhr. Um dieses Objekt zu erstellen, rufen Sie [**mfkreatesystemtimesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource)auf. Die Systemzeit Quelle kann verwendet werden, wenn keine Medien senken eine Zeit Quelle bereitstellen.

Im Allgemeinen muss eine Medien Senke die dargestellte Präsentations Uhr verwenden, unabhängig davon, welche Zeit Quelle von der Präsentationszeit verwendet wird. Diese Regel gilt auch, wenn eine Medien Senke [**IMF presentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource)implementiert. Wenn die Präsentations Uhr eine andere Zeit Quelle verwendet, muss die Medien Senke dieser Zeit Quelle und nicht der eigenen internen Uhr folgen.

Es gibt zwei Situationen, in denen eine Medien Senke nicht der Präsentations Uhr folgt:

-   Einige Medien senken sind Gebühren *loser*. Wenn eine Medien Senke nicht mehr benötigt wird, werden Stichproben so schnell wie möglich verarbeitet, ohne Sie entsprechend der Präsentationszeit zu planen. In der Regel schreiben ratlose senken Daten in eine Datei. Daher ist es wünschenswert, den Vorgang so schnell wie möglich abzuschließen. Eine Gebühren lose Senke gibt das mediasink- \_ Flag in der [**imfmediasink:: getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode zurück. Wenn alle senken in einer Topologie ratlos sind, überträgt die Medien Sitzung Daten so schnell wie möglich über die Pipeline.

-   Einige Medien senken können nicht mit den Raten einer anderen Zeit Quelle als sich selbst vergleichen. Wenn dies der Fall ist, gibt die Senke das mediasink- \_ \_ \_ Flag für die Uhr nicht mit der [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode identisch. Die Pipeline kann immer noch eine andere Zeit Quelle verwenden, die Ergebnisse sind jedoch kleiner als optimal. Die Senke wird wahrscheinlich zurückliegen und bewirkt, dass während der Wiedergabe Fehler auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 




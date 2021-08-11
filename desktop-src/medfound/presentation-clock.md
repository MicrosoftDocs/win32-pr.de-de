---
description: Präsentationsuhr
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Präsentationsuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0219b6384373fd75bc8a424935e502841071f69eaa9ae719ec6ed35c950218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239159"
---
# <a name="presentation-clock"></a>Präsentationsuhr

Die *Präsentationsuhr* ist ein Objekt, das die Uhrzeit für eine Präsentation generiert. Die von der Präsentationsuhr gemeldete Zeit wird als *Präsentationszeit bezeichnet.* Alle Streams in einer Präsentation werden mit der Präsentationszeit synchronisiert. Die Präsentationsuhr macht die folgenden Schnittstellen verfügbar.



| Schnittstelle                                            | BESCHREIBUNG                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**DEADPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Primäre Schnittstelle für die Verwendung der Präsentationsuhr. |
| [**ATRATEControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Steuert die Taktrate.                            |
| [**VERERBungszeit**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Stellt einen Timerrückruf zur                          |
| [**BEShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Fährt die Präsentationsuhr herunter.                  |



 

Mediensenken verwenden die Präsentationszeit, um zu planen, wann Stichproben gerendert werden. Wenn eine Mediensenke ein neues Beispiel empfängt, ruft sie den Zeitstempel aus dem Beispiel ab und rendert das Beispiel zum angegebenen Zeitpunkt oder so nah wie möglich an diesem Zeitpunkt. Da alle Mediensenken in einer Topologie dieselbe Präsentationsuhr verwenden, werden mehrere Datenströme (z. B. Audio und Video) synchronisiert. Medienquellen und Transformationen verwenden nicht die Präsentationsuhr, da sie nicht planen, wann Stichproben zu liefern sind. Stattdessen erzeugen sie Stichproben, wenn die Pipeline ein neues Beispiel an fordert.

Wenn Sie die Mediensitzung für die Wiedergabe verwenden, verarbeitet die Mediensitzung alle Details zum Erstellen der Präsentationsuhr, auswählen einer Zeitquelle und Benachrichtigen der Mediensenken. Ihre Anwendung verwendet möglicherweise die Präsentationsuhr, um die aktuelle Präsentationszeit während der Wiedergabe zu erhalten, aber andernfalls werden keine Methoden für die Präsentationsuhr aufruft.

## <a name="clock-time-and-clock-states"></a>Uhrzeit und Uhrzustände

Um die aktuelle Uhrzeit aus der Präsentationsuhr zu erhalten, rufen [**Sie DIEPRESENTATIONClock::GetTime auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) Die Zeiteinheiten liegen immer in Einheiten von 100 Nanosekunden, sodass eine Sekunde 10.000.000 (10^7) Ticks beträgt. Dies entspricht einer Frequenz von 10 MHz.

Die Präsentationsuhr hat drei Zustände: Wird ausgeführt, angehalten und beendet.

-   Um die Uhr ausführen zu können, rufen [**Sie DANNPRESENTationClock::Start auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) Die **Startmethode** gibt die Startzeit der Uhr an. Während die Uhr ausgeführt wird, erhöht sich die Uhrzeit ab der Startzeit mit der aktuellen Taktrate.
-   Um die Uhr anzuhalten, rufen [**Sie DANNPresentationClock::P ause auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) Während die Uhr angehalten wird, wird die Uhrzeit nicht vorangehen, und [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) gibt die Uhrzeit zurück, zu der die Uhr angehalten wurde.
-   Um die Uhr zu beenden, rufen [**Sie DIEPRESENTationClock::Stop auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) Wenn die Uhr beendet wird, wird die Uhrzeit nicht vorangesetzt, und [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) gibt 0 (null) zurück.

Standardmäßig wird die Uhr mit einer Rate von 1,0 vorangestellt, was 1 Tick pro 100 Nanosekunden bedeutet. Um die Geschwindigkeit zu ändern, mit der die Uhr nach vorn geht, fragen Sie die Präsentationsuhr nach der [**BERRATEControl-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) ab, und rufen [**Sie DANNRATEControl::SetRate auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)

Objekte können Benachrichtigungen über Zustandsänderungen (einschließlich Änderungen der Geschwindigkeit) von der Präsentationsuhr empfangen. Implementieren Sie zum Empfangen von Benachrichtigungen [**die BENUTZEROBERFLÄCHEClockStateSink-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) und rufen Sie [**DANNPRESENTPresentationClock::AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) auf der Präsentationsuhr auf. Rufen Sie vor dem Herunterfahren [**DIEPRESENTationClock::RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) auf, um die Registrierung des Objekts zu aufheben. Mediensenken verwenden diesen Mechanismus, um Benachrichtigungen von der Uhr zu empfangen.

## <a name="presentation-times"></a>Präsentationszeiten

Eine Mediensenke versucht, jedes Beispiel so zu planen, dass das Beispiel zum richtigen Zeitpunkt oder so nah wie möglich an der richtigen Zeit gerendert wird. Es gelten die folgenden Definitionen:

-   *Präsentationszeit.* Die Zeit, zu der ein Beispiel gerendert werden soll. Die Zeit wird in Einheiten von 100 Nanosekunden angegeben.
-   *Medienzeit.* Zeit relativ zum Anfang des Inhalts. Wenn eine Videodatei beispielsweise 10 Sekunden lang ist, hat der Punkt in der Hälfte der Datei eine Medienzeit von 5 Sekunden.
-   *Zeitstempel.* Die in einem Medienbeispiel markierte Zeit. Um den Zeitstempel zu erhalten, rufen [**Sie DIESAMPLE::GetSampleTime auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) Wenn eine Medienquelle ein Beispiel erzeugt, legt sie den Zeitstempel auf die Medienzeit fest. Die Mediensitzung übersetzt den Zeitstempel in die Präsentationszeit.

Standardmäßig sind Medienzeit und Präsentationszeit identisch. Wenn beispielsweise ein Videoframe 5 Sekunden in der Quelldatei angezeigt wird, beträgt die Medienzeit und die Präsentationszeit beide 5 Sekunden. Wenn Sie die [Sequencerquelle](sequencer-source.md)verwenden, ist das Zeitsteuerungsmodell etwas komplizierter, um reibungslose Übergänge zwischen Segmenten zu ermöglichen. Weitere Informationen zum Zeitsteuerungsmodell der Sequencerquelle finden Sie unter [Sequence Presentation Times](sequence-presentation-times.md).

Die Medienquelle legt den Zeitstempel immer auf die Medienzeit fest. Wenn die Präsentationszeit nicht an der Medienzeit ausgerichtet ist, konvertiert die Mediensitzung die Zeitstempel der Medienbeispiele. Wenn die Senke ein Beispiel empfängt, wurde der Zeitstempel des Beispiels in die Präsentationszeit konvertiert. Die Senke geplant das Beispiel mit der aktuellen Uhrzeit der Präsentationsuhr. (Rateless-Senken sind eine Ausnahme, da sie die Präsentationsuhr ignorieren.)

Wenn die Anwendung eine neue Position ansuchet, startet die Mediensitzung die Präsentationsuhr zur angegebenen Suchzeit neu. Wenn die Anwendung beispielsweise die 5-Sekunden-Position in der Datei anfängt, startet die Mediensitzung die Uhr um 5 Sekunden. Die Medienquelle kann Stichproben mit einem etwas früheren Zeitstempel liefern, wenn die Suchzeit nicht auf eine Keyframegrenze fällt. Dies ist erforderlich, damit die Decoder alle Frames decodieren können. Die Mediensitzung löscht oder schneidet Stichproben ab, bevor sie die Mediensenken erreichen, um die angeforderte Suchzeit zu erreichen. Wenn die Suchzeit beispielsweise 5 Sekunden beträgt, kann das erste Audiobeispiel bei 4,5 Sekunden beginnen. Die Mediensitzung entfernt die ersten 0,5 Sekunden vom ersten decodierten Audiobeispiel.

## <a name="creating-the-presentation-clock"></a>Erstellen der Präsentationsuhr

Rufen Sie zum Erstellen der Präsentationsuhr [**MFCreatePresentationClock auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock) Fragen Sie zum Herunterfahren der Uhr nach [**der BENUTZEROBERFLÄCHE AB,**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) und rufen [**Sie DIEZShutdown::Shutdown auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) Der Aufrufer von **MFCreatePresentationClock** ist für den Aufruf von **Shutdown verantwortlich.** In den meisten Fällen ist dies die Mediensitzung und nicht die Anwendung.

## <a name="presentation-time-sources"></a>Präsentationszeitquellen

Trotz des Namens implementiert die Präsentationsuhr keine Uhr. Stattdessen ruft sie die Uhrzeiten von einem anderen Objekt ab, das als *Präsentationszeitquelle bezeichnet wird.* Die Zeitquelle kann ein beliebiges Objekt sein, das genaue Takte generiert und die [**BENUTZEROBERFLÄCHEPresentationTimeSource-Schnittstelle verfügbar**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) macht. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das die Beziehung zwischen der Präsentationsuhr und der Präsentationszeitquelle zeigt](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Wenn die Präsentationsuhr zum ersten Mal erstellt wird, verfügt sie nicht über eine Zeitquelle. Rufen Sie ZUM Festlegen der Zeitquelle [**DIE ZEITQUELLEPresentationClock::SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) mit einem Zeiger auf die [**BENUTZEROBERFLÄCHE DER ZEITQUELLE AUF.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) Eine Zeitquelle unterstützt die gleichen Zustände wie die Präsentationsuhr (wird ausgeführt, angehalten und angehalten) und muss die [**BERClockStateSink-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) implementieren. Die Präsentationsuhr verwendet diese Schnittstelle, um die Zeitquelle zu benachrichtigen, wann der Zustand geändert werden soll. Auf diese Weise stellt die Zeitquelle die Takte zur Verfügung, aber die Präsentationsuhr initiiert Zustandsänderungen in der Uhr.

Einige Mediensenken haben Zugriff auf eine genaue Uhr und machen daher die [**BENUTZEROBERFLÄCHEPRESENTationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) verfügbar. Insbesondere kann der Audiorenderer die Frequenz der Soundkarte als Uhr verwenden. Bei der Audiowiedergabe ist es nützlich, dass der Audiorenderer als Zeitquelle verwendet wird, damit das Video mit der Audiowiedergaberate synchronisiert wird. Dies führt im Allgemeinen zu besseren Ergebnissen als der Versuch, die Audiodaten mit einer externen Uhr zu ab passen.

Media Foundation stellt auch eine Präsentationszeitquelle basierend auf der Systemuhr zur Verfügung. Rufen Sie zum Erstellen dieses Objekts [**MFCreateSystemTimeSource auf.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource) Die Systemzeitquelle kann verwendet werden, wenn keine Mediensenken eine Zeitquelle bereitstellen.

Im Allgemeinen muss eine Mediensenke die bereitgestellte Präsentationsuhr verwenden, unabhängig davon, welche Zeitquelle die Präsentationsuhr verwendet. Diese Regel gilt auch, wenn eine Mediensenke [**DIEPRESENTationTimeSource implementiert.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) Wenn die Präsentationsuhr eine andere Zeitquelle verwendet, muss die Mediensenke dieser Zeitquelle folgen, nicht ihrer eigenen internen Uhr.

Es gibt zwei Situationen, in denen eine Mediensenke nicht der Präsentationsuhr folgt:

-   Einige Mediensenken sind *rateless*. Wenn eine Mediensenke ratelos ist, werden Stichproben so schnell wie möglich verbraucht, ohne sie gemäß der Präsentationsuhr zu planen. In der Regel schreiben rateless-Senken Daten in eine Datei, daher ist es wünschenswert, den Vorgang so schnell wie möglich abschließen. Eine rateless-Senke gibt das MEDIASINK \_ RATELESS-Flag in [**derEN METHODE ZUEink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) zurück. Wenn alle Senken in einer Topologie ratelos sind, überträgt die Mediensitzung Daten so schnell wie möglich über die Pipeline.

-   Einige Mediensenken können nicht mit einer anderen Zeitquelle als sich selbst übereinstimmen. Wenn dies der Wert ist, gibt die Senke das FLAG MEDIASINK \_ CANNOT MATCH CLOCK in der \_ \_ [**GetCharacteristics-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) zurück. Die Pipeline kann weiterhin eine andere Zeitquelle verwenden, aber die Ergebnisse sind weniger optimal. Die Senke fällt wahrscheinlich zurück und verursacht während der Wiedergabe Störungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 




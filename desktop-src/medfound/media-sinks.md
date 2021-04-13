---
description: Medien senken sind die Pipeline Objekte, die Mediendaten empfangen.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Medien senken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351248"
---
# <a name="media-sinks"></a>Medien senken

*Medien senken* sind die Pipeline Objekte, die Mediendaten empfangen. Eine Medien Senke ist das Ziel für einen oder mehrere Mediendaten Ströme. Medien senken lassen sich in zwei allgemeine Kategorien unterteilen:

-   Ein *Renderer* ist eine Medien Senke, die Daten für die Wiedergabe darstellt. Der Enhanced Video Renderer (EVR) zeigt Video Frames an, und der audiorenderer stellt Audiostreams über die Soundkarte oder ein anderes Audiogerät wieder.

-   Eine *Archiv Senke* ist eine Medien Senke, die Daten in eine Datei oder einen anderen Speicher schreibt.

Der Hauptunterschied besteht darin, dass eine Archiv Senke die Daten nicht mit fester Wiedergabe Rate beansprucht. Stattdessen werden die empfangenen Daten so schnell wie möglich geschrieben.

Medien senken machen die [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Schnittstelle verfügbar. Jede Medien Senke enthält mindestens einen *streamsenken*. Jede streamsenke empfängt die Daten aus einem Datenstrom. Stream-senken machen die [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle verfügbar. In der Regel werden Medien senken nicht direkt von einer Anwendung erstellt. Stattdessen erstellt die Anwendung ein oder mehrere Aktivierungs Objekte, die von der Medien Sitzung zum Erstellen der Senke verwendet werden. Alle anderen Vorgänge in der Senke werden von der Medien Sitzung verarbeitet, und die Anwendung ruft keine Methoden für die Medien Senke oder einen der streamsenken auf. Weitere Informationen zu Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).

Lesen Sie den Rest dieses Themas, wenn Sie eine benutzerdefinierte Medien Senke schreiben, oder wenn Sie eine Medien Senke direkt ohne die Medien Sitzung verwenden möchten.

-   [Streamsenken](#stream-sinks)
-   [Präsentations Uhr](#presentation-clock)
-   [Streamformate](#stream-formats)
-   [Datenfluss](#data-flow)
-   [Marker](#markers)
-   [Statusänderungen](#state-changes)
-   [Ausführung wird abgeschlossen](#finalizing)
-   [Wird heruntergefahren](#shutting-down)
-   [Media Sink-Schnittstellen](#media-sink-interfaces)
-   [Stream Sink-Schnittstellen](#stream-sink-interfaces)
-   [Streamsink-Ereignisse](#stream-sink-events)
-   [Zugehörige Themen](#related-topics)

## <a name="stream-sinks"></a>Streamsenken

Eine Medien Senke kann eine Fixed-Anzahl von streamsenken aufweisen, oder Sie kann das Hinzufügen und Entfernen von streamsenken unterstützen. Wenn Sie über eine festgelegte Anzahl von streamsenken verfügt, gibt die [**imfmediasink:: getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode das Flag "mediasink \_ Fixed Streams" zurück \_ . Andernfalls können Sie streamsenken hinzufügen und entfernen. Um eine neue streamsenke hinzuzufügen, nennen Sie [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Um eine streamsenke zu entfernen, nennen Sie [**imfmediasink:: removestreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Das Flag für "mediasink \_ Fixed \_ Streams" gibt an, dass die Medien Senke diese beiden Methoden nicht unterstützt. (Es kann eine andere Möglichkeit zum Konfigurieren der Anzahl von Streams unterstützen, z. b. durch Festlegen von Initialisierungs Parametern, wenn die Senke erstellt wird.) Die Liste der streamsenken ist geordnet. Um diese nach Indexwert aufzulisten, müssen Sie die [**imfmediasink:: getstreamsink byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) -Methode aufrufen.

Streamsenken verfügen auch über Bezeichner. Stream-IDs sind innerhalb der Medien Senke eindeutig, müssen jedoch nicht aufeinander folgen. Abhängig von der Medien Senke können die Datenstrom Bezeichner eine gewisse Bedeutung haben, die mit dem Inhalt verknüpft ist. Beispielsweise könnte eine Archiv Senke die Datenstrom Bezeichner in den Dateiheader schreiben. Andernfalls handelt es sich um beliebige. Um eine streamsenke anhand ihres Bezeichners abzurufen, nennen Sie [**imfmediasink:: getstreamsinkbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Präsentations Uhr

Die Rate, mit der eine Medien Senke Stichproben verarbeitet, wird von der [Präsentations Uhr](presentation-clock.md)gesteuert. In der Medien Sitzung wird die Präsentations Uhr ausgewählt und auf der Medien Senke durch Aufrufen der [**imfmediasink:: setpresentationclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) -Methode der Medien Senke festgelegt. Die Präsentations Uhr muss auf der Medien Senke festgelegt werden, bevor das Streaming beginnen kann. Für jede Medien Senke muss eine Präsentations-Uhr ausgeführt werden. Die Medien Senke verwendet die Präsentations Uhr für zwei Zwecke:

-   Zum Empfangen von Benachrichtigungen, wenn Streaming gestartet oder angehalten wird. Die Medien Senke empfängt diese Benachrichtigungen über die [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle, die alle Medien senken implementieren müssen.

-   , Um zu bestimmen, wann die Beispiele angezeigt werden sollen. Wenn die Medien Senke ein neues Beispiel empfängt, ruft Sie den Zeitstempel aus dem Beispiel ab und versucht, das Beispiel zu dieser Präsentationszeit zu rendernieren.

Die Präsentations Uhr leitet die Uhrzeiten von einem anderen Objekt ab, das als *Präsentationszeit Quelle* bezeichnet wird. Präsentationszeit Quellen machen die [**IMF presentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) -Schnittstelle verfügbar. Einige Medien senken haben Zugriff auf eine exakte Uhr, sodass Sie diese Schnittstelle verfügbar machen. Dies bedeutet, dass eine Medien Senke Stichproben anhand einer Zeit planen kann, die von der eigenen Uhr bereitgestellt wird. Die Medien Senke kann dies jedoch nicht annehmen. Es muss immer die Uhrzeit von der Präsentations Uhr verwenden, unabhängig davon, ob die Präsentations Uhr von der Medien Senke selbst oder von einer anderen Uhr gesteuert wird.

Wenn eine Medien Senke nicht mit einer anderen als der eigenen Uhr abgeglichen werden kann, gibt die [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode das mediasink-Flag für die \_ \_ \_ Uhrzeitangabe nicht zurück. Wenn dieses Flag vorhanden ist und die Präsentations Uhr eine andere Präsentationszeit Quelle verwendet, ist die Medien Senke wahrscheinlich schlecht. Beispielsweise könnte es während der Wiedergabe passieren.

Eine Gebühren *lose* Senke ist eine Medien Senke, die die Zeitstempel von Beispielen ignoriert und Daten verarbeitet, sobald die einzelnen Beispiele eintreffen. Eine ratlose Medien Senke gibt das mediasink- \_ Flag mit der Methode " [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) " zurück. Dieses Flag gilt in der Regel für Archiv senken. Wenn jede Medien Senke in der Pipeline Gebühren lose ist, verwendet die Medien Sitzung eine spezielle, ratlose Präsentationszeit. Diese Uhr wird so schnell ausgeführt, wie die senken Stichproben belegen.

## <a name="stream-formats"></a>Streamformate

Bevor die Medien Senke Beispiele empfangen kann, muss der Client den Medientyp für die streamsenken festlegen. Um den Medientyp festzulegen, müssen Sie die [**imfstreamsink:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) -Methode der Stream-Senke aufrufen. Diese Methode gibt einen Zeiger auf die [**imfmediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle zurück. Verwenden Sie diese Schnittstelle, um die Liste der bevorzugten Medientypen zu erhalten, den aktuellen Medientyp zu erhalten und den Medientyp festzulegen.

Wenn Sie die Liste der bevorzugten Medientypen abrufen möchten, müssen Sie [**imfmediatyethandler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex)aufrufen. Die bevorzugten Typen sollten als Hinweis für den Client übernommen werden. Die Liste kann unvollständig sein oder partielle Medientypen einschließen. Ein partieller Medientyp ist ein Typ, der nicht über alle Attribute verfügt, die zum Beschreiben eines gültigen Formats benötigt werden. Beispielsweise kann ein partieller Videotyp den Farb Raum und die Bitrate, aber nicht die Breite oder Höhe des Bilds angeben. Mit einem partiellen Audiotyp können das Komprimierungs Format und die Samplingrate, aber nicht die Anzahl der Audiokanäle angegeben werden.

Um den aktuellen Medientyp der Stream-Senke abzurufen, nennen Sie [**imfmediatyphandler:: getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Wenn eine streamsenke erstmalig erstellt wird, ist möglicherweise bereits ein Standard Medientyp festgelegt, oder es kann kein Medientyp vorhanden sein, bis der Client einen festgelegt hat.

Um den Medientyp festzulegen, müssen Sie [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)aufrufen. Einige streamsenken unterstützen möglicherweise nicht das Ändern des Typs, nachdem festgelegt wurde. Daher ist es hilfreich, die Medientypen vor dem festlegen zu testen. Um zu testen, ob die Medien Senke einen Medientyp annimmt (ohne Festlegen des Typs), nennen Sie [**imfmediatypehandler:: ismediatypesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Datenfluss

Medien senken verwenden ein *Pull-Modell*, was bedeutet, dass die Stream-senken Daten anfordern, wenn Sie Sie benötigen. Der Client sollte rechtzeitig reagieren, um das Abrufen zu vermeiden.

Einige Medien senken unterstützen die *vorab* Version. Die Vorabversion ist der Prozess, bei dem Daten an die Medien Senke über gegeben werden, bevor die Präsentations Uhr beginnt. Wenn eine Medien Senke die Vorabversion unterstützt, macht die Medien Senke die [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) -Schnittstelle verfügbar, und die [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode gibt das mediasink-Flag für den vorab Befehl zurück \_ \_ . Die Vorabversion stellt sicher, dass die Medien Senke bereit ist, das erste Beispiel zu präsentieren, wenn die Präsentations Uhr gestartet wird. Es wird empfohlen, dass der Client immer vorab einen vorab Vorgang vorhat, wenn er von der Medien Senke unterstützt wird

Der Datenfluss zu einer Medien Senke funktioniert wie folgt:

1.  Der Client legt die Medientypen und die Präsentations Uhr fest. Die Medien Senke registriert sich selbst bei der Präsentationszeit, um Benachrichtigungen zu Änderungen des uhrzustands zu erhalten.
2.  Optional fragt der Client [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)ab. Wenn die Medien Senke diese Schnittstelle verfügbar macht, ruft der Client [**imfmediasinkpreroll:: notifypreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll)auf. Andernfalls springt der Client zu Schritt 5.
3.  Jede streamsenke sendet ein oder mehrere [mestreamsinkrequestsample](mestreamsinkrequestsample.md) -Ereignisse. Als Reaktion auf jedes dieser Ereignisse ruft der Client die nächste Stichprobe der Daten für diesen Stream ab und ruft [**imfstreamsink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample)auf.
4.  Wenn jede streamsenke genügend vorab Daten empfängt, sendet Sie ein [mestreamsinkprerolled](mestreamsinkprerolled.md) -Ereignis.
5.  Der Client ruft die [**imfpresentationclock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) -Methode auf, um die Präsentations Uhr zu starten.
6.  Die Präsentations Uhr benachrichtigt die Medien Senke, dass die Uhr gestartet wird, indem [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)aufgerufen wird.
7.  Um weitere Daten zu erhalten, sendet jede streamsenke [mestreamsinkrequestsample](mestreamsinkrequestsample.md) -Ereignisse. Als Reaktion auf jedes dieser Ereignisse wird der Client das nächste Beispiel abrufen und [**processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample)aufrufen. Dieser Schritt wird bis zum Ende der Präsentation wiederholt.

Die meisten Medien senken Prozess Beispiele asynchron, sodass die streamsenken mehr als eine Beispiel Anforderung gleichzeitig senden können.

Beim Streaming kann der Client " [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) " und " [**imfstreamsink:: Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) " jederzeit aufrufen. Marker werden im nächsten Abschnitt beschrieben. Das leeren bewirkt, dass die streamsenke alle in der Warteschlange befindlichen, aber noch nicht gerenderten Beispiele löscht.

## <a name="markers"></a>Marker

Marker bieten eine Möglichkeit für den Client, bestimmte Punkte im Stream anzugeben. Ein Marker besteht aus den folgenden Informationen:

-   Der Markertyp, der als Member der [**mfstreamsink- \_ \_ Markertyp**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) -Enumeration definiert ist.
-   Dem Marker zugeordnete Daten. Die Bedeutung der Daten hängt vom Markertyp ab. Einige Markertypen weisen keine Daten auf.
-   Optionale Daten für die Verwendung durch den Client.

Zum Platzieren eines Markers ruft der Client [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)auf. Die streamsenke schließt die Verarbeitung von vor dem **Placemarker** -Aufruf empfangenen Beispielen ab und sendet dann ein [mestreamsinkmarker](mestreamsinkmarker.md) -Ereignis.

Die meisten Medien senken behalten eine Warteschlange von ausstehenden Stichproben bei, die Sie asynchron verarbeiten. Markerereignisse müssen mit Beispiel Verarbeitung serialisiert werden, sodass die Medien Senke die Marker in derselben Warteschlange platzieren sollte. Nehmen Sie beispielsweise an, der Client führt die folgenden Methodenaufrufe aus:

1.  [**Processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (Beispiel \# 1)
2.  [**Processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (Beispiel \# 2)
3.  [**Placemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (Marker \# 1)
4.  [**Processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (Beispiel \# 3)
5.  [**Placemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (Marker \# 2)

In diesem Beispiel muss die streamsenke das [mestreamsinkmarker](mestreamsinkmarker.md) -Ereignis für Marker \# 1 nach der Verarbeitung von Beispiel \# 2 und das-Ereignis für Marker \# 2 nach dem Verarbeiten von Beispiel \# 3 senden.

Wenn der Client eine streamsenke leert, verarbeitet die streamsenke sofort alle Marker, die sich in der Warteschlange befanden. Der Statuscode wird für \_ diese Ereignisse auf E Abort festgelegt.

Einige Marker enthalten Informationen, die für die Medien Senke relevant sind:

-   **MF-Senke \_ Marker- \_ Tick**: gibt an, dass sich eine Lücke im Stream befindet. Das nächste Beispiel ist eine Diskontinuität.
-   **MF-Senke \_ Marker \_ EndOf Segment**: gibt das Ende eines Segments oder das Ende eines Streams an. Das nächste Beispiel (falls vorhanden) kann eine Diskontinuität sein.
-   **MF-Senke \_ \_Markerereignis**: enthält ein Ereignis. Abhängig vom Ereignistyp und der Implementierung der Medien Senke kann die Medien Senke das Ereignis behandeln oder ignorieren.

## <a name="state-changes"></a>Zustandsänderungen

Eine Medien Senke wird über die [**imboclockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle der Medien Senke über Zustandsänderungen in der Präsentationszeit benachrichtigt. Wenn der Client die Präsentations Uhr festlegt, ruft die Medien Senke [**imfpresentationclock:: addclockstaatink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) auf, um sich selbst für Benachrichtigungen von der Uhr zu registrieren. In der folgenden Tabelle wird zusammengefasst, wie sich eine Medien Senke in Reaktion auf Änderungen des uhrzustands verhält.



| Änderung des uhrzustands                                         | Beispiel Verarbeitung                                                                                                                                                                                                                                             | Markerverarbeitung                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Prozess Beispiele, deren Zeitstempel gleich oder nach der Startzeit der Uhr ist.                                                                                                                                                                              | Senden Sie das [mestreamsinkmarker](mestreamsinkmarker.md) -Ereignis, wenn alle vor der Markierung empfangenen Beispiele verarbeitet wurden.                                                                 |
| [**Onclockpause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | Beim Anhalten der Medien Senke kann [**processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) fehlschlagen.<br/> Wenn die Medien Senke beim Anhalten Stichproben annimmt, muss Sie in die Warteschlange eingereiht werden, bis die Uhr neu gestartet wird. Verarbeiten Sie keine Stichproben in der Warteschlange, während Sie angehalten wurden.<br/> | Wenn Beispiele in der Warteschlange vorhanden sind, platzieren Sie Marker in derselben Warteschlange. Sendet das Markerereignis, wenn die Uhr neu gestartet wird.<br/> Senden Sie andernfalls das Markerereignis sofort.<br/>                    |
| [**Onclockrestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Verarbeiten Sie alle Samplings, die während der Warteschlange in die Warteschlange eingereiht wurden, und behandeln Sie diese dann wie [**onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).                                                                                                                         | Senden Sie [mestreamsink Marker](mestreamsinkmarker.md) -Ereignisse für in der Warteschlange eingereihte Marker (serialisiert mit der Beispiel Verarbeitung), und behandeln Sie diese dann genauso wie [**onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**Onclockstoppt**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Löschen Sie alle Beispiele in der Warteschlange. Weitere Aufrufe von [**processsample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) können fehlschlagen.                                                                                                                                                      | Senden von Markerereignissen in der Warteschlange. Senden Sie bei nachfolgenden Aufrufen von [**Placemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)das Markerereignis sofort.                                                              |



 

Außerdem müssen streamsenken die folgenden Ereignisse senden, wenn Sie die Zustandsübergänge abgeschlossen haben:

-   [**Onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**onclockrestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart): [mestreamsink Started](mestreamsinkstarted.md) -Ereignis
-   [**Onclockpause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause): [mestreamsink](mestreamsinkpaused.md) -Ereignis
-   [**Onclockstopp**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop): [mestreamsink](mestreamsinkstopped.md) -Ereignis

## <a name="finalizing"></a>Ausführung wird abgeschlossen

Einige Medien senken erfordern einen zusätzlichen Verarbeitungsschritt, nachdem das letzte Beispiel übermittelt wurde. Diese Anforderung gilt in der Regel für Archivierungs senken, bei denen Header oder Indizes in die Datei geschrieben werden müssen. Wenn eine Medien Senke eine abschließende Verarbeitung erfordert, macht Sie die [**imffinalizablemediasink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) -Schnittstelle verfügbar.

Nachdem der Client das letzte Beispiel übermittelt hat, fragt der Client diese Schnittstelle ab. Wenn die Medien Senke die-Schnittstelle unterstützt, ruft der Client [**imffinalizablemediasink:: beginfinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) auf, um die endgültige Verarbeitung asynchron auszuführen. Diese Methode folgt dem Standard Media Foundation asynchronen Model, das in [asynchronen Callback Methods](asynchronous-callback-methods.md)beschrieben wird. Die Medien Senke kann davon ausgehen, dass der Client **beginfinalize** aufruft. Wenn **beginfinalize** nicht aufgerufen wird, kann dies zu einer falsch erstellten Datei führen.

## <a name="shutting-down"></a>Wird heruntergefahren

Wenn der Client mithilfe der Medien Senke ausgeführt wird, ruft der Client [**imfmediasink:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown)auf. Innerhalb dieser Methode sollte die Medien Senke alle Zirkel Verweis Zählungen unterbrechen. In der Regel gibt es zirkuläre Verweise zwischen der Medien Senke und den streamsenken.

Wenn Sie das Hilfsprogramm für die Ereignis Warteschlange verwenden, um [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)zu implementieren, nennen Sie [**imfmediaeventqueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) für die Ereignis Warteschlange. Diese Methode beendet die Ereignis Warteschlange und signalisiert jedem Aufrufer, der zurzeit auf ein Ereignis wartet.

Nach dem Herunterfahren geben alle Methoden der Medien Senke \_ das Herunterfahren von MF E zurück \_ , mit Ausnahme von **IUnknown** -Methoden.

## <a name="media-sink-interfaces"></a>Media Sink-Schnittstellen

In der folgenden Tabelle werden die Standardschnittstellen aufgelistet, die Medien senken über **QueryInterface** verfügbar machen können. Medien senken können auch benutzerdefinierte Schnittstellen verfügbar machen.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | Die primäre Schnittstelle für Medien senken. (Erforderlich.)                                            |
| [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Wird verwendet, um die Medien Senke zu benachrichtigen, wenn sich die Präsentationszeit ändert. (Erforderlich.)              |
| [**Imffinalizablemediasink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implementieren Sie, wenn die Medien Senke einen abschließenden Verarbeitungsschritt ausführen muss. (Optional.)                 |
| [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implementieren Sie, wenn die Medien Senke beliebige Dienst Schnittstellen verfügbar macht. (Optional.)                       |
| [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implementieren Sie, wenn die Medien Senke Ereignisse sendet. (Optional.)                                     |
| [**Imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implementieren Sie, wenn die Medien Senke Preroll unterstützt. (Optional.)                                     |
| [**IMF presentationtimesource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implementieren Sie, wenn die Medien Senke eine Zeit Quelle für die Präsentationszeit bereitstellen kann. (Optional.) |
| [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implementieren Sie, wenn die Medien Senke die Wiedergabequalität anpassen kann. (Optional.)                          |



 

Optional kann eine Medien Senke die folgende Schnittstelle als Dienst implementieren.



| Dienst Schnittstelle                        | BESCHREIBUNG                                    |
|------------------------------------------|------------------------------------------------|
| [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Meldet den Bereich der unterstützten Wiedergabe Raten. |



 

Weitere Informationen zu Dienst Schnittstellen und [**immagetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)finden Sie unter [Dienst Schnittstellen](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Stream Sink-Schnittstellen

Streamsenken müssen die folgenden Schnittstellen über **QueryInterface** verfügbar machen.



| Schnittstelle                                                | BESCHREIBUNG                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMF-Senke**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | Die primäre Schnittstelle für streamsenken. (Erforderlich.)                                                      |
| [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Warteschlangen Ereignisse. Die [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle erbt diese Schnittstelle. (Erforderlich.) |



 

Zurzeit sind keine Dienst Schnittstellen für streamsenken definiert.

## <a name="stream-sink-events"></a>Streamsink-Ereignisse

In der folgenden Tabelle sind die Ereignisse aufgelistet, die für generische streamsenken definiert sind. Streamsenken können auch benutzerdefinierte, hier nicht aufgelistete Ereignisse senden.



| Ereignis                                                                  | BESCHREIBUNG                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [Mestreamsinkformatchanged](mestreamsinkformatchanged.md)             | Der Medientyp der Stream-Senke ist nicht mehr gültig. (Optional.) |
| [Mestreamsink Marker](mestreamsinkmarker.md)                           | Ein Marker wurde verarbeitet. (Erforderlich.)                          |
| [Mestreamsink angehalten](mestreamsinkpaused.md)                           | Die streamsenke wurde angehalten. (Erforderlich.)                      |
| [Mestreamsinkprerolled](mestreamsinkprerolled.md)                     | Die Vorabversion ist fertiggestellt. (Optional.)                             |
| [Mestreamsinkratechanged](mestreamsinkratechanged.md)                 | Die Wiedergabe Rate wurde von der streamsenke geändert. (Optional.)       |
| [Mestreamsinkrequestsample](mestreamsinkrequestsample.md)             | Ein neues Beispiel wird angefordert. (Erforderlich.)                       |
| [Mestreamsinkscrubsamplecomplete](mestreamsinkscrubsamplecomplete.md) | Eine Bereinigungsanforderung wurde abgeschlossen. (Optional.)                   |
| [Mestreamsink Started](mestreamsinkstarted.md)                         | Die streamsenke wurde gestartet. (Erforderlich.)                     |
| [Mestreamsink beendet](mestreamsinkstopped.md)                         | Die streamsenke wurde beendet. (Erforderlich.)                     |



 

Zurzeit sind keine allgemeinen Ereignisse für Medien senken definiert. Einige Medien senken können benutzerdefinierte Ereignisse senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Pipeline](media-foundation-pipeline.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> </dl>

 

 





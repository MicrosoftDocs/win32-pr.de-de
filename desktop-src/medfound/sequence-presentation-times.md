---
description: In diesem Thema wird beschrieben, wie die Sequencerquelle Präsentationszeiten während der Wiedergabe behandelt.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Sequenzpräsentationszeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45ea9c8b315171365810f33bb9a66ca4d223fb2119d7aea19288c3ebdd93ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238366"
---
# <a name="sequence-presentation-times"></a>Sequenzpräsentationszeiten

In diesem Thema wird beschrieben, wie [die Sequencerquelle](sequencer-source.md) Präsentationszeiten während der Wiedergabe behandelt.

## <a name="overview"></a>Übersicht

Die Sequencerquelle unterstützt zwei verschiedene Modi: Wiedergabelistensequenzen und Bearbeitungssequenzen.

In einer Bearbeitungssequenz gibt die Anwendung die Dauer der einzelnen Segmente im Voraus an, bevor die Wiedergabe gestartet wird. In einer Wiedergabelistensequenz gibt die Anwendung die Dauer nicht im Voraus an. (Tatsächlich ist die Dauer möglicherweise nicht bekannt.)

In beiden Fällen können Sie die Start- und Stoppzeit der Medien eines Segments angeben. Diese Zeiten geben die Position in der Quelldatei an, an der das Segment beginnt und endet. Angenommen, die Quelldatei ist 90 Sekunden lang. Wenn Sie die ersten 10 Sekunden und die letzten 10 Sekunden kürzen möchten, geben Sie die folgenden Werte an:

-   Medienstart: 10 Sekunden
-   Medienstopp: 80 Sekunden

Um die Startzeit des Mediums anzugeben, legen Sie das [MF \_ TOPONODE \_ MEDIASTART-Attribut](mf-toponode-mediastart-attribute.md) auf dem Quellknoten fest. Um die Medienstoppzeit anzugeben, legen Sie das [MF \_ TOPONODE \_ MEDIASTOP-Attribut](mf-toponode-mediastop-attribute.md) auf dem Quellknoten fest.

Um eine Bearbeitungssequenz zu erstellen, legen Sie beim Erstellen der Mediensitzung das [MF \_ SESSION GLOBAL \_ \_ TIME-Attribut](mf-session-global-time-attribute.md) fest. Andernfalls erwartet die Mediensitzung Wiedergabelistensequenzen. In einer Bearbeitungssequenz muss jede Segmenttopologie über das [MF \_ TOPOLOGY \_ PROJECTSTART-Attribut](mf-topology-projectstart-attribute.md) und das [MF \_ TOPOLOGY \_ PROJECTSTOP-Attribut](mf-topology-projectstop-attribute.md) verfügen.

## <a name="playlist-sequences"></a>Wiedergabelistensequenzen

In einer Wiedergabelistensequenz beginnt die Präsentationsuhr bei 0 (null) und wird über Segmentgrenzen hinweg fortgesetzt. Die nativen Quellen liefern Beispiele mit Zeitstempeln, die der Medienzeit entspricht. Die Pipeline konvertiert die Zeitstempel wie folgt in die richtige Präsentationszeit:

-   Neuer Zeitstempel = Medienzeit + Offset – Medienstart

Der Offsetwert *ist* die Präsentationszeit, zu der das vorherige Segment beendet wurde. Für das erste Segment ist der Offset 0 (null). Im Folgenden finden Sie zwei Beispiele für die Berechnung dieser Zeitstempelkonvertierungen:

-   Beispiel 1: Angenommen, das erste Segment (S1) ist 10 Sekunden lang, und das zweite Segment (S2) hat eine Medienstartzeit von 0 (null). Die native Quelle verwendet die Medienzeit für ihre Zeitstempel, sodass die erste Stichprobe von S2 einen Zeitstempel von 0 hat. Der Offset beträgt 10 Sekunden (die Dauer von S1), sodass der angepasste Zeitstempel:0 + 10 × 0 = 10 Sekunden ist.
-   Beispiel 2: Angenommen, das Segment S1 ist 10 Sekunden lang, und S2 hat eine Medienstartzeit von 5 Sekunden. Das erste Beispiel von S2 hat einen Zeitstempel von 5 Sekunden (Medienzeit). Der Offset beträgt 10 Sekunden, sodass der angepasste Zeitstempel:5 + 10 × 5 = 10 Sekunden ist.

Alle Pipelinekomponenten, die nach den Quellknoten nachgelagert sind, erhalten Stichproben mit den angepassten Zeitstempeln. Die Quellknoten in einer Topologie können unterschiedliche Startzeiten für Medien haben, sodass die Anpassungen für jeden Branch der Topologie separat berechnet werden.

Wenn die Präsentation zum nächsten Segment wechselt, wird die Präsentationsuhr nicht an- oder zurückgesetzt, und die Präsentationszeit erhöht sich monoton. Bevor ein neues Segment gestartet wird, sendet die Mediensitzung der Anwendung ein [MESessionNotifyPresentationTime-Ereignis.](mesessionnotifypresentationtime.md) Das -Ereignis gibt die Startzeit des Segments relativ zur Präsentationsuhr und den Wert des Offsets an. Wenn ein neues Segment gestartet wird, ruft die Pipeline [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) für die Sequencerquelle mit dem Wert VT \_ EMPTY auf. Die Sequencerquelle sendet ein [MESourceStarted-Ereignis](mesourcestarted.md) ohne Startzeit.

Für die Suche gibt die Anwendung einen Segmentbezeichner plus einen Zeitoffset innerhalb des Segments an. Nach der Suche beginnt die Präsentationsuhr am *Segmentoffset.* Hier ist ein Beispiel für die Funktionsweise dieses Prozesses:

-   Beispiel 3: Die Anwendung versucht, S3 mit einem Segmentoffset von 10 Sekunden zu segmentieren. Die Präsentationsuhr beginnt bei 10 Sekunden (Segmentoffset). Der Offset enthält nicht die Dauer der Segmente S1 und S2. Die Sequencerquelle sendet ein [MESourceStarted-Ereignis](mesourcestarted.md) mit einer Startzeit, die dem Segmentoffset von 10 Sekunden entspricht.

Wenn die Wiedergabe nach einer Suche mit dem nächsten Segment fortgesetzt wird, funktioniert der Übergang wie in den vorherigen Beispielen, mit der Ausnahme, dass der Offset die übersprungenen Segmente nicht enthält.

Hier sind einige weitere Details, die sich darauf auswirken, wie Stichproben mit einem Zeitstempel versehen werden:

-   Decoder benötigen möglicherweise Daten, die über die Medienstoppzeit hinausgehen. Die Pipeline pullt so viele Daten aus der Quelle, wie der Decoder erfordert, und entfernt dann die Ausgabebeispiele des Decoders.
-   Transformationen können Daten puffern. Dies kann beispielsweise bei einem Audioeffekt der Fall sein. Wenn ein Segment endet, liegt der Zeitstempel der letzten Stichprobe aus der Transformation vor dem Ende des Segments, da die Transformation einige Daten zurückbehaltung. Wenn das nächste Segment gestartet wird, liegt der Zeitstempel der ersten Stichprobe etwas vor dem Start des Segments. Es gibt keine Lücke in den Zeitstempeln, sodass die Daten, die die Mediensenke erreichen, fortlaufend sind. Wenn das letzte Segment endet, entleert die Pipeline die Transformation, sodass keine Daten verloren gehen.
-   Die Quelle muss möglicherweise etwas früher als die Startzeit des Mediums beginnen, um den vorherigen Keyframe zu verwenden. Daher kann die erste Stichprobe nach der Anpassung eine negative Präsentationszeit haben.

## <a name="editing-sequences"></a>Bearbeiten von Sequenzen

In einer Bearbeitungssequenz gibt die Anwendung die Segmentgrenzen im Voraus an, indem die [**Attribute MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) und [**MF \_ TOPOLOGY \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) festgelegt werden. Die Pipeline berechnet Anpassungen für die Zeitstempel fast auf die gleiche Weise wie für eine Wiedergabelistensequenz:

-   Für den Offset wird der Wert von [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)verwendet, anstatt das beobachtete Ende des Segments zu verwenden.

-   Für die Suche verwendet der Offset einen Wert, der dem [**MF \_ TOPOLOGY \_ PROJECTSTART-Wert**](mf-topology-projectstart-attribute.md) des Segments plus dem Segmentoffset entspricht.

Daher ist die Präsentationszeit in einer Bearbeitungssequenz immer relativ zum Beginn der Präsentation, auch wenn die Anwendung nach einem anderen Segment sucht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 




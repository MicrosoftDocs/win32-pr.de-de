---
description: In diesem Thema wird beschrieben, wie die Sequencer-Quelle Präsentations Zeiten während der Wiedergabe behandelt.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Sequenz Präsentations Zeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17f5b0ff4bd6f0cfee2b1b461d6fbd11bdbf0fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527836"
---
# <a name="sequence-presentation-times"></a>Sequenz Präsentations Zeiten

In diesem Thema wird beschrieben, wie die [Sequencer-Quelle](sequencer-source.md) Präsentations Zeiten während der Wiedergabe behandelt.

## <a name="overview"></a>Übersicht

Die Sequencer-Quelle unterstützt zwei verschiedene Modi: Wiedergabelisten Sequenzen und Bearbeitungs Sequenzen.

In einer Bearbeitungs Sequenz gibt die Anwendung die Dauer der einzelnen Segmente im Voraus an, bevor die Wiedergabe gestartet wird. In einer Wiedergabelisten Sequenz wird die Dauer von der Anwendung nicht im Voraus angegeben. (Die Dauer ist möglicherweise nicht bekannt.)

In beiden Fällen können Sie den Medien Start des Segments und die Endzeit des Mediums angeben. Diese Zeiten geben die Position in der Quelldatei an, an der das Segment beginnt und endet. Nehmen wir beispielsweise an, dass die Quelldatei 90 Sekunden lang ist. Wenn Sie die ersten 10 Sekunden und die letzten 10 Sekunden kürzen möchten, geben Sie die folgenden Werte an:

-   Medien Start: 10 Sekunden
-   Medien Ende: 80 Sekunden

Legen Sie zum Angeben der Start Zeit des Mediums das [MF- \_ toponode \_ mediastart](mf-toponode-mediastart-attribute.md) -Attribut für den Quellknoten fest. Um die Endzeit des Mediums anzugeben, legen Sie das [MF- \_ toponode \_ mediastop](mf-toponode-mediastop-attribute.md) -Attribut für den Quellknoten fest.

Wenn Sie eine Bearbeitungs Sequenz erstellen möchten, legen Sie das [ \_ \_ globale \_ Zeit](mf-session-global-time-attribute.md) Attribut der MF-Sitzung fest, wenn Sie die Medien Sitzung erstellen. Andernfalls erwartet die Medien Sitzung Wiedergabelisten Sequenzen. In einer Bearbeitungs Sequenz muss jede Segment Topologie über das Projekt für die [MF- \_ \_ TopologieTopologie](mf-topology-projectstart-attribute.md) und das [Projekt "MF- \_ Topologie \_ Projectplace](mf-topology-projectstop-attribute.md) " verfügen.

## <a name="playlist-sequences"></a>Wiedergabelisten Sequenzen

In einer Wiedergabelisten Sequenz beginnt die Präsentations Uhr bei Null und wird über Segment Grenzen hinweg fortgesetzt. Die nativen Quellen liefern Beispiele mit Zeitstempeln, die der Medien Zeit entsprechen. Die Pipeline konvertiert die Zeitstempel wie folgt in die richtige Präsentationszeit:

-   Neuer Zeitstempel = Medien Zeit + Offset − Medien Start

Der Wert von *Offset* ist die Präsentationszeit, zu der das vorherige Segment beendet wurde. Für das erste Segment ist der Offset 0 (null). Im folgenden finden Sie zwei Beispiele für die Berechnung dieser Zeitstempel Konvertierungen:

-   Beispiel 1: angenommen, das erste Segment (S1) ist 10 Sekunden lang, und das zweite Segment (S2) hat eine Medien Start Zeit von 0 (null). Die native Quelle verwendet die Medien Zeit für Ihre Zeitstempel, sodass das erste Beispiel von S2 den Zeitstempel 0 (null) aufweist. Der Offset beträgt 10 Sekunden (die Dauer S1), daher beträgt der angepasste Zeitstempel: 0 + 10 − 0 = 10 Sekunden.
-   Beispiel 2: angenommen, das Segment S1 ist 10 Sekunden lang, und S2 hat eine Medien Start Zeit von 5 Sekunden. Das erste Beispiel von S2 weist einen Zeitstempel von 5 Sekunden (Medien Zeit) auf. Der Offset beträgt 10 Sekunden, sodass der angepasste Zeitstempel: 5 + 10 − 5 = 10 Sekunden ist.

Alle Pipeline Komponenten, die von den Quellknoten nachgelagert werden, erhalten Stichproben mit den angepassten Zeitstempeln. Die Quellknoten in einer Topologie können unterschiedliche Startzeiten für Medien aufweisen, sodass die Anpassungen für jede Verzweigung der Topologie separat berechnet werden.

Wenn die Präsentation zum nächsten Segment wechselt, wird die Präsentations Uhr nicht beendet oder zurückgesetzt, und die Präsentationszeit nimmt monoton zu. Bevor ein neues Segment gestartet wird, sendet die Medien Sitzung der Anwendung ein [mesessionnotifypresentationtime](mesessionnotifypresentationtime.md) -Ereignis. Das-Ereignis gibt die Startzeit des Segments relativ zur Präsentations Uhr und den Wert des Offsets an. Wenn ein neues [**Segment gestartet wird, ruft die**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Pipeline auf der Sequencer-Quelle auf, wobei der Wert VT \_ leer ist. Die Sequencer-Quelle sendet ein [mesourcestarted](mesourcestarted.md) -Ereignis ohne Startzeit.

Zum Suchen gibt die Anwendung einen Segment Bezeichner zuzüglich eines Zeit Offsets innerhalb des Segments an. Nach der Suche beginnt die Präsentations Uhr am *Segment* Offset. Im folgenden finden Sie ein Beispiel für die Funktionsweise dieses Prozesses:

-   Beispiel 3: die Anwendung versucht, S3 mit einem Segment Offset von 10 Sekunden zu segmentieren. Die Präsentations Uhr beginnt bei 10 Sekunden (Segment Offset). Der Offset umfasst nicht die Dauer der Segmente S1 und S2. Die Sequencer-Quelle sendet ein [mesourcestarted](mesourcestarted.md) -Ereignis mit einer Startzeit, die gleich dem Segment Offset ist, 10 Sekunden.

Wenn die Wiedergabe im nächsten Segment fortgesetzt wird, funktioniert der Übergang wie in den vorherigen Beispielen, mit dem Unterschied, dass der Offset nicht die übersprungenen Segmente enthält.

Im folgenden finden Sie weitere Details, die beeinflussen, wie Beispiele mit Zeitstempel versehen werden:

-   Decoder benötigen möglicherweise Daten, die über die Endzeit des Mediums hinausgehen. Die Pipeline ruft so viele Daten aus der Quelle ab, wie der Decoder erfordert, und gibt dann die Ausgabe Beispiele des Decoders aus.
-   Transformationen können Daten Puffern. Beispielsweise ist ein Audioeffekt möglicherweise erforderlich. Wenn ein Segment endet, liegt der Zeitstempel für das letzte Beispiel aus der Transformation vor dem Ende des Segments, da die Transformation einige Daten zurückgibt. Wenn das nächste Segment gestartet wird, ist der Zeitstempel im ersten Beispiel etwas niedriger als der Anfang des Segments. Es gibt keine Lücke in den Zeitstempeln, sodass die Daten, die die Medien Senke erreichen, kontinuierlich sind. Wenn das abschließende Segment endet, zieht die Pipeline die Transformation, sodass keine Daten verloren gehen.
-   Die Quelle muss möglicherweise vor der Start Zeit des Mediums beginnen, um den vorherigen Keyframe zu übernehmen. Daher kann das erste Beispiel nach der Anpassung eine negative Präsentationszeit haben.

## <a name="editing-sequences"></a>Bearbeiten von Sequenzen

In einer Bearbeitungs Sequenz gibt die Anwendung die Segment Grenzen im Voraus an, indem Sie die Projekt-und die MF-TopologieTopologie [**\_ \_ ProjectStart**](mf-topology-projectstop-attribute.md) -Attribute festlegt. [**\_ \_**](mf-topology-projectstart-attribute.md) Die Pipeline berechnet die Anpassungen für die Zeitstempel auf fast die gleiche Weise wie für eine Wiedergabelisten Sequenz:

-   Für den Offset wird der Wert der MF- [**\_ Topologie \_ ProjectStart**](mf-topology-projectstart-attribute.md)verwendet, anstatt das beobachtete Ende des Segments zu verwenden.

-   Für die Suche verwendet der Offset einen Wert, der gleich dem Wert für den [**MF- \_ \_ topologietopologiewert**](mf-topology-projectstart-attribute.md) des Segments plus dem Segment Offset ist.

Daher ist die Präsentationszeit in einer Bearbeitungs Sequenz immer relativ zum Anfang der Präsentation, auch wenn die Anwendung zu einem anderen Segment sucht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 




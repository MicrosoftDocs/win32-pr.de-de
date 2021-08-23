---
description: Der Satz aller Stimmen mit ihren enthaltenen Effekten und ihren Verbindungen wird als Audioverarbeitungsgraph bezeichnet.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 Audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b461b89095152f3f8073a09a230e18f5e30fd7f42ffb60b4c45a32702094f70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707020"
---
# <a name="xaudio2-audio-graph"></a>XAudio2 Audio Graph

Der Satz aller Stimmen mit ihren enthaltenen Effekten und ihren Verbindungen wird als Audioverarbeitungsgraph bezeichnet. Das Diagramm verwendet eine Reihe von Audiostreams vom Client als Eingabe, verarbeitet sie und übermittelt das Endergebnis an ein Audiogerät. Die gesamte Audioverarbeitung erfolgt in einem separaten Thread mit einer Periodizität, die vom Quanten des Graphen definiert wird (derzeit 10 Millisekunden auf Microsoft Windows und 5 1/3 Millisekunden auf Xbox 360). Jede Quanten-Millisekunde wird der Thread aktiviert und verteilt Quanten-Millisekunden von Audiodaten über den gesamten Graphen. Ein Beispiel für die Erstellung eines einfachen Audiographen finden Sie unter Vorgehensweise: [Erstellen einer einfachen Audioverarbeitung Graph](how-to--build-a-basic-audio-processing-graph.md).

Ein einfacher Audiograph:

![ein einfaches Audiodiagramm](images/xaudio2-audio-graph.png)

Der Client kann den Zustand des Graphen dynamisch steuern, während er ausgeführt wird. Steuerungsaktionen können das Hinzufügen und Entfernen von Eingaben und Ausgaben, das Ändern der internen Effekte und Verbindungen, das Festlegen von Parametern für die Auswirkungen, das Aktivieren und Deaktivieren von Teilen des Diagramms usw. umfassen. Ein Beispiel für das dynamische Ändern eines Audiographen finden Sie unter [Vorgehensweise: Dynamisches Hinzufügen oder Entfernen von Stimmen aus einem Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).

## <a name="processing-the-graph"></a>Verarbeiten der Graph

Jeder Methodenaufruf, der sich auf ein Objekt im Graphen auswirkt, wird als Auswirkung auf eine Änderung des Diagrammzustands betrachtet. Graph Zustandsänderungen umfassen Folgendes:

-   Erstellen und Zerstören von Stimmen
-   Starten oder Beenden von Stimmen
-   Ändern der Ziele einer Stimme
-   Ändern von Effektketten
-   Aktivieren oder Deaktivieren von Effekten
-   Festlegen von Parametern für die Auswirkungen oder die integrierten SRCs, Filter, Volumes und Mixer

Jeder Satz von Diagrammzustandsänderungen kann kombiniert und als atomare Transaktion ausgeführt werden. Diese atomaren Vorgänge werden als Vorgangssätze bezeichnet. Sie werden in der Übersicht über [XAudio2-Vorgangssätze](xaudio2-operation-sets.md) erläutert.

## <a name="internal-data-representation"></a>Interne Datendarstellung

Audiodaten im XAudio2-Diagramm werden immer in 32-Bit-Gleitkomma-PCM-Form gespeichert und verarbeitet. Die Kanalanzahl und die Abtastrate können jedoch innerhalb des Diagramms variieren. Das Format, in dem eine bestimmte Stimme Audiodaten verarbeitet, wird durch den Sprachtyp und die Parameter bestimmt, die zum Erstellen der Stimme verwendet werden.



| Sprachtyp                                                                                                      | Parameter                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | Die Kanalanzahl und die Abtastrate der Stimmen, an die die Quellstimme Audiodaten sendet.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) und [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Die Argumente *InputChannels* und *InputSampleRate,* die zum Erstellen der Submix/Mastering-Stimme verwendet werden. |



 

## <a name="format-conversion"></a>Formatkonvertierung

XAudio2 verarbeitet alle Abtastraten- oder Kanalkonvertierungen, die erforderlich sind, wenn Audio von einer Stimme in eine andere übertragen wird, mit den folgenden Einschränkungen:

-   Alle Zielstimmen für eine bestimmte Stimme müssen mit derselben Abtastrate ausgeführt werden.
-   Effekte in einer Effektkette können die Kanalanzahl des Audios ändern, jedoch nicht die Abtastrate.
-   Die Ausgabekanalanzahl einer Effektkette muss mit der Anzahl der Stimmen übereinstimmen, an die sie gesendet wird.
-   Es kann keine dynamische Graphänderung vorgenommen werden, die die oben genannten Regeln unterbrechen würde.

Auf der Eingabeseite können Quellstimmen Daten in einem beliebigen gültigen PCM-Format oder in einem der von XAudio2 unterstützten komprimierten Formate lesen. Wenn die Eingabedaten komprimiert sind, werden sie zu Gleitkomma-PCM decodiert, bevor eine weitere Verarbeitung erfolgt.

Auf der Ausgabeseite können Masteringstimmen nur PCM-Daten erzeugen. Diese Daten erfüllen immer die oben beschriebenen Einschränkungen für PCM-Eingabedaten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiographen](audio-graphs.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[So wird's gemacht: Verwenden von Submixstimmen](how-to--use-submix-voices.md)
</dt> <dt>

[So wird's gemacht: Erstellen einer Effektkette](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 




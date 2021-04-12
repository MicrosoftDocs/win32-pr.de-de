---
description: Der Satz aller Stimmen mit den darin enthaltenen Effekten und deren Verbindungen wird als audioverarbeitungsgraph bezeichnet.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2-audiodiagramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218556"
---
# <a name="xaudio2-audio-graph"></a>XAudio2-audiodiagramm

Der Satz aller Stimmen mit den darin enthaltenen Effekten und deren Verbindungen wird als audioverarbeitungsgraph bezeichnet. Das Diagramm übernimmt eine Reihe von Audiodatenströmen vom Client als Eingabe, verarbeitet sie und übergibt das Endergebnis an ein Audiogerät. Die gesamte Audioverarbeitung erfolgt in einem separaten Thread mit einer Periodizität, die durch das Quantum des Diagramms definiert wird (derzeit 10 Millisekunden unter Microsoft Windows und 5 1/3 Millisekunden auf Xbox 360). Jede Quantum-Millisekunde wird der Thread reaktiviert und die Quantum-Millisekunden der Audiodaten über das gesamte Diagramm verteilt. Ein Beispiel für das Erstellen eines einfachen audiodiagramms finden Sie unter Gewusst wie: [Erstellen eines einfachen audioverarbeitungdiagramms](how-to--build-a-basic-audio-processing-graph.md).

Ein einfaches audiodiagramm:

![ein einfaches audiodiagramm](images/xaudio2-audio-graph.png)

Der Client kann den Status des Diagramms dynamisch steuern, während er ausgeführt wird. Steuerungs Aktionen können das Hinzufügen und Entfernen von Eingaben und Ausgaben, das Ändern der internen Effekte und der Verbindungen, das Festlegen von Parametern für die Effekte, das Aktivieren und Deaktivieren von Teilen des Diagramms usw. umfassen. Ein Beispiel für das dynamische Ändern eines audiodiagramms finden [Sie unter Gewusst wie: Dynamisches Hinzufügen oder Entfernen von Stimmen aus einem audiodiagramm](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).

## <a name="processing-the-graph"></a>Verarbeiten des Diagramms

Jeder Methodenaufruf, der sich auf ein Objekt im Diagramm auswirkt, wird als Auswirkung einer Diagramm Zustandsänderung betrachtet. Die Änderungen des Graph-Zustands umfassen Folgendes:

-   Erstellen und zerstören von Stimmen
-   Starten oder Beenden von Stimmen
-   Ändern der Ziele einer Stimme
-   Ändern von Effektketten
-   Aktivieren oder Deaktivieren von Effekten
-   Festlegen von Parametern für die Auswirkungen oder die integrierten SRCS, Filter, Volumes und Mixer

Jeder Satz von Diagramm Zustandsänderungen kann kombiniert und als atomarische Transaktion ausgeführt werden. Diese atomaren Vorgänge werden als Vorgangs Sätze bezeichnet. Diese werden in der Übersicht über [XAudio2-Vorgangs Sätze](xaudio2-operation-sets.md) erläutert.

## <a name="internal-data-representation"></a>Interne Datendarstellung

Audiodaten innerhalb des XAudio2-Diagramms werden stets in 32-Bit-PCM-Gleit Komma Formularen gespeichert und verarbeitet. Allerdings können die Anzahl der Kanäle und die Stichprobenrate innerhalb des Diagramms variieren. Das Format, in dem eine bestimmte Stimme das audioverfahren verarbeitet, wird durch den voicetype und die Parameter bestimmt, die zum Erstellen der Stimme verwendet werden.



| Sprachtyp                                                                                                      | Parameter                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | Die Anzahl der Kanäle und die Samplingrate der Stimmen, an die die Quell Stimme Audiodaten sendet.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) und [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Die *inputchannels* -und *inputsamplerate* -Argumente, die zum Erstellen der unter Mischung/der Mastering-Stimme verwendet werden. |



 

## <a name="format-conversion"></a>Format Konvertierung

XAudio2 verarbeitet jede Samplingrate oder Kanal Konvertierungen, die bei der Audioübertragung von einer Sprache zu einer anderen erforderlich sind, wobei die folgenden Einschränkungen gelten:

-   Alle Ziel Stimmen für eine bestimmte Stimme müssen mit der gleichen Stichprobenrate ausgeführt werden.
-   Auswirkungen in einer Effekt Kette können die Kanalanzahl der Audiodaten ändern, aber nicht die Abtastrate.
-   Die Anzahl der Ausgabekanäle einer Effekt Kette muss mit der Anzahl der von ihr gesendeten Stimmen identisch sein.
-   Es kann keine dynamische Diagramm Änderung vorgenommen werden, die die oben genannten Regeln unterbricht.

Auf der Eingabe Seite können Quell Stimmen Daten in jedem gültigen PCM-Format oder in einem der komprimierten Formate lesen, die von XAudio2 unterstützt werden. Wenn die Eingabedaten komprimiert werden, werden Sie vor der weiteren Verarbeitung in ein Gleit Komma-PCM decodiert.

Auf der Ausgabe Seite können durch Mastering Stimmen nur PCM-Daten erzeugt werden. Diese Daten erfüllen immer die gleichen Einschränkungen, die oben für die Eingabe von PCM-Daten beschrieben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiodiagramme](audio-graphs.md)
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

 

 




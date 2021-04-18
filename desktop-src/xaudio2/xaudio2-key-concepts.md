---
description: In dieser Übersicht werden einige wichtige Konzepte für die Verwendung von XAudio2 vorgestellt.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: XAudio2 Schlüsselkonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351061"
---
# <a name="xaudio2-key-concepts"></a>XAudio2 Schlüsselkonzepte

In dieser Übersicht werden einige wichtige Konzepte für die Verwendung von XAudio2 vorgestellt.

-   [XAudio2-Engine](#xaudio2-engine)
-   [Stimmen](#voices)
-   [Audiodiagramm](#audio-graph)
-   [Rückrufe](#callbacks)
-   [Verwandte Themen](#related-topics)

## <a name="xaudio2-engine"></a>XAudio2-Engine

Die [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)-Schnittstelle bildet den Kern des XAudio2-Moduls. Das Erstellen einer Instanz der **IXAudio2** -Schnittstelle ermöglicht es dem Client, die verfügbaren Audiogeräte aufzuzählen, globale API-Eigenschaften zu konfigurieren, stimmen zu erstellen und die Leistung zu überwachen. Die [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) Helper-Funktion führt Instanziierung und Initialisierungs Aufgaben für XAudio2 aus.

Sie können Instanzen von XAudio2 mehrmals innerhalb eines einzelnen Prozesses erstellen. Jedes XAudio2-Objekt wird unabhängig voneinander betrieben und verfügt über einen eigenen audioverarbeitungsthread. Nur die Debugeinstellungen werden freigegeben. Dies ist unter Windows wichtig, wenn mehrere verschiedene Komponenten in einem einzelnen Prozess geladen werden können. Internet Explorer kann z. b. mehrere XAudio2-Komponenten gleichzeitig verwenden. Obwohl es möglich ist, mehrere XAudio2-Engine-Objekte innerhalb einer einzelnen Client Anwendung zu erstellen, sollten Sie keine Informationen zwischen den jeweiligen Diagrammen übergeben.

Ein Beispiel für das Initialisieren der XAudio2-Engine finden [Sie unter Gewusst wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md).

## <a name="voices"></a>Stimmen

Stimmen sind die Objekte, die XAudio2 zur Verarbeitung, Bearbeitung und Wiedergabe von Audiodaten verwendet werden. In XAudio2 gibt es drei Arten von Stimmen.

-   [**Quellen Stimmen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Quell Stimmen stellen einen Stream von Audiodaten dar. Quell Stimmen senden Ihre Daten an andere Arten von Stimmen.

-   [**Teilmengen von Stimmen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Teilmischungs Stimmen führen eine gewisse Bearbeitung der Audiodaten aus, die Sie erhalten. Ein Beispiel für die Bearbeitung von Audiodaten könnte eine Stichproben Raten Konvertierung sein. Nachdem eine unter Mischungs Sprache Daten verarbeitet hat, übergibt Sie diese Daten an eine andere Teil Mischungs Stimme oder an eine Master Stimme.

-   [**Meistern von Stimmen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    Durch das beherrschen von Stimmen erhalten Sie Daten aus Quell Stimmen und Teil Mischungs Stimmen und sendet diese Daten an die Audiohardware.

Unter [XAudio2 Voices](voices.md) finden Sie eine Übersicht über XAudio2 Stimmen.

## <a name="audio-graph"></a>Audiodiagramm

Ein audiodiagramm ist eine Sammlung von XAudio2 Stimmen. Audiodaten werden an einer Seite eines audiodiagramms in den Quell Stimmen gestartet. optional wird eine oder mehrere Teil Mischungs Stimmen durchlaufen, und eine Stimme an. Ein audiodiagramm enthält eine Quell Stimme für jeden aktuell wiedergegebenen Sound, 0 (null) oder mehr Teil Mischungs Stimmen und eine Stimme. Das einfachste audiodiagramm und die Mindestanforderungen für die Durchführung eines Rauschens in XAudio2 ist eine einzelne Quelle, die direkt auf eine Mastering-Stimme aussteht. Ein Beispiel für die minimalen Schritte, die zur Wiedergabe eines Sounds mit XAudio2 erforderlich sind, finden Sie unter Gewusst [wie: Wiedergeben eines Sounds mit XAudio2](how-to--play-a-sound-with-xaudio2.md) .

Eine Übersicht über XAudio2-audiodiagramme finden Sie unter [XAudio2-audiodiagramm](audio-graphs.md) .

## <a name="callbacks"></a>Rückrufe

Rückrufe sind der Mechanismus, den XAudio2 verwendet, um Client Code zu signalisieren, dass ein Ereignis in einer Stimme oder im Engine-Objekt aufgetreten ist. Da die Audiowiedergabe in der XAudio2-Engine asynchron ist, stellen Rückrufe die einzige Möglichkeit dar, zu bestimmen, wann die Wiedergabe eines Sounds abgeschlossen ist.

Eine Übersicht über XAudio2-Rückrufe finden Sie unter [XAudio2](callbacks.md) -Rückrufe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[XAudio2-Versionen](xaudio2-versions.md)
</dt> <dt>

[So wird's gemacht: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Gewusst wie: Wiedergabe eines Sounds mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 




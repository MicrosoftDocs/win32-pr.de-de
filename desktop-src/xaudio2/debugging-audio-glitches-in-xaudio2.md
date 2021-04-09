---
description: Fehler können in XAudio2 auftreten. in diesem Thema wird erläutert, wie Sie gemeldet werden, und es gibt einige Ansätze zur Behebung dieser Fehler.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debuggen von Audiostörungen in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866495"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Debuggen von Audiostörungen in XAudio2

Fehler können in XAudio2 auftreten. in diesem Thema wird erläutert, wie Sie gemeldet werden, und es gibt einige Ansätze zur Behebung dieser Fehler.

In dieser Übersicht werden die folgenden Themen behandelt:

-   [Ursachen für audioausgabeprobleme oder-Ausfälle](#causes-of-audio-output-problems-or-glitches)
-   [So meldet XAudio2 Probleme](#how-xaudio2-reports-problems)
-   [Ansätze zum Beheben von Problemen](#approaches-to-fixing-problems)
-   [Zugehörige Themen](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Ursachen für audioausgabeprobleme oder-Ausfälle

In der XAudio2-Ausgabe können aus verschiedenen Gründen Fehler auftreten.

-   Eine XAudio2-Quellsprache wird verhungert. Der Client sendet nicht schnell genug neue Audiodaten. Sie erhalten eine Ruhe, weil Sie keine Daten für die Wiedergabe hat.
-   XAudio2 als Ganzes ist überlastet. Es dauert länger als *x* MS, bis *x* MS Audiodaten erzeugt werden. Sie erhalten Dropouts, weil XAudio2 keine Daten so schnell wie möglich mit dem Audiogerät erzeugt. Möglicherweise führen Sie zu viele Stimmen oder Effekte gleichzeitig aus, arbeiten in XAudio2-Rückrufen oder XAudio2-API-aufrufen zu häufig.
-   Der Audioverarbeitungs Thread wird nicht ausgeführt, da die Implementierung eines XAudio2-Rückrufs durch den Client Dinge bewirkt, die den Thread blockieren können. Beispielsweise kann der Zugriff auf den Datenträger erfolgen, mit anderen Threads synchronisiert oder andere Funktionen aufgerufen werden, die blockieren können. Verwenden Sie einen Hintergrund Thread mit niedrigerer Priorität, den der Rückruf signalisieren kann, um solche Aufgaben auszuführen.
-   Das System wird als Ganzes überladen. Andere Threads, die mit der gleichen oder einer höheren Priorität als XAudio2 ausgeführt werden, funktionieren zu viel. Sie konkurrieren mit dem audiothread für die CPU-Zeit.

## <a name="how-xaudio2-reports-problems"></a>So meldet XAudio2 Probleme

XAudio2 kann im Debugbuild auf verschiedene Weise auf eine Weise kommunizieren.

-   Wenn eine Stimme verhungert wird, wird in XAudio2 eine Meldung in dieser Form angezeigt.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Wenn der audiothread zu lange ausgeführt wird, wird in XAudio2 eine Meldung in dieser Form angezeigt.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    In der Regel wird diese Meldung mit der nächsten Meldung angezeigt.

-   Wenn der Audiotreiber nicht rechtzeitig mit neuen Audiodaten versorgt werden kann, wird in XAudio2 eine Meldung in dieser Form angezeigt.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   Durch Aufrufen von [**IXAudio2:: getperformancedata**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) werden XAudio2-Leistungsdaten bereitstellt, einschließlich der Gesamtzahl der seit dem Start der XAudio2-Engine erstellten Fehler.

## <a name="approaches-to-fixing-problems"></a>Ansätze zum Beheben von Problemen

Es gibt folgende Möglichkeiten, um audioglime zu reduzieren:

-   Bei der sprach Hungersnot: erhöhen Sie die Menge an Audiodaten, die in der Warteschlange einer Stimme in der Warteschlange stehen. Sie können [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) verwenden, um die Anzahl der Puffer zu ermitteln, die in der Warteschlange stehen. Wenn weiterhin Probleme mit der sprach Hungersnot angezeigt werden, aber keine Fehler auftreten, stellen Sie sicher, dass Sie [**XAUDIO2 \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)festlegen.**Flags** zum XAUDIO2- \_ Ende \_ des \_ Streams im letzten Puffer eines Sounds. Dies weist darauf hin, dass XAudio2 nicht zu erwarten ist, dass mehr Puffer unbedingt verfügbar sind, sobald dieser Vorgang abgeschlossen ist.

    In den anderen Fällen:

    -   Reduzieren Sie die Anzahl aktiver Stimmen und Effekte im Diagramm, insbesondere teure Effekte wie "Hall".
    -   Deaktivieren Sie stimmen und Effekte, die Sie nicht verwenden.
    -   Verwenden Sie nach \_ Möglichkeit die Flags "XAUDIO2 Voice \_ nosrc" und "XAUDIO2 \_ Voice \_ nopitch" in [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Die Stichproben Raten Konvertierung ist aufwendig.
    -   Reduzieren Sie die Stichprobenrate einzelner Stimmen. Beispielsweise kann eine unter Mischungs Stimme, die einen Hall-Effekt als Host hat, eine niedrigere Samplingrate aufweisen als die an Sie gesendete Quell Stimme. Sounds, wie z. b. Explosionen und schießshots, die keine hohe Treue erfordern, können auch zu niedrigeren Stichproben Raten aufgezeichnet werden.
    -   Stellen Sie sicher, dass Rückruf Implementierungen so wenig wie möglich funktionieren und nie blockiert werden.
    -   Nehmen Sie weniger Aufrufe an XAudio2 vor. Audioparameter müssen in der Regel nicht für jeden Videorahmen aktualisiert werden. Alle 30 ms sind ausreichend. Sie sollten redundante Aufrufe vermeiden, z. b. das Volume mehrmals in schneller Folge festlegen.
    -   Reduzieren Sie die CPU-Gesamtauslastung des Spiels.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugging-Einrichtungen](debugging-facilities.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 

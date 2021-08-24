---
description: In XAudio2 können Störungen auftreten. In diesem Thema wird erläutert, wie sie gemeldet werden, und es werden einige Ansätze zur Behebung beschrieben.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debuggen von Audiostörungen in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8856defc67bc9453b9d83f5ed369bfb96f48b8c2c16c92ea535a0c1b648402b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703620"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Debuggen von Audiostörungen in XAudio2

In XAudio2 können Störungen auftreten. In diesem Thema wird erläutert, wie sie gemeldet werden, und es werden einige Ansätze zur Behebung beschrieben.

In dieser Übersicht werden die folgenden Themen behandelt:

-   [Ursachen von Audioausgabeproblemen oder -störungen](#causes-of-audio-output-problems-or-glitches)
-   [Wie XAudio2 Probleme meldet](#how-xaudio2-reports-problems)
-   [Ansätze zum Beheben von Problemen](#approaches-to-fixing-problems)
-   [Zugehörige Themen](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Ursachen von Audioausgabeproblemen oder -störungen

Störungen können in der XAudio2-Ausgabe aus verschiedenen Gründen auftreten.

-   Eine XAudio2-Quellstimme ist ausgehungert. Der Client übermittelt nicht schnell genug neue Audiodaten. Sie erhalten Ruhe, da keine Daten wiedergegeben werden müssen.
-   XAudio2 als Ganzes ist überlastet. Es dauert länger als *X* ms, *X* ms Audio zu erzeugen. Sie erhalten Auslassungszeichen, da XAudio2 daten nicht so schnell erzeugen kann, wie das Audiogerät sie benötigt. Möglicherweise führen Sie zu viele Stimmen oder Effekte gleichzeitig aus, erledigen zu viel Arbeit in XAudio2-Rückrufen oder führen zu häufig XAudio2-API-Aufrufe durch.
-   Der Audioverarbeitungsthread wird angehalten, da die Clientimplementierung eines XAudio2-Rückrufs Dinge tut, die den Thread blockieren können. Beispielsweise kann er auf den Datenträger zugreifen, mit anderen Threads synchronisieren oder andere Funktionen aufrufen, die blockieren können. Verwenden Sie einen Hintergrundthread mit niedrigerer Priorität, den der Rückruf signalisieren kann, um solche Aufgaben auszuführen.
-   Das system als Ganzes ist überladen. Andere Threads, die mit derselben oder einer höheren Priorität als XAudio2 ausgeführt werden, führen zu viel Arbeit aus. Sie konkurrieren mit dem Audiothread um CPU-Zeit.

## <a name="how-xaudio2-reports-problems"></a>Wie XAudio2 Probleme meldet

XAudio2 kann Störungen im Debugbuild auf verschiedene Weise kommunizieren.

-   Wenn eine Stimme ausgehungert wird, zeigt XAudio2 eine Nachricht in dieser Form an.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Wenn der Audiothread zu lange ausgeführt wird, zeigt XAudio2 eine Meldung in diesem Format an.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    In der Regel tritt diese Meldung mit der nächsten Nachricht auf.

-   Wenn dem Audiotreiber keine neuen Audiodaten rechtzeitig zugeführt werden können, zeigt XAudio2 eine Meldung in diesem Format an.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   Der Aufruf von [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) stellt XAudio2-Leistungsdaten bereit, einschließlich der Gesamtzahl von Störungen seit dem Start der XAudio2-Engine.

## <a name="approaches-to-fixing-problems"></a>Ansätze zum Beheben von Problemen

Folgende Möglichkeiten zum Reduzieren von Audiostörungen sind möglich.

-   Im Fall des Sprachmangels: Erhöhen Sie die Menge der Audiodaten, die auf einer Stimme in die Warteschlange eingereiht werden. Sie können [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) verwenden, um die Anzahl der Puffer zu ermitteln, die zu einem beliebigen Zeitpunkt in die Warteschlange eingereiht werden. Wenn weiterhin Sprachhungerfehler auftreten, aber keine Störung zu hören ist, stellen Sie sicher, dass Sie [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)festlegen.**Flags** für XAUDIO2 \_ END OF STREAM im \_ \_ endgültigen Puffer eines Sounds. Dies weist XAudio2 an, nicht mehr Puffer zu erwarten, die notwendigerweise verfügbar sind, sobald dieser abgeschlossen ist.

    In den anderen Fällen:

    -   Reduzieren Sie die Anzahl der aktiven Stimmen und Effekte im Diagramm, insbesondere teure Effekte wie Hall.
    -   Deaktivieren Sie Stimmen und Effekte, die Sie nicht verwenden.
    -   Verwenden Sie nach Möglichkeit die \_ \_ NOSRC- und XAUDIO2 \_ VOICE \_ NOPITCH-Flags in [**IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) Die Konvertierung der Stichprobenrate ist teuer.
    -   Reduzieren Sie die Abtastrate einzelner Stimmen. Beispielsweise kann eine Submix-Stimme, die einen Halleffekt hostet, eine niedrigere Abtastrate aufweisen als die Quellstimme, die an sie sendet. Sounds wie Explosionen und Schütze, die keine hohe Genauigkeit benötigen, können auch mit niedrigeren Abtastraten aufgezeichnet werden.
    -   Stellen Sie sicher, dass Rückrufimplementierungen so wenig Arbeit wie möglich leisten und niemals blockieren.
    -   Nehmen Sie weniger Aufrufe an XAudio2 vor. Audioparameter müssen in der Regel nicht für jeden Videoframe aktualisiert werden. Alle 30 ms ist ausreichend. Sie sollten redundante Aufrufe vermeiden, z. B. das mehrmalige Festlegen des Volumes in schneller Folge.
    -   Reduzieren Sie die cpu-Gesamtauslastung des Spiels.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Einrichtungen](debugging-facilities.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 

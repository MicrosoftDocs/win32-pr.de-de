---
description: Die Mindestanforderung zum Aktivieren von XAudio2 für die Wiedergabe von Audiodaten ist ein audioverarbeitungsgraph, das aus einer einzelnen Stimme und einer einzelnen Quelle erstellt wird.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: "So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360656"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms

Die Mindestanforderung zum Aktivieren von XAudio2 für die Wiedergabe von Audiodaten ist ein audioverarbeitungsgraph, das aus einer einzelnen Stimme und einer einzelnen Quelle erstellt wird.

## <a name="to-build-a-basic-audio-processing-graph"></a>So erstellen Sie ein einfaches Audioverarbeitungs Diagramm

1.  Initialisieren Sie die XAudio2-Engine, indem Sie die unter Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)beschriebenen Schritte befolgen.
2.  Füllen Sie eine **WaveFormatEx** -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aus, indem Sie die Schritte befolgen, die unter Gewusst [wie: Laden von audiodatendateien in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md)beschrieben sind.
3.  Erstellen Sie eine Quell Stimme mithilfe der Funktion " [**kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) ".

    Wenn Sie NULL für das psendlist-Argument von " [**kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)" angeben, wird die Ausgabe der Quell Stimme an die in Schritt 1 erstellte "Mastering"-Stimme geleitet.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Nachdem Sie diesen Schritt abgeschlossen haben, gibt es ein einfaches audiodiagramm, das aus der Quell Stimme, der Mastering-Stimme und dem Audiogerät besteht. In den restlichen Schritten in diesem Thema wird gezeigt, wie Sie Audiodaten starten, die über das Diagramm fließen.

    Ein einfaches audiodiagramm

    ![ein einfaches audiodiagramm.](images/xaudio2-audio-graph.png)

4.  Verwenden Sie die Funktion " [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) ", um einen [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quell Stimme zu senden.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Verwenden Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion, um die Quell Stimme zu starten.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiodiagramme](audio-graphs.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 

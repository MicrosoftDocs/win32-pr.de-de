---
description: Die Mindestanforderung, XAudio2 die Wiedergabe von Audiodaten zu ermöglichen, ist ein Audioverarbeitungsgraph, der aus einer einzelnen Masterstimme und einer einzelnen Quellstimme erstellt wird.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: "So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bab39c878b37a6f89ef7598f6fa6b6eb1a997654373122fe3c3980bf12f160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082959"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms

Die Mindestanforderung, XAudio2 die Wiedergabe von Audiodaten zu ermöglichen, ist ein Audioverarbeitungsgraph, der aus einer einzelnen Masterstimme und einer einzelnen Quellstimme erstellt wird.

## <a name="to-build-a-basic-audio-processing-graph"></a>So erstellen Sie ein einfaches Audioverarbeitungsdiagramm

1.  Initialisieren Sie die XAudio2-Engine, indem Sie die unter [How to: Initialize XAudio2 beschriebenen Schritte ausführen.](how-to--initialize-xaudio2.md)
2.  Füllen Sie **eine WAVEFORMATEX-** und [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) auf, indem Sie die unter [How to: Load Audio Data Files in XAudio2 beschriebenen Schritte ausführen.](how-to--load-audio-data-files-in-xaudio2.md)
3.  Erstellen Sie mithilfe der [**CreateSourceVoice-Funktion eine Quellstimme.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

    Wenn Sie NULL für das pSendList-Argument von [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)angeben, wird die Ausgabe der Quellstimme an die in Schritt 1 erstellte Masterstimme übergeben.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Nachdem Sie diesen Schritt abgeschlossen haben, gibt es ein einfaches Audiodiagramm, das aus der Quellstimme, der Masterstimme und dem Audiogerät besteht. In den verbleibenden Schritten in diesem Schritt wird gezeigt, wie Sie mit dem Fließen von Audiodaten durch das Diagramm beginnen.

    Ein einfaches Audiodiagramm

    ![ein einfaches Audiodiagramm.](images/xaudio2-audio-graph.png)

4.  Verwenden Sie die [**Funktion SubmitSourceBuffer,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) um einen [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quellstimme zu übermitteln.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Verwenden [](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) Sie die Start-Funktion, um die Quellstimme zu starten.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiographen](audio-graphs.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 

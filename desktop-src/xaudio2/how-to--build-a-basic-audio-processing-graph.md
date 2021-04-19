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
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="030c7-103">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="030c7-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="030c7-104">Die Mindestanforderung zum Aktivieren von XAudio2 für die Wiedergabe von Audiodaten ist ein audioverarbeitungsgraph, das aus einer einzelnen Stimme und einer einzelnen Quelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="030c7-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="030c7-105">So erstellen Sie ein einfaches Audioverarbeitungs Diagramm</span><span class="sxs-lookup"><span data-stu-id="030c7-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="030c7-106">Initialisieren Sie die XAudio2-Engine, indem Sie die unter Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)beschriebenen Schritte befolgen.</span><span class="sxs-lookup"><span data-stu-id="030c7-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="030c7-107">Füllen Sie eine **WaveFormatEx** -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aus, indem Sie die Schritte befolgen, die unter Gewusst [wie: Laden von audiodatendateien in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md)beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="030c7-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="030c7-108">Erstellen Sie eine Quell Stimme mithilfe der Funktion " [**kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) ".</span><span class="sxs-lookup"><span data-stu-id="030c7-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="030c7-109">Wenn Sie NULL für das psendlist-Argument von " [**kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)" angeben, wird die Ausgabe der Quell Stimme an die in Schritt 1 erstellte "Mastering"-Stimme geleitet.</span><span class="sxs-lookup"><span data-stu-id="030c7-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="030c7-110">Nachdem Sie diesen Schritt abgeschlossen haben, gibt es ein einfaches audiodiagramm, das aus der Quell Stimme, der Mastering-Stimme und dem Audiogerät besteht.</span><span class="sxs-lookup"><span data-stu-id="030c7-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="030c7-111">In den restlichen Schritten in diesem Thema wird gezeigt, wie Sie Audiodaten starten, die über das Diagramm fließen.</span><span class="sxs-lookup"><span data-stu-id="030c7-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="030c7-112">Ein einfaches audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="030c7-112">A simple audio graph</span></span>

    ![ein einfaches audiodiagramm.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="030c7-114">Verwenden Sie die Funktion " [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) ", um einen [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quell Stimme zu senden.</span><span class="sxs-lookup"><span data-stu-id="030c7-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="030c7-115">Verwenden Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion, um die Quell Stimme zu starten.</span><span class="sxs-lookup"><span data-stu-id="030c7-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="030c7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="030c7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030c7-117">Audiodiagramme</span><span class="sxs-lookup"><span data-stu-id="030c7-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="030c7-118">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="030c7-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 

---
description: Sie können Audiodaten in XAudio2 streamen, indem Sie einen separaten Thread erstellen und Puffer Lesevorgänge für die Audiodaten im streamingthread durchführen. verwenden Sie dann Rückrufe, um diesen Thread zu steuern.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: "So wird's gemacht: Streamen von Sound von einem Datenträger"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757687"
---
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="68b35-103">So wird's gemacht: Streamen von Sound von einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="68b35-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="68b35-104">Dieser Inhalt gilt nur für Desktop-Apps und erfordert Revision, damit Sie in einer Windows Store-App funktionieren.</span><span class="sxs-lookup"><span data-stu-id="68b35-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="68b35-105">Weitere Informationen finden Sie in der Dokumentation zu **CreateFile2**, " [forateeventex](/windows/win32/api/synchapi/nf-synchapi-createeventexa)", " [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)", " [setfilepointerex](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)" und " **getoverlappedresultex**".</span><span class="sxs-lookup"><span data-stu-id="68b35-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="68b35-106">Weitere Informationen finden Sie im Beispiel zu streameffect Windows 8 aus der [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="68b35-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="68b35-107">Sie können Audiodaten in XAudio2 streamen, indem Sie einen separaten Thread erstellen und Puffer Lesevorgänge für die Audiodaten im streamingthread durchführen. verwenden Sie dann Rückrufe, um diesen Thread zu steuern.</span><span class="sxs-lookup"><span data-stu-id="68b35-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="68b35-108">Ausführen von Puffer Lesevorgängen im streamingindthread</span><span class="sxs-lookup"><span data-stu-id="68b35-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="68b35-109">Erstellen der Rückruf Klasse</span><span class="sxs-lookup"><span data-stu-id="68b35-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="68b35-110">Ausführen von Puffer Lesevorgängen im streamingindthread</span><span class="sxs-lookup"><span data-stu-id="68b35-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="68b35-111">Führen Sie die folgenden Schritte aus, um die Puffer Lesevorgänge im streamingthread auszuführen:</span><span class="sxs-lookup"><span data-stu-id="68b35-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="68b35-112">Erstellen Sie ein Array von Lese Puffern.</span><span class="sxs-lookup"><span data-stu-id="68b35-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="68b35-113">Initialisieren Sie eine überlappende Struktur.</span><span class="sxs-lookup"><span data-stu-id="68b35-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="68b35-114">Die-Struktur wird verwendet, um zu überprüfen, wann ein asynchroner Datenträger Lesevorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="68b35-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="68b35-115">Geben Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion auf der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) an, die das streamingaudiomaterial wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="68b35-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="68b35-116">Schleife, während die aktuelle Lese Position nicht das Ende der Audiodatei überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="68b35-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="68b35-117">Führen Sie in der-Schleife die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="68b35-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="68b35-118">Liest einen Datenblock vom Datenträger in den aktuellen Lese Puffer.</span><span class="sxs-lookup"><span data-stu-id="68b35-118">Read a chunk of data from the disk into the current read buffer.</span></span>

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  <span data-ttu-id="68b35-119">Verwenden Sie die **ge-verlappedresult** -Funktion, um auf das Ereignis zu warten, das signalisiert, dass der Lesevorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="68b35-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="68b35-120">Warten Sie, bis die Anzahl der in der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) befindlichen Puffer kleiner als die Anzahl der gelesenen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="68b35-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="68b35-121">Der Zustand der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) wird mit der [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) -Funktion geprüft.</span><span class="sxs-lookup"><span data-stu-id="68b35-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="68b35-122">Übermitteln Sie den aktuellen Lese Puffer mithilfe der [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) -Funktion an die [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="68b35-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  <span data-ttu-id="68b35-123">Legen Sie den aktuellen lesepufferindex auf den nächsten Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="68b35-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="68b35-124">Nachdem die Schleife abgeschlossen ist, warten Sie, bis die verbleibenden Puffer in der Warteschlange beendet sind.</span><span class="sxs-lookup"><span data-stu-id="68b35-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="68b35-125">Wenn die restlichen Puffer wieder abgespielt wurden, wird der Sound angehalten, und der Thread kann beendet oder wieder verwendet werden, um einen anderen Sound zu streamen.</span><span class="sxs-lookup"><span data-stu-id="68b35-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="68b35-126">Erstellen der Rückruf Klasse</span><span class="sxs-lookup"><span data-stu-id="68b35-126">Creating the callback class</span></span>

<span data-ttu-id="68b35-127">Um die Rückruf Klasse zu erstellen, erstellen Sie eine Klasse, die von der [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="68b35-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="68b35-128">Die Klasse sollte ein Ereignis in der [**onbufferend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="68b35-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="68b35-129">Dadurch kann sich der Streaminginhalt in den Standbymodus versetzen, bis das Ereignis signalisiert, dass XAudio2 das Lesen aus einem Audiopuffer beendet hat.</span><span class="sxs-lookup"><span data-stu-id="68b35-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="68b35-130">Weitere Informationen zur Verwendung von Rückrufen mit XAudio2 finden Sie unter Gewusst [wie: Verwenden von Quellcode-Rückrufe](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="68b35-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a><span data-ttu-id="68b35-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68b35-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b35-132">Streaming von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="68b35-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="68b35-133">XAudio2-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="68b35-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="68b35-134">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="68b35-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="68b35-135">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="68b35-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="68b35-136">So wird's gemacht: Verwenden der Rückrufe für Quellstimmen</span><span class="sxs-lookup"><span data-stu-id="68b35-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 

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
# <a name="how-to-stream-a-sound-from-disk"></a>So wird's gemacht: Streamen von Sound von einem Datenträger

> [!Note]  
> Dieser Inhalt gilt nur für Desktop-Apps und erfordert Revision, damit Sie in einer Windows Store-App funktionieren. Weitere Informationen finden Sie in der Dokumentation zu **CreateFile2**, " [forateeventex](/windows/win32/api/synchapi/nf-synchapi-createeventexa)", " [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)", " [setfilepointerex](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)" und " **getoverlappedresultex**". Weitere Informationen finden Sie im Beispiel zu streameffect Windows 8 aus der [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).

 

Sie können Audiodaten in XAudio2 streamen, indem Sie einen separaten Thread erstellen und Puffer Lesevorgänge für die Audiodaten im streamingthread durchführen. verwenden Sie dann Rückrufe, um diesen Thread zu steuern.

-   [Ausführen von Puffer Lesevorgängen im streamingindthread](#performing-buffer-reads-in-the-streaming-thread)
-   [Erstellen der Rückruf Klasse](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Ausführen von Puffer Lesevorgängen im streamingindthread

Führen Sie die folgenden Schritte aus, um die Puffer Lesevorgänge im streamingthread auszuführen:

1.  Erstellen Sie ein Array von Lese Puffern.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Initialisieren Sie eine überlappende Struktur.

    Die-Struktur wird verwendet, um zu überprüfen, wann ein asynchroner Datenträger Lesevorgang abgeschlossen wurde.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Geben Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion auf der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) an, die das streamingaudiomaterial wieder gibt.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Schleife, während die aktuelle Lese Position nicht das Ende der Audiodatei überschritten wird.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    Führen Sie in der-Schleife die folgenden Schritte aus:

    1.  Liest einen Datenblock vom Datenträger in den aktuellen Lese Puffer.

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

        

    2.  Verwenden Sie die **ge-verlappedresult** -Funktion, um auf das Ereignis zu warten, das signalisiert, dass der Lesevorgang abgeschlossen wurde.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Warten Sie, bis die Anzahl der in der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) befindlichen Puffer kleiner als die Anzahl der gelesenen Puffer ist.

        Der Zustand der [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) wird mit der [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) -Funktion geprüft.

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Übermitteln Sie den aktuellen Lese Puffer mithilfe der [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) -Funktion an die [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) .

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

        

    5.  Legen Sie den aktuellen lesepufferindex auf den nächsten Puffer fest.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Nachdem die Schleife abgeschlossen ist, warten Sie, bis die verbleibenden Puffer in der Warteschlange beendet sind.

    Wenn die restlichen Puffer wieder abgespielt wurden, wird der Sound angehalten, und der Thread kann beendet oder wieder verwendet werden, um einen anderen Sound zu streamen.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Erstellen der Rückruf Klasse

Um die Rückruf Klasse zu erstellen, erstellen Sie eine Klasse, die von der [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle erbt.

Die Klasse sollte ein Ereignis in der [**onbufferend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) -Methode festlegen. Dadurch kann sich der Streaminginhalt in den Standbymodus versetzen, bis das Ereignis signalisiert, dass XAudio2 das Lesen aus einem Audiopuffer beendet hat. Weitere Informationen zur Verwendung von Rückrufen mit XAudio2 finden Sie unter Gewusst [wie: Verwenden von Quellcode-Rückrufe](how-to--use-source-voice-callbacks.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streaming von Audiodaten](streaming-audio-data.md)
</dt> <dt>

[XAudio2-Rückrufe](callbacks.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Verwenden der Rückrufe für Quellstimmen](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 

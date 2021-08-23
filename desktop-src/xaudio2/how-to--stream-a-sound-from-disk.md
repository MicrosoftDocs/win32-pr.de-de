---
description: Sie können Audiodaten in XAudio2 streamen, indem Sie einen separaten Thread erstellen und Pufferlesedaten der Audiodaten im Streamingthread ausführen und dann Rückrufe verwenden, um diesen Thread zu steuern.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: "So wird's gemacht: Streamen von Sound von einem Datenträger"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ee06866427a8efcdd3e132740d595ec547f55a592182ebfbdced0feefca793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707100"
---
# <a name="how-to-stream-a-sound-from-disk"></a>So wird's gemacht: Streamen von Sound von einem Datenträger

> [!Note]  
> Dieser Inhalt gilt nur für Desktop-Apps und erfordert eine Revision, um in einer Windows Store-App zu funktionieren. Weitere Informationen finden Sie in der Dokumentation zu **CreateFile2,** [CreateEventEx,](/windows/win32/api/synchapi/nf-synchapi-createeventexa) [WaitForSingleObjectEx,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)und **GetOverlappedResultEx.** Weitere Informationen finden Sie im StreamEffect Windows 8-Beispiel aus dem [Windows SDK-Beispielkatalog.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208))

 

Sie können Audiodaten in XAudio2 streamen, indem Sie einen separaten Thread erstellen und Pufferlesedaten der Audiodaten im Streamingthread ausführen und dann Rückrufe verwenden, um diesen Thread zu steuern.

-   [Ausführen von Pufferleseläufen im Streamingthread](#performing-buffer-reads-in-the-streaming-thread)
-   [Erstellen der Rückrufklasse](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Ausführen von Pufferleseläufen im Streamingthread

Führen Sie die folgenden Schritte aus, um Pufferleseläufe im Streamingthread auszuführen:

1.  Erstellen Sie ein Array von Lesepuffern.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Initialisieren sie eine OVERLAPPED-Struktur.

    Die -Struktur wird verwendet, um zu überprüfen, wann ein asynchroner Datenträgerleselauf abgeschlossen ist.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Rufen Sie die [**Start-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) für die [**Quellstimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) auf, die das Streamingaudio wiedergeben wird.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Schleife, während die aktuelle Leseposition nicht an das Ende der Audiodatei übergeben wird.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    Gehen Sie in der -Schleife wie folgt vor:

    1.  Liest einen Datenabschnitt vom Datenträger in den aktuellen Lesepuffer.

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

        

    2.  Verwenden Sie die **GetOverlappedResult-Funktion,** um auf das Ereignis zu warten, das signalisiert, dass der Leselauf abgeschlossen ist.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Warten Sie, bis die Anzahl der Puffer, die in der [**Quellstimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) in die Warteschlange eingereiht werden, kleiner als die Anzahl der Lesepuffer ist.

        Der Zustand der [**Quellstimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) wird mit der [**GetState-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) überprüft.

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Übermitteln Sie den aktuellen Lesepuffer mithilfe der [**SubmitSourceBuffer-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) an die [**Quellstimme.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

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

        

    5.  Legen Sie den aktuellen Index des Lesepuffers auf den nächsten Puffer fest.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Warten Sie nach Abschluss der Schleife, bis die verbleibenden Puffer in der Warteschlange die Wiedergabe abgeschlossen haben.

    Wenn die wiedergabe der verbleibenden Puffer abgeschlossen ist, wird der Sound beendet, und der Thread kann beendet oder wiederverwendet werden, um einen anderen Sound zu streamen.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Erstellen der Rückrufklasse

Erstellen Sie zum Erstellen der Rückrufklasse eine Klasse, die von der [**IXAudio2VoiceCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) erbt.

Die -Klasse sollte ein Ereignis in ihrer [**OnBufferEnd-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) festlegen. Dadurch kann sich der Streamingthread in den Ruhezustand versetzen, bis das Ereignis signalisiert, dass XAudio2 das Lesen aus einem Audiopuffer abgeschlossen hat. Weitere Informationen zur Verwendung von Rückrufen mit XAudio2 finden Sie unter [Vorgehensweise: Verwenden von Quellstimmenrückrufen.](how-to--use-source-voice-callbacks.md)


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

 

 

---
description: In diesem Thema werden die Schritte zum Auffüllen der Strukturen beschrieben, die zum Wiedergeben von Audiodaten in XAudio2 erforderlich sind.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: "So wird's gemacht: Laden von Datendateien in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bacf08e8f16e5cd9c42409776b02846990b9d66d685a0186314445742f23341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962659"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>So wird's gemacht: Laden von Datendateien in XAudio2

> [!Note]  
> Dieser Inhalt gilt nur für Desktop-Apps und erfordert eine Revision, um in einer Windows Store-App zu funktionieren. Weitere Informationen finden Sie in der Dokumentation zu [**CreateFile2,**](/windows/win32/api/fileapi/nf-fileapi-createfile2) [**CreateEventEx,**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) [**WaitForSingleObjectEx,**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)und [**GetOverlappedResultEx.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex) Weitere Informationen finden Sie unter SoundFileReader.h/.cpp im BasicSound Windows 8-Beispiel aus dem [Windows SDK-Beispielkatalog.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208))

 

In diesem Thema werden die Schritte zum Auffüllen der Strukturen beschrieben, die zum Wiedergeben von Audiodaten in XAudio2 erforderlich sind. Die folgenden Schritte laden die Blöcke "fmt" und "data" einer Audiodatei und verwenden sie, um eine **WAVEFORMATEXTENSIBLE-Struktur** und eine [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) aufzufüllen.

-   [Vorbereiten der Analyse der Audiodatei.](#preparing-to-parse-the-audio-file)
-   [Auffüllen von XAudio2-Strukturen mit dem Inhalt von CSV-Blöcken.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Vorbereiten der Analyse der Audiodatei

Audiodateien, die von XAudio2 unterstützt werden, verwenden das Resource Interchange File Format (DOSSIER). DER ABSCHNITT WIRD in der Übersicht über das [Resource Interchange File Format (CSV)](resource-interchange-file-format--riff-.md) beschrieben. Die Audiodaten in einer CSV-Datei werden geladen, indem der ABSCHNITT GESUCHT und dann durch den Block schleifet wird, um einzelne Blöcke zu finden, die im SEGMENT enthalten sind. Die folgenden Funktionen sind Beispiele für Code zum Suchen von Segmenten und Laden von Daten, die in den Blöcken enthalten sind.

-   So suchen Sie einen Block in einer PROTOKOLLDATEI:

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   So lesen Sie Daten in einem Block, nachdem sie gefunden wurden.

    Sobald ein gewünschter Block gefunden wurde, können seine Daten gelesen werden, indem der Dateizeiger an den Anfang des Datenabschnitts des Blockes angepasst wird. Eine Funktion zum Lesen der Daten aus einem Block, sobald sie gefunden wurde, könnte wie folgt aussehen.

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Auffüllen von XAudio2-Strukturen mit dem Inhalt von VERSA-Blöcken

Damit XAudio2 Audio mit einer Quellstimme wiedergeben kann, benötigen sie eine **WAVEFORMATEX-Struktur** und eine [**XAUDIO2 \_ BUFFER-Struktur.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Die **WAVEFORMATEX-Struktur** kann eine größere Struktur wie **WAVEFORMATEXTENSIBLE** sein, die eine **WAVEFORMATEX-Struktur** als erstes Element enthält. Weitere Informationen finden Sie auf der **WAVEFORMATEX-Referenzseite.**

In diesem Beispiel wird **WAVEFORMATEXTENSIBLE** verwendet, um das Laden von PCM-Audiodateien mit mehr als zwei Kanälen zu ermöglichen.

Die folgenden Schritte veranschaulichen die Verwendung der oben beschriebenen Funktionen, um eine **WAVEFORMATEXTENSIBLE-Struktur** und eine [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) aufzufüllen. In diesem Fall enthält die zu ladende Audiodatei PCM-Daten und nur die Blöcke 'CSV', 'fmt ' und 'data'. Andere Formate können zusätzliche Blocktypen enthalten, wie in [RESOURCE Interchange File Format (CSV)](resource-interchange-file-format--riff-.md)beschrieben.

1.  Deklarieren Sie **WAVEFORMATEXTENSIBLE-** und [**XAUDIO2 \_ BUFFER-Strukturen.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Öffnen Sie die Audiodatei mit CreateFile.
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  Suchen Sie in der Audiodatei nach dem Block "CSV", und überprüfen Sie den Dateityp.
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  Suchen Sie den Block "fmt", und kopieren Sie dessen Inhalt in eine **WAVEFORMATEXTENSIBLE-Struktur.**
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Suchen Sie den Datenabschnitt, und lesen Sie dessen Inhalt in einen Puffer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Füllen Sie eine [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) auf.
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[So wird's gemacht: Wiedergeben von Ton mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 

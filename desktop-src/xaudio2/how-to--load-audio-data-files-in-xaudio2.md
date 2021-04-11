---
description: In diesem Thema werden die Schritte zum Auffüllen der Strukturen beschrieben, die für die Wiedergabe von Audiodaten in XAudio2 erforderlich sind.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: "So wird's gemacht: Laden von Datendateien in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129765"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>So wird's gemacht: Laden von Datendateien in XAudio2

> [!Note]  
> Dieser Inhalt gilt nur für Desktop-Apps und erfordert Revision, damit Sie in einer Windows Store-App funktionieren. Weitere Informationen finden Sie in der Dokumentation zu [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), " [**forateeventex**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)", " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)", " [**setfilepointerex**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)" und " [**getoverlappedresultex**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex)". Weitere Informationen finden Sie unter "Soundfilter eader. h/. cpp" im Beispiel "basicsound Windows 8" aus der [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

In diesem Thema werden die Schritte zum Auffüllen der Strukturen beschrieben, die für die Wiedergabe von Audiodaten in XAudio2 erforderlich sind. Mit den folgenden Schritten werden die "fmt"-und "Data"-Blöcke einer Audiodatei geladen und verwendet, um eine **WAVEFORMATEXTENSIBLE** -Struktur und eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen.

-   [Das Analysieren der Audiodatei wird vorbereitet.](#preparing-to-parse-the-audio-file)
-   [Auffüllen von XAudio2-Strukturen mit dem Inhalt von Riff-Blöcken.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Das Analysieren der Audiodatei wird vorbereitet.

Audiodateien, die von XAudio2 unterstützt werden, verwenden das Ressourcenaustausch Datei Format (Riff). Das Riff wird in der Übersicht über das [Ressourcenaustausch Datei Format (Riff)](resource-interchange-file-format--riff-.md) beschrieben. Audiodaten in einer Riff Datei werden geladen, indem der Riff Block gefunden und dann durch den Block durchlaufen wird, um einzelne Segmente im Riff Block zu suchen. Die folgenden Funktionen sind Beispiele für Code zum Suchen von Blöcken und Laden von Daten, die in den Blöcken enthalten sind.

-   So finden Sie einen Block in einer Riff Datei:

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

    

-   , Wenn Daten in einem Block gelesen werden sollen, nachdem Sie gefunden wurden.

    Sobald ein gewünschter Block gefunden wird, können seine Daten gelesen werden, indem der Dateizeiger auf den Anfang des Daten Abschnitts des Segments angepasst wird. Eine Funktion zum Lesen der Daten aus einem Block, sobald Sie gefunden wird, könnte wie folgt aussehen.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Auffüllen von XAudio2-Strukturen mit dem Inhalt von Riff Blöcken

Damit XAudio2 Audiodaten mit einer Quell Stimme abspielen kann, benötigt es eine **WaveFormatEx** -Struktur und eine [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur. Die **WaveFormatEx** -Struktur kann eine größere Struktur sein, z. b. **WAVEFORMATEXTENSIBLE** , die eine **WaveFormatEx** -Struktur als ersten Member enthält. Weitere Informationen finden Sie auf der Referenzseite zu **WaveFormatEx** .

In diesem Beispiel wird eine **WAVEFORMATEXTENSIBLE** verwendet, um das Laden von PCM-Audiodateien mit mehr als zwei Kanälen zuzulassen.

Die folgenden Schritte veranschaulichen die Verwendung der oben beschriebenen Funktionen, um eine **WAVEFORMATEXTENSIBLE** -Struktur und eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen. In diesem Fall enthält die Audiodatei, die geladen wird, PCM-Daten und enthält nur den Block "Riff", "fmt" und "Data". Andere Formate enthalten möglicherweise zusätzliche Segmenttypen, wie im Text [Format der Ressourcenaustausch Datei (Riff)](resource-interchange-file-format--riff-.md)beschrieben.

1.  Deklarieren Sie **WAVEFORMATEXTENSIBLE** -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Strukturen.
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Öffnen Sie die Audiodatei mit "deatefile".
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

    

3.  Suchen Sie den Block "Riff" in der Audiodatei, und überprüfen Sie den Dateityp.
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

    

4.  Suchen Sie den Block "f", und kopieren Sie seinen Inhalt in eine **WAVEFORMATEXTENSIBLE** -Struktur.
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Suchen Sie den Block "Data", und lesen Sie seinen Inhalt in einem Puffer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Füllt eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur auf.
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

 

 

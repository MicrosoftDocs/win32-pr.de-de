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
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="d3949-103">So wird's gemacht: Laden von Datendateien in XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3949-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="d3949-104">Dieser Inhalt gilt nur für Desktop-Apps und erfordert Revision, damit Sie in einer Windows Store-App funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d3949-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="d3949-105">Weitere Informationen finden Sie in der Dokumentation zu [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), " [**forateeventex**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)", " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)", " [**setfilepointerex**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)" und " [**getoverlappedresultex**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex)".</span><span class="sxs-lookup"><span data-stu-id="d3949-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="d3949-106">Weitere Informationen finden Sie unter "Soundfilter eader. h/. cpp" im Beispiel "basicsound Windows 8" aus der [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="d3949-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="d3949-107">In diesem Thema werden die Schritte zum Auffüllen der Strukturen beschrieben, die für die Wiedergabe von Audiodaten in XAudio2 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d3949-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="d3949-108">Mit den folgenden Schritten werden die "fmt"-und "Data"-Blöcke einer Audiodatei geladen und verwendet, um eine **WAVEFORMATEXTENSIBLE** -Struktur und eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="d3949-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="d3949-109">Das Analysieren der Audiodatei wird vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d3949-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="d3949-110">Auffüllen von XAudio2-Strukturen mit dem Inhalt von Riff-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="d3949-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="d3949-111">Das Analysieren der Audiodatei wird vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d3949-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="d3949-112">Audiodateien, die von XAudio2 unterstützt werden, verwenden das Ressourcenaustausch Datei Format (Riff).</span><span class="sxs-lookup"><span data-stu-id="d3949-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="d3949-113">Das Riff wird in der Übersicht über das [Ressourcenaustausch Datei Format (Riff)](resource-interchange-file-format--riff-.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3949-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="d3949-114">Audiodaten in einer Riff Datei werden geladen, indem der Riff Block gefunden und dann durch den Block durchlaufen wird, um einzelne Segmente im Riff Block zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d3949-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="d3949-115">Die folgenden Funktionen sind Beispiele für Code zum Suchen von Blöcken und Laden von Daten, die in den Blöcken enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d3949-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="d3949-116">So finden Sie einen Block in einer Riff Datei:</span><span class="sxs-lookup"><span data-stu-id="d3949-116">To find a chunk in a RIFF file:</span></span>

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

    

-   <span data-ttu-id="d3949-117">, Wenn Daten in einem Block gelesen werden sollen, nachdem Sie gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="d3949-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="d3949-118">Sobald ein gewünschter Block gefunden wird, können seine Daten gelesen werden, indem der Dateizeiger auf den Anfang des Daten Abschnitts des Segments angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="d3949-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="d3949-119">Eine Funktion zum Lesen der Daten aus einem Block, sobald Sie gefunden wird, könnte wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="d3949-119">A function to read the data from a chunk once it is found might look like this.</span></span>

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="d3949-120">Auffüllen von XAudio2-Strukturen mit dem Inhalt von Riff Blöcken</span><span class="sxs-lookup"><span data-stu-id="d3949-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="d3949-121">Damit XAudio2 Audiodaten mit einer Quell Stimme abspielen kann, benötigt es eine **WaveFormatEx** -Struktur und eine [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d3949-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="d3949-122">Die **WaveFormatEx** -Struktur kann eine größere Struktur sein, z. b. **WAVEFORMATEXTENSIBLE** , die eine **WaveFormatEx** -Struktur als ersten Member enthält.</span><span class="sxs-lookup"><span data-stu-id="d3949-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="d3949-123">Weitere Informationen finden Sie auf der Referenzseite zu **WaveFormatEx** .</span><span class="sxs-lookup"><span data-stu-id="d3949-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="d3949-124">In diesem Beispiel wird eine **WAVEFORMATEXTENSIBLE** verwendet, um das Laden von PCM-Audiodateien mit mehr als zwei Kanälen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d3949-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="d3949-125">Die folgenden Schritte veranschaulichen die Verwendung der oben beschriebenen Funktionen, um eine **WAVEFORMATEXTENSIBLE** -Struktur und eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="d3949-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="d3949-126">In diesem Fall enthält die Audiodatei, die geladen wird, PCM-Daten und enthält nur den Block "Riff", "fmt" und "Data".</span><span class="sxs-lookup"><span data-stu-id="d3949-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="d3949-127">Andere Formate enthalten möglicherweise zusätzliche Segmenttypen, wie im Text [Format der Ressourcenaustausch Datei (Riff)](resource-interchange-file-format--riff-.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3949-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="d3949-128">Deklarieren Sie **WAVEFORMATEXTENSIBLE** -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="d3949-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="d3949-129">Öffnen Sie die Audiodatei mit "deatefile".</span><span class="sxs-lookup"><span data-stu-id="d3949-129">Open the audio file with CreateFile.</span></span>
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

    

3.  <span data-ttu-id="d3949-130">Suchen Sie den Block "Riff" in der Audiodatei, und überprüfen Sie den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="d3949-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
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

    

4.  <span data-ttu-id="d3949-131">Suchen Sie den Block "f", und kopieren Sie seinen Inhalt in eine **WAVEFORMATEXTENSIBLE** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d3949-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="d3949-132">Suchen Sie den Block "Data", und lesen Sie seinen Inhalt in einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="d3949-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="d3949-133">Füllt eine [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="d3949-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="d3949-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3949-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3949-135">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d3949-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="d3949-136">So wird's gemacht: Wiedergeben von Ton mit XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3949-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="d3949-137">XAudio2-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="d3949-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 

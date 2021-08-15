---
description: In diesem Tutorial erfahren Sie, wie Sie den Quellleser verwenden, um Audiodaten aus einer Mediendatei zu decodieren und in eine WAVE-Datei zu schreiben.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Tutorial: Decodieren von Audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ad5dbac47680c4d8faa73affa711b987edf220e05324d88cd0ffbda3bb93e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237664"
---
# <a name="tutorial-decoding-audio"></a>Tutorial: Decodieren von Audio

In diesem Tutorial erfahren Sie, wie Sie den [Quellleser](source-reader.md) verwenden, um Audiodaten aus einer Mediendatei zu decodieren und in eine WAVE-Datei zu schreiben. Das Tutorial basiert auf dem [Audio clip-Beispiel.](audio-clip-sample.md)

-   [Übersicht](#overview)
-   [Header- und Bibliotheksdateien](#header-and-library-files)
-   [Implementieren von wmain](#implement-wmain)
-   [Schreiben der WAVE-Datei](#write-the-wave-file)
-   [Konfigurieren des Quelllesers](#configure-the-source-reader)
-   [Schreiben des WAVE-Dateiheaders](#write-the-wave-file-header)
-   [Berechnen der maximalen Datengröße](#calculate-the-maximum-data-size)
-   [Decodieren der Audiodaten](#decode-the-audio)
-   [Finalisieren des Dateiheaders](#finalize-the-file-header)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

In diesem Tutorial erstellen Sie eine Konsolenanwendung, die zwei Befehlszeilenargumente verwendet: den Namen einer Eingabedatei, die einen Audiostream enthält, und den Namen der Ausgabedatei. Die Anwendung liest fünf Sekunden Audiodaten aus der Eingabedatei und schreibt die Audiodaten als WAVE-Daten in die Ausgabedatei.

Um die decodierten Audiodaten zu erhalten, verwendet die Anwendung das Quellleseobjekt. Der Quellleser macht die [**BENUTZEROBERFLÄCHESourceReader-Schnittstelle**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) verfügbar. Um die decodierte Audiodatei in die WAVE-Datei zu schreiben, verwenden die Anwendungen Windows E/A-Funktionen. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das zeigt, wie der Quellleser Audiodaten aus der Quelldatei bekommt.](images/audio-clip-tutorial.gif)

In der einfachsten Form hat eine WAVE-Datei die folgende Struktur:



| Datentyp                              | Größe (Byte) | Wert                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | 'BENT'                                                                |
| **DWORD**                              | 4            | Gesamtdateigröße, ohne die ersten 8 Bytes                      |
| **FOURCC**                             | 4            | "WAVE"                                                                |
| **FOURCC**                             | 4            | 'fmt'                                                                |
| **DWORD**                              | 4            | Größe der [**folgenden WAVEFORMATEX-Daten.**](/previous-versions/dd757713(v=vs.85)) |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | Varies       | Audioformatheader.                                                  |
| **FOURCC**                             | 4            | "data"                                                                |
| **DWORD**                              | 4            | Größe der Audiodaten.                                               |
| **Byte**\[\]                           | Varies       | Audiodaten.                                                           |



 

> [!Note]  
> Ein **FOURCC ist** ein **DWORD,** das durch Verkettung von vier ASCII-Zeichen gebildet wird.

 

Diese grundlegende Struktur kann erweitert werden, indem Dateimetadaten und andere Informationen hinzugefügt werden, die den Rahmen dieses Tutorials nicht erweitern.

## <a name="header-and-library-files"></a>Header- und Bibliotheksdateien

Schließen Sie die folgenden Headerdateien in Ihr Projekt ein:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Link zu den folgenden Bibliotheken:

-   mfplat.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="implement-wmain"></a>Implementieren von wmain

Der folgende Code zeigt die Einstiegspunktfunktion für die Anwendung.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



Diese Funktion führt Folgendes aus:

1.  Ruft [**CoInitializeEx auf,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) um die COM-Bibliothek zu initialisieren.
2.  Ruft [**MFStartup auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) um die Media Foundation zu initialisieren.
3.  Ruft [**MFCreateSourceReaderFromURL auf,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) um den Quellreader zu erstellen. Diese Funktion nimmt den Namen der Eingabedatei an und empfängt einen [**BESSOURCEReader-Schnittstellenzeiger.**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
4.  Erstellt die Ausgabedatei durch Aufrufen der **CreateFile-Funktion,** die ein Dateihand handle zurückgibt.
5.  Ruft die anwendungsdefinierte [WriteWavFile-Funktion](#write-the-wave-file) auf. Diese Funktion decodiert die Audiodaten und schreibt die WAVE-Datei.
6.  Gibt den POINTer UND das Dateihandles für [**DIE SOURCESourceReader-Datei**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) frei.
7.  Ruft [**MFShutdown auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) um die Media Foundation herunterfahren.
8.  Ruft [**CoUninitialize auf,**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) um die COM-Bibliothek frei zu geben.

## <a name="write-the-wave-file"></a>Schreiben der WAVE-Datei

Der Größte Teil der Arbeit erfolgt in der `WriteWavFile` -Funktion, die von aufgerufen `wmain` wird.


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



Diese Funktion ruft eine Reihe anderer anwendungsdefinierter Funktionen auf:

1.  Die [ConfigureAudioStream-Funktion](#configure-the-source-reader) initialisiert den Quellreader. Diese Funktion empfängt einen Zeiger auf die [**INTERFACESMediaType-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) die verwendet wird, um eine Beschreibung des decodierten Audioformats zu erhalten, einschließlich Abtastrate, Anzahl von Kanälen und Bittiefe (Bits pro Stichprobe).
2.  Die WriteWaveHeader-Funktion schreibt den ersten Teil der WAVE-Datei, einschließlich des Headers und des Beginns des Datenbereichs.
3.  Die CalculateMaxAudioDataSize-Funktion berechnet die maximale Audiomenge in Byte, die in die Datei geschrieben werden soll.
4.  Die WriteWaveData-Funktion schreibt die PCM-Audiodaten in die Datei.
5.  Die FixUpChunkSizes-Funktion schreibt die Dateigrößeninformationen, die nach den **FOURCC-Werten** "FIX" und "data" in der WAVE-Datei angezeigt werden. (Diese Werte sind erst bekannt, wenn `WriteWaveData` sie abgeschlossen sind.)

Diese Funktionen werden in den verbleibenden Abschnitten dieses Tutorials gezeigt.

## <a name="configure-the-source-reader"></a>Konfigurieren des Quelllesers

Die `ConfigureAudioStream` -Funktion konfiguriert den Quellreader zum Decodieren des Audiostreams in der Quelldatei. Außerdem werden Informationen zum Format des decodierten Audios zurückgegeben.

In Media Foundation werden Medienformate mithilfe von *Medientypobjekten* beschrieben. Ein Medientypobjekt macht die [**BESCHRIFTUNGMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) verfügbar, die die [**BESCHRIFTUNGAttributes-Schnittstelle erbt.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Im Wesentlichen ist ein Medientyp eine Auflistung von Eigenschaften, die das Format beschreiben. Weitere Informationen finden Sie unter [Medientypen.](media-types.md)


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



Die `ConfigureAudioStream` Funktion führt Folgendes aus:

1.  Ruft die [**METHODE VERERBSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) auf, um den Audiodatenstrom auszuwählen und die Auswahl aller anderen Streams aufzuheben. Dieser Schritt kann die Leistung verbessern, da er verhindert, dass der Quellleser Videoframes beibehaltung, die von der Anwendung nicht verwendet werden.
2.  Erstellt einen *partiellen* Medientyp, der PCM-Audio angibt. Die Funktion erstellt den partiellen Typ wie folgt:
    1.  Ruft [**MFCreateMediaType auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) um ein leeres Medientypobjekt zu erstellen.
    2.  Legt das [**MF \_ MT MAJOR \_ \_ TYPE-Attribut**](mf-mt-major-type-attribute.md) auf **MFMediaType \_ Audio fest.**
    3.  Legt das [**MF \_ MT \_ SUBTYPE-Attribut**](mf-mt-subtype-attribute.md) auf **MFAudioFormat \_ PCM fest.**
3.  Ruft [**DEN WERTSOURCEReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) auf, um den partiellen Typ für den Quellreader fest zu legen. Wenn die Quelldatei codierte Audiodaten enthält, lädt der Quellleser automatisch den erforderlichen Audiodecoder.
4.  Ruft [**DEN COMPUTERSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) auf, um den tatsächlichen PCM-Medientyp zu erhalten. Diese Methode gibt einen Medientyp mit allen ausgefüllten Formatdetails zurück, z. B. die Audio-Abtastrate und die Anzahl der Kanäle.
5.  Ruft [**ZUM Aktivieren des Audiodatenstroms DIE SOURCEReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) auf.

## <a name="write-the-wave-file-header"></a>Schreiben des WAVE-Dateiheaders

Die `WriteWaveHeader` Funktion schreibt den WAVE-Dateiheader.

Die einzige Media Foundation API, die von dieser Funktion aufgerufen wird, ist [**MFCreateWaveFormatExFromMFMediaType,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)die den Medientyp in eine [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) konvertiert.


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



Die -Funktion ist eine einfache Hilfsfunktion, die die Windows WriteFile-Funktion umschließt `WriteToFile` und einen **HRESULT-Wert** zurückgibt. 


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a>Berechnen der maximalen Datengröße

Da die Dateigröße als 4-Byte-Wert im Dateiheader gespeichert wird, ist eine WAVE-Datei auf eine maximale Größe von 0xFFFFFFFF Bytes beschränkt – ungefähr 4 GB. Dieser Wert enthält die Größe des Dateiheaders. PCM-Audio hat eine konstante Bitrate, sodass Sie die maximale Datengröße aus dem Audioformat wie folgt berechnen können:


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



Um partielle Audioframes zu vermeiden, wird die Größe auf die Blockausrichtung gerundet, die im [**MF \_ MT AUDIO BLOCK \_ \_ \_ ALIGNMENT-Attribut gespeichert**](mf-mt-audio-block-alignment-attribute.md) ist.

## <a name="decode-the-audio"></a>Decodieren der Audiodaten

Die `WriteWaveData` Funktion liest decodierte Audiodaten aus der Quelldatei und schreibt in die WAVE-Datei.


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



Die `WriteWaveData` Funktion führt in einer Schleife Folgendes aus:

1.  Ruft [**DEN Reader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) auf, um Audiodaten aus der Quelldatei zu lesen. Der *dwFlags-Parameter* empfängt ein bitweises **OR** von Flags von der [**MF SOURCE \_ READER \_ \_ FLAG-Enumeration.**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) Der *pSample-Parameter* empfängt einen Zeiger auf die [**NSSAMPLE-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) die für den Zugriff auf die Audiodaten verwendet wird. In einigen Fällen werden durch einen Aufruf **von ReadSample** keine Daten generiert. In diesem Fall ist der **DURCHZEIGSample-Zeiger** **NULL.**
2.  Überprüft *dwFlags* auf die folgenden Flags:
    -   **MF \_ SOURCE \_ READERF \_ CURRENTMEDIATYPECHANGED**. Dieses Flag gibt eine Formatänderung in der Quelldatei an. WAVE-Dateien unterstützen keine Formatänderungen.
    -   **MF \_ SOURCE \_ READERF \_ ENDOFSTREAM**. Dieses Flag gibt das Ende des Streams an.
3.  Ruft [**DIEBsample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) auf, um einen Zeiger auf ein Pufferobjekt zu erhalten.
4.  Ruft [**EINEMEDIABuffer::Lock auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) um einen Zeiger auf den Pufferspeicher zu erhalten.
5.  Schreibt die Audiodaten in die Ausgabedatei.
6.  Ruft [**DIEBMEDIABuffer::Unlock auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) um das Pufferobjekt zu entsperren.

Die Funktion bricht die Schleife aus, wenn eine der folgenden Bedingungen auftritt:

-   Das Streamformat ändert sich.
-   Das Ende des Streams ist erreicht.
-   Die maximale Menge an Audiodaten wird in die Ausgabedatei geschrieben.
-   Ein Fehler tritt auf.

## <a name="finalize-the-file-header"></a>Finalisieren des Dateiheaders

Die im WAVE-Header gespeicherten Größenwerte sind erst bekannt, wenn die vorherige Funktion abgeschlossen ist. Die `FixUpChunkSizes` füllt die folgenden Werte aus:


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> <dt>

[**VERERBUNGQuelleLeser**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 

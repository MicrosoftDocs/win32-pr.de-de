---
description: In diesem Tutorial wird gezeigt, wie Sie den Quell Leser zum Decodieren von Audiodaten aus einer Mediendatei und zum Schreiben der Audiodatei in eine Wave-Datei verwenden.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Tutorial: Decodieren von Audiodaten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565783"
---
# <a name="tutorial-decoding-audio"></a>Tutorial: Decodieren von Audiodaten

In diesem Tutorial wird gezeigt, wie Sie den [Quell Leser](source-reader.md) zum Decodieren von Audiodaten aus einer Mediendatei und zum Schreiben der Audiodatei in eine Wave-Datei verwenden. Das Tutorial basiert auf dem Beispiel [Audioclip](audio-clip-sample.md) .

-   [Übersicht](#overview)
-   [Header-und Bibliotheksdateien](#header-and-library-files)
-   [Implementieren von wmain](#implement-wmain)
-   [Schreiben der Wave-Datei](#write-the-wave-file)
-   [Konfigurieren des Quell Readers](#configure-the-source-reader)
-   [Schreiben des Wave-Datei Headers](#write-the-wave-file-header)
-   [Berechnen der maximalen Datengröße](#calculate-the-maximum-data-size)
-   [Decodieren der Audiodatei](#decode-the-audio)
-   [Beenden Sie den Datei Header.](#finalize-the-file-header)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

In diesem Tutorial erstellen Sie eine Konsolenanwendung, die zwei Befehlszeilenargumente annimmt: den Namen einer Eingabedatei, die einen Audiodatenstrom enthält, und den Namen der Ausgabedatei. Die Anwendung liest fünf Sekunden Audiodaten aus der Eingabedatei und schreibt die Audiodaten als wellendaten in die Ausgabedatei.

Die Anwendung verwendet das Quell Lese Objekt, um die decodierten Audiodaten zu erhalten. Der Quell Leser macht die [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Schnittstelle verfügbar. Die Anwendungen verwenden Windows-e/a-Funktionen, um die decodierte Audiodatei in die Wave-Datei zu schreiben. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![das Diagramm zeigt den Quell Leser, der Audiodaten aus der Quelldatei erhält.](images/audio-clip-tutorial.gif)

In seiner einfachsten Form hat eine Wave-Datei die folgende Struktur:



| Datentyp                              | Größe (Byte) | Wert                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FourCC**                             | 4            | FF                                                                |
| **DWORD**                              | 4            | Gesamt Dateigröße ohne die ersten 8 Bytes                      |
| **FourCC**                             | 4            | Welle                                                                |
| **FourCC**                             | 4            | fmt                                                                |
| **DWORD**                              | 4            | Größe der folgenden [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Daten. |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | Varies       | Audioformatierungs Header.                                                  |
| **FourCC**                             | 4            | Vorrats                                                                |
| **DWORD**                              | 4            | Größe der Audiodaten.                                               |
| **Hobby**\[\]                           | Varies       | Audiodaten.                                                           |



 

> [!Note]  
> Ein **FourCC** ist ein **DWORD** , das durch Verkettung von vier ASCII-Zeichen gebildet wird.

 

Diese grundlegende Struktur kann durch Hinzufügen von Datei Metadaten und anderen Informationen erweitert werden, die den Rahmen dieses Tutorials sprengen.

## <a name="header-and-library-files"></a>Header-und Bibliotheksdateien

Fügen Sie die folgenden Header Dateien in das Projekt ein:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Verknüpfen Sie die folgenden Bibliotheken:

-   MF. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="implement-wmain"></a>Implementieren von wmain

Der folgende Code zeigt die Einstiegspunkt Funktion für die Anwendung.


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

1.  [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) wird aufgerufen, um die com-Bibliothek zu initialisieren.
2.  Ruft [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.
3.  Ruft [**mfkreatesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) zum Erstellen des Quell Readers auf. Diese Funktion nimmt den Namen der Eingabedatei an und empfängt einen [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Schnittstellen Zeiger.
4.  Erstellt die Ausgabedatei durch Aufrufen der **CreateFile** -Funktion, die ein Datei Handle zurückgibt.
5.  Ruft die Anwendungs definierte Funktion " [schreitewavfile](#write-the-wave-file) " auf. Diese Funktion decodiert die Audiodatei und schreibt die Wavedatei.
6.  Gibt den [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Zeiger und das Datei Handle frei.
7.  Ruft [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) auf, um die Media Foundation Plattform zu beenden.
8.  Ruft zum Freigeben der com-Bibliothek " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " auf.

## <a name="write-the-wave-file"></a>Schreiben der Wave-Datei

Die meiste Arbeit erfolgt in der- `WriteWavFile` Funktion, die von aufgerufen wird `wmain` .


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



Diese Funktion Ruft eine Reihe von anderen Anwendungs definierten Funktionen auf:

1.  Die Funktion " [konfigurierungsstream](#configure-the-source-reader) " initialisiert den Quell Reader. Diese Funktion empfängt einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle, die verwendet wird, um eine Beschreibung des decodierten Audioformats zu erhalten, einschließlich der Samplingrate, der Anzahl der Kanäle und der Bittiefe (Bits pro Stichprobe).
2.  Die Funktion "schreitewaveheader" schreibt den ersten Teil der Wave-Datei, einschließlich des Headers und des Starts des "Data"-Blocks.
3.  Die calculatemaxaudiodatasize-Funktion berechnet die maximale audiomenge in Bytes, die in die Datei geschrieben werden soll.
4.  Die Funktion "Beschreib tewavedata" schreibt die PCM-Audiodaten in die Datei.
5.  Die fixupchunksizes-Funktion schreibt die Dateigrößen Informationen, die nach den **FourCC** -Werten ' Riff ' und ' Data ' in der Wave-Datei angezeigt werden. (Diese Werte sind erst bekannt, wenn `WriteWaveData` abgeschlossen ist.)

Diese Funktionen sind in den verbleibenden Abschnitten dieses Tutorials aufgeführt.

## <a name="configure-the-source-reader"></a>Konfigurieren des Quell Readers

Die `ConfigureAudioStream` -Funktion konfiguriert den Quell Reader, um den Audiostream in der Quelldatei zu decodieren. Außerdem werden Informationen über das Format der decodierten Audiodatei zurückgegeben.

In Media Foundation werden Medienformate mithilfe von *Medientyp* Objekten beschrieben. Ein Medientyp Objekt macht die [**imbomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verfügbar, die die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle erbt. Im Wesentlichen handelt es sich bei einem Medientyp um eine Sammlung von Eigenschaften, die das Format beschreiben. Weitere Informationen finden Sie unter [Medientypen](media-types.md).


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

1.  Ruft die [**imfsourcereader:: setstreamselection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) -Methode auf, um den Audiostream auszuwählen und alle anderen Streams zu deaktivieren. Mit diesem Schritt kann die Leistung verbessert werden, da der Quell Leser nicht in Video Frames gehalten werden kann, die von der Anwendung nicht verwendet werden.
2.  Erstellt einen *partiellen* Medientyp, der PCM-Audiodaten angibt. Die-Funktion erstellt den partiellen Typ wie folgt:
    1.  Ruft [**mfkreatemediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) auf, um ein leeres Medientyp-Objekt zu erstellen.
    2.  Legt das [**MF \_ MT \_ Major \_ Type**](mf-mt-major-type-attribute.md) -Attribut auf **mfmediatype \_ -Audiodaten** fest.
    3.  Legt das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " auf das **mfaudioformat \_ PCM** fest.
3.  Ruft [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) auf, um den partiellen Typ für den Quell Leser festzulegen. Wenn die Quelldatei codierte Audiodaten enthält, lädt der Quell Leser automatisch den erforderlichen Audiodecoder.
4.  Ruft [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) auf, um den eigentlichen PCM-Medientyp zu erhalten. Diese Methode gibt einen Medientyp zurück, bei dem alle Formatierungs Details ausgefüllt sind, z. b. die audiobeispielrate und die Anzahl der Kanäle.
5.  Ruft [**imfsourcereader:: setstreamselection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) auf, um den Audiodatenstrom zu aktivieren.

## <a name="write-the-wave-file-header"></a>Schreiben des Wave-Datei Headers

Die- `WriteWaveHeader` Funktion schreibt den Wave File-Header.

Die einzige Media Foundation API, die von dieser Funktion aufgerufen wird, ist [**mfkreatewaveformatexfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), die den Medientyp in eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur konvertiert.


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



Die `WriteToFile` -Funktion ist eine einfache Hilfsfunktion, die die Funktion " **Write File** " von Windows umschließt und einen **HRESULT** -Wert zurückgibt.


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

Da die Dateigröße als 4-Byte-Wert im Dateiheader gespeichert wird, ist eine Wave-Datei auf eine maximale Größe von 0xFFFFFFFF Bytes – ca. 4 GB beschränkt. Dieser Wert enthält die Größe des Datei Headers. PCM-Audiodaten haben eine Konstante Bitrate, sodass Sie die maximale Datengröße wie folgt aus dem Audioformat berechnen können:


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



Um partielle Audioframes zu vermeiden, wird die Größe auf die Block Ausrichtung gerundet, die im [**MF \_ -MT-Attribut für die \_ \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md) gespeichert wird.

## <a name="decode-the-audio"></a>Decodieren der Audiodatei

Die `WriteWaveData` -Funktion liest decodierte Audiodaten aus der Quelldatei und schreibt in die Wave-Datei.


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



Die- `WriteWaveData` Funktion führt in einer-Schleife folgende Aktionen aus:

1.  Ruft [**imfsourcereader:: infosample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) auf, um Audiodaten aus der Quelldatei zu lesen. Der *dwFlags* -Parameter empfängt ein bitweises **or** von-Flags aus der [**MF- \_ \_ \_ quellleseflag**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) -Enumeration. Der *psample* -Parameter erhält einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, die für den Zugriff auf die Audiodaten verwendet wird. In einigen Fällen werden bei einem **CallSample-Aufrufvorgang** keine Daten generiert. in diesem Fall ist der **imfsample** -Zeiger **null**.
2.  Überprüft *dwFlags* auf die folgenden Flags:
    -   **MF \_ \_quellreaderf \_ currentmediatypeer Changed**. Dieses Flag gibt eine Formatänderung in der Quelldatei an. Die Formatänderungen werden von Wave-Dateien nicht unterstützt.
    -   **MF \_ der \_ quellreaderf \_ EndOf-Stream**. Dieses Flag gibt das Ende des Streams an.
3.  Ruft [**imfsample:: convertdecontiguousbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) auf, um einen Zeiger auf ein Puffer Objekt zu erhalten.
4.  Ruft [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) auf, um einen Zeiger auf den Pufferspeicher zu erhalten.
5.  Schreibt die Audiodaten in die Ausgabedatei.
6.  Ruft [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) auf, um das Puffer Objekt zu entsperren.

Die-Funktion wird von der-Schleife unterbrochen, wenn Folgendes auftritt:

-   Das Datenstrom Format ändert sich.
-   Das Ende des Streams ist erreicht.
-   Die maximale Menge an Audiodaten wird in die Ausgabedatei geschrieben.
-   Ein Fehler tritt auf.

## <a name="finalize-the-file-header"></a>Beenden Sie den Datei Header.

Die im Wave-Header gespeicherten Größen Werte sind erst bekannt, wenn die vorherige Funktion abgeschlossen ist. Füllt die folgenden `FixUpChunkSizes` Werte aus:


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

[Quell Leser](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 

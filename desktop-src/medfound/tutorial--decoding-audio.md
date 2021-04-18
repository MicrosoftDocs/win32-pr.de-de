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
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="8476f-103">Tutorial: Decodieren von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="8476f-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="8476f-104">In diesem Tutorial wird gezeigt, wie Sie den [Quell Leser](source-reader.md) zum Decodieren von Audiodaten aus einer Mediendatei und zum Schreiben der Audiodatei in eine Wave-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="8476f-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="8476f-105">Das Tutorial basiert auf dem Beispiel [Audioclip](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="8476f-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="8476f-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8476f-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="8476f-107">Header-und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="8476f-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="8476f-108">Implementieren von wmain</span><span class="sxs-lookup"><span data-stu-id="8476f-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="8476f-109">Schreiben der Wave-Datei</span><span class="sxs-lookup"><span data-stu-id="8476f-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="8476f-110">Konfigurieren des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="8476f-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="8476f-111">Schreiben des Wave-Datei Headers</span><span class="sxs-lookup"><span data-stu-id="8476f-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="8476f-112">Berechnen der maximalen Datengröße</span><span class="sxs-lookup"><span data-stu-id="8476f-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="8476f-113">Decodieren der Audiodatei</span><span class="sxs-lookup"><span data-stu-id="8476f-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="8476f-114">Beenden Sie den Datei Header.</span><span class="sxs-lookup"><span data-stu-id="8476f-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="8476f-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8476f-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="8476f-116">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8476f-116">Overview</span></span>

<span data-ttu-id="8476f-117">In diesem Tutorial erstellen Sie eine Konsolenanwendung, die zwei Befehlszeilenargumente annimmt: den Namen einer Eingabedatei, die einen Audiodatenstrom enthält, und den Namen der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="8476f-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="8476f-118">Die Anwendung liest fünf Sekunden Audiodaten aus der Eingabedatei und schreibt die Audiodaten als wellendaten in die Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="8476f-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="8476f-119">Die Anwendung verwendet das Quell Lese Objekt, um die decodierten Audiodaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8476f-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="8476f-120">Der Quell Leser macht die [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8476f-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="8476f-121">Die Anwendungen verwenden Windows-e/a-Funktionen, um die decodierte Audiodatei in die Wave-Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="8476f-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="8476f-122">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8476f-122">The following image illustrates this process.</span></span>

![das Diagramm zeigt den Quell Leser, der Audiodaten aus der Quelldatei erhält.](images/audio-clip-tutorial.gif)

<span data-ttu-id="8476f-124">In seiner einfachsten Form hat eine Wave-Datei die folgende Struktur:</span><span class="sxs-lookup"><span data-stu-id="8476f-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="8476f-125">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8476f-125">Data Type</span></span>                              | <span data-ttu-id="8476f-126">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="8476f-126">Size (Bytes)</span></span> | <span data-ttu-id="8476f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8476f-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8476f-128">**FourCC**</span><span class="sxs-lookup"><span data-stu-id="8476f-128">**FOURCC**</span></span>                             | <span data-ttu-id="8476f-129">4</span><span class="sxs-lookup"><span data-stu-id="8476f-129">4</span></span>            | <span data-ttu-id="8476f-130">FF</span><span class="sxs-lookup"><span data-stu-id="8476f-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="8476f-131">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8476f-131">**DWORD**</span></span>                              | <span data-ttu-id="8476f-132">4</span><span class="sxs-lookup"><span data-stu-id="8476f-132">4</span></span>            | <span data-ttu-id="8476f-133">Gesamt Dateigröße ohne die ersten 8 Bytes</span><span class="sxs-lookup"><span data-stu-id="8476f-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="8476f-134">**FourCC**</span><span class="sxs-lookup"><span data-stu-id="8476f-134">**FOURCC**</span></span>                             | <span data-ttu-id="8476f-135">4</span><span class="sxs-lookup"><span data-stu-id="8476f-135">4</span></span>            | <span data-ttu-id="8476f-136">Welle</span><span class="sxs-lookup"><span data-stu-id="8476f-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="8476f-137">**FourCC**</span><span class="sxs-lookup"><span data-stu-id="8476f-137">**FOURCC**</span></span>                             | <span data-ttu-id="8476f-138">4</span><span class="sxs-lookup"><span data-stu-id="8476f-138">4</span></span>            | <span data-ttu-id="8476f-139">fmt</span><span class="sxs-lookup"><span data-stu-id="8476f-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="8476f-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8476f-140">**DWORD**</span></span>                              | <span data-ttu-id="8476f-141">4</span><span class="sxs-lookup"><span data-stu-id="8476f-141">4</span></span>            | <span data-ttu-id="8476f-142">Größe der folgenden [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Daten.</span><span class="sxs-lookup"><span data-stu-id="8476f-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="8476f-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8476f-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="8476f-144">Varies</span><span class="sxs-lookup"><span data-stu-id="8476f-144">Varies</span></span>       | <span data-ttu-id="8476f-145">Audioformatierungs Header.</span><span class="sxs-lookup"><span data-stu-id="8476f-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="8476f-146">**FourCC**</span><span class="sxs-lookup"><span data-stu-id="8476f-146">**FOURCC**</span></span>                             | <span data-ttu-id="8476f-147">4</span><span class="sxs-lookup"><span data-stu-id="8476f-147">4</span></span>            | <span data-ttu-id="8476f-148">Vorrats</span><span class="sxs-lookup"><span data-stu-id="8476f-148">'data'</span></span>                                                                |
| <span data-ttu-id="8476f-149">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8476f-149">**DWORD**</span></span>                              | <span data-ttu-id="8476f-150">4</span><span class="sxs-lookup"><span data-stu-id="8476f-150">4</span></span>            | <span data-ttu-id="8476f-151">Größe der Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8476f-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="8476f-152">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="8476f-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="8476f-153">Varies</span><span class="sxs-lookup"><span data-stu-id="8476f-153">Varies</span></span>       | <span data-ttu-id="8476f-154">Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8476f-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="8476f-155">Ein **FourCC** ist ein **DWORD** , das durch Verkettung von vier ASCII-Zeichen gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="8476f-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="8476f-156">Diese grundlegende Struktur kann durch Hinzufügen von Datei Metadaten und anderen Informationen erweitert werden, die den Rahmen dieses Tutorials sprengen.</span><span class="sxs-lookup"><span data-stu-id="8476f-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="8476f-157">Header-und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="8476f-157">Header and Library Files</span></span>

<span data-ttu-id="8476f-158">Fügen Sie die folgenden Header Dateien in das Projekt ein:</span><span class="sxs-lookup"><span data-stu-id="8476f-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="8476f-159">Verknüpfen Sie die folgenden Bibliotheken:</span><span class="sxs-lookup"><span data-stu-id="8476f-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="8476f-160">MF. lib</span><span class="sxs-lookup"><span data-stu-id="8476f-160">mfplat.lib</span></span>
-   <span data-ttu-id="8476f-161">mfreadwrite. lib</span><span class="sxs-lookup"><span data-stu-id="8476f-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="8476f-162">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="8476f-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="8476f-163">Implementieren von wmain</span><span class="sxs-lookup"><span data-stu-id="8476f-163">Implement wmain</span></span>

<span data-ttu-id="8476f-164">Der folgende Code zeigt die Einstiegspunkt Funktion für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8476f-164">The following code shows the entry-point function for the application.</span></span>


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



<span data-ttu-id="8476f-165">Diese Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8476f-165">This function does the following:</span></span>

1.  <span data-ttu-id="8476f-166">[**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) wird aufgerufen, um die com-Bibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8476f-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="8476f-167">Ruft [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8476f-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="8476f-168">Ruft [**mfkreatesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) zum Erstellen des Quell Readers auf.</span><span class="sxs-lookup"><span data-stu-id="8476f-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="8476f-169">Diese Funktion nimmt den Namen der Eingabedatei an und empfängt einen [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8476f-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="8476f-170">Erstellt die Ausgabedatei durch Aufrufen der **CreateFile** -Funktion, die ein Datei Handle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8476f-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="8476f-171">Ruft die Anwendungs definierte Funktion " [schreitewavfile](#write-the-wave-file) " auf.</span><span class="sxs-lookup"><span data-stu-id="8476f-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="8476f-172">Diese Funktion decodiert die Audiodatei und schreibt die Wavedatei.</span><span class="sxs-lookup"><span data-stu-id="8476f-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="8476f-173">Gibt den [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Zeiger und das Datei Handle frei.</span><span class="sxs-lookup"><span data-stu-id="8476f-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="8476f-174">Ruft [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) auf, um die Media Foundation Plattform zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8476f-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="8476f-175">Ruft zum Freigeben der com-Bibliothek " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " auf.</span><span class="sxs-lookup"><span data-stu-id="8476f-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="8476f-176">Schreiben der Wave-Datei</span><span class="sxs-lookup"><span data-stu-id="8476f-176">Write the WAVE File</span></span>

<span data-ttu-id="8476f-177">Die meiste Arbeit erfolgt in der- `WriteWavFile` Funktion, die von aufgerufen wird `wmain` .</span><span class="sxs-lookup"><span data-stu-id="8476f-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


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



<span data-ttu-id="8476f-178">Diese Funktion Ruft eine Reihe von anderen Anwendungs definierten Funktionen auf:</span><span class="sxs-lookup"><span data-stu-id="8476f-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="8476f-179">Die Funktion " [konfigurierungsstream](#configure-the-source-reader) " initialisiert den Quell Reader.</span><span class="sxs-lookup"><span data-stu-id="8476f-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="8476f-180">Diese Funktion empfängt einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle, die verwendet wird, um eine Beschreibung des decodierten Audioformats zu erhalten, einschließlich der Samplingrate, der Anzahl der Kanäle und der Bittiefe (Bits pro Stichprobe).</span><span class="sxs-lookup"><span data-stu-id="8476f-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="8476f-181">Die Funktion "schreitewaveheader" schreibt den ersten Teil der Wave-Datei, einschließlich des Headers und des Starts des "Data"-Blocks.</span><span class="sxs-lookup"><span data-stu-id="8476f-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="8476f-182">Die calculatemaxaudiodatasize-Funktion berechnet die maximale audiomenge in Bytes, die in die Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8476f-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="8476f-183">Die Funktion "Beschreib tewavedata" schreibt die PCM-Audiodaten in die Datei.</span><span class="sxs-lookup"><span data-stu-id="8476f-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="8476f-184">Die fixupchunksizes-Funktion schreibt die Dateigrößen Informationen, die nach den **FourCC** -Werten ' Riff ' und ' Data ' in der Wave-Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8476f-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="8476f-185">(Diese Werte sind erst bekannt, wenn `WriteWaveData` abgeschlossen ist.)</span><span class="sxs-lookup"><span data-stu-id="8476f-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="8476f-186">Diese Funktionen sind in den verbleibenden Abschnitten dieses Tutorials aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8476f-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="8476f-187">Konfigurieren des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="8476f-187">Configure the Source Reader</span></span>

<span data-ttu-id="8476f-188">Die `ConfigureAudioStream` -Funktion konfiguriert den Quell Reader, um den Audiostream in der Quelldatei zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="8476f-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="8476f-189">Außerdem werden Informationen über das Format der decodierten Audiodatei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8476f-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="8476f-190">In Media Foundation werden Medienformate mithilfe von *Medientyp* Objekten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8476f-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="8476f-191">Ein Medientyp Objekt macht die [**imbomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verfügbar, die die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="8476f-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="8476f-192">Im Wesentlichen handelt es sich bei einem Medientyp um eine Sammlung von Eigenschaften, die das Format beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8476f-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="8476f-193">Weitere Informationen finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="8476f-193">For more information, see [Media Types](media-types.md).</span></span>


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



<span data-ttu-id="8476f-194">Die `ConfigureAudioStream` Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8476f-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="8476f-195">Ruft die [**imfsourcereader:: setstreamselection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) -Methode auf, um den Audiostream auszuwählen und alle anderen Streams zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8476f-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="8476f-196">Mit diesem Schritt kann die Leistung verbessert werden, da der Quell Leser nicht in Video Frames gehalten werden kann, die von der Anwendung nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8476f-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="8476f-197">Erstellt einen *partiellen* Medientyp, der PCM-Audiodaten angibt.</span><span class="sxs-lookup"><span data-stu-id="8476f-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="8476f-198">Die-Funktion erstellt den partiellen Typ wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8476f-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="8476f-199">Ruft [**mfkreatemediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) auf, um ein leeres Medientyp-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8476f-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="8476f-200">Legt das [**MF \_ MT \_ Major \_ Type**](mf-mt-major-type-attribute.md) -Attribut auf **mfmediatype \_ -Audiodaten** fest.</span><span class="sxs-lookup"><span data-stu-id="8476f-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="8476f-201">Legt das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " auf das **mfaudioformat \_ PCM** fest.</span><span class="sxs-lookup"><span data-stu-id="8476f-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="8476f-202">Ruft [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) auf, um den partiellen Typ für den Quell Leser festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8476f-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="8476f-203">Wenn die Quelldatei codierte Audiodaten enthält, lädt der Quell Leser automatisch den erforderlichen Audiodecoder.</span><span class="sxs-lookup"><span data-stu-id="8476f-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="8476f-204">Ruft [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) auf, um den eigentlichen PCM-Medientyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8476f-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="8476f-205">Diese Methode gibt einen Medientyp zurück, bei dem alle Formatierungs Details ausgefüllt sind, z. b. die audiobeispielrate und die Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="8476f-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="8476f-206">Ruft [**imfsourcereader:: setstreamselection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) auf, um den Audiodatenstrom zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8476f-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="8476f-207">Schreiben des Wave-Datei Headers</span><span class="sxs-lookup"><span data-stu-id="8476f-207">Write the WAVE File Header</span></span>

<span data-ttu-id="8476f-208">Die- `WriteWaveHeader` Funktion schreibt den Wave File-Header.</span><span class="sxs-lookup"><span data-stu-id="8476f-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="8476f-209">Die einzige Media Foundation API, die von dieser Funktion aufgerufen wird, ist [**mfkreatewaveformatexfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), die den Medientyp in eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur konvertiert.</span><span class="sxs-lookup"><span data-stu-id="8476f-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


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



<span data-ttu-id="8476f-210">Die `WriteToFile` -Funktion ist eine einfache Hilfsfunktion, die die Funktion " **Write File** " von Windows umschließt und einen **HRESULT** -Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8476f-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


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



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="8476f-211">Berechnen der maximalen Datengröße</span><span class="sxs-lookup"><span data-stu-id="8476f-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="8476f-212">Da die Dateigröße als 4-Byte-Wert im Dateiheader gespeichert wird, ist eine Wave-Datei auf eine maximale Größe von 0xFFFFFFFF Bytes – ca. 4 GB beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8476f-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="8476f-213">Dieser Wert enthält die Größe des Datei Headers.</span><span class="sxs-lookup"><span data-stu-id="8476f-213">This value includes the size of the file header.</span></span> <span data-ttu-id="8476f-214">PCM-Audiodaten haben eine Konstante Bitrate, sodass Sie die maximale Datengröße wie folgt aus dem Audioformat berechnen können:</span><span class="sxs-lookup"><span data-stu-id="8476f-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


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



<span data-ttu-id="8476f-215">Um partielle Audioframes zu vermeiden, wird die Größe auf die Block Ausrichtung gerundet, die im [**MF \_ -MT-Attribut für die \_ \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8476f-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="8476f-216">Decodieren der Audiodatei</span><span class="sxs-lookup"><span data-stu-id="8476f-216">Decode the Audio</span></span>

<span data-ttu-id="8476f-217">Die `WriteWaveData` -Funktion liest decodierte Audiodaten aus der Quelldatei und schreibt in die Wave-Datei.</span><span class="sxs-lookup"><span data-stu-id="8476f-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


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



<span data-ttu-id="8476f-218">Die- `WriteWaveData` Funktion führt in einer-Schleife folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="8476f-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="8476f-219">Ruft [**imfsourcereader:: infosample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) auf, um Audiodaten aus der Quelldatei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="8476f-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="8476f-220">Der *dwFlags* -Parameter empfängt ein bitweises **or** von-Flags aus der [**MF- \_ \_ \_ quellleseflag**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="8476f-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="8476f-221">Der *psample* -Parameter erhält einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, die für den Zugriff auf die Audiodaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8476f-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="8476f-222">In einigen Fällen werden bei einem **CallSample-Aufrufvorgang** keine Daten generiert. in diesem Fall ist der **imfsample** -Zeiger **null**.</span><span class="sxs-lookup"><span data-stu-id="8476f-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="8476f-223">Überprüft *dwFlags* auf die folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="8476f-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="8476f-224">**MF \_ \_quellreaderf \_ currentmediatypeer Changed**.</span><span class="sxs-lookup"><span data-stu-id="8476f-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="8476f-225">Dieses Flag gibt eine Formatänderung in der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="8476f-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="8476f-226">Die Formatänderungen werden von Wave-Dateien nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8476f-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="8476f-227">**MF \_ der \_ quellreaderf \_ EndOf-Stream**.</span><span class="sxs-lookup"><span data-stu-id="8476f-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="8476f-228">Dieses Flag gibt das Ende des Streams an.</span><span class="sxs-lookup"><span data-stu-id="8476f-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="8476f-229">Ruft [**imfsample:: convertdecontiguousbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) auf, um einen Zeiger auf ein Puffer Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8476f-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="8476f-230">Ruft [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) auf, um einen Zeiger auf den Pufferspeicher zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8476f-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="8476f-231">Schreibt die Audiodaten in die Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="8476f-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="8476f-232">Ruft [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) auf, um das Puffer Objekt zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="8476f-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="8476f-233">Die-Funktion wird von der-Schleife unterbrochen, wenn Folgendes auftritt:</span><span class="sxs-lookup"><span data-stu-id="8476f-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="8476f-234">Das Datenstrom Format ändert sich.</span><span class="sxs-lookup"><span data-stu-id="8476f-234">The stream format changes.</span></span>
-   <span data-ttu-id="8476f-235">Das Ende des Streams ist erreicht.</span><span class="sxs-lookup"><span data-stu-id="8476f-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="8476f-236">Die maximale Menge an Audiodaten wird in die Ausgabedatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8476f-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="8476f-237">Ein Fehler tritt auf.</span><span class="sxs-lookup"><span data-stu-id="8476f-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="8476f-238">Beenden Sie den Datei Header.</span><span class="sxs-lookup"><span data-stu-id="8476f-238">Finalize the File Header</span></span>

<span data-ttu-id="8476f-239">Die im Wave-Header gespeicherten Größen Werte sind erst bekannt, wenn die vorherige Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8476f-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="8476f-240">Füllt die folgenden `FixUpChunkSizes` Werte aus:</span><span class="sxs-lookup"><span data-stu-id="8476f-240">The `FixUpChunkSizes` fills in these values:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8476f-241">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8476f-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8476f-242">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="8476f-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="8476f-243">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="8476f-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="8476f-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="8476f-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 

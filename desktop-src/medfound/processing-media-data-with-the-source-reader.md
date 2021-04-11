---
description: In diesem Thema wird beschrieben, wie Sie den Quell Leser zum Verarbeiten von Mediendaten verwenden können.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Verwenden des Quell Readers zum Verarbeiten von Mediendaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351179"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Verwenden des Quell Readers zum Verarbeiten von Mediendaten

In diesem Thema wird beschrieben, wie Sie den [Quell Leser](source-reader.md) zum Verarbeiten von Mediendaten verwenden können.

Führen Sie die folgenden grundlegenden Schritte aus, um den Quell Leser zu verwenden:

1.  Erstellen Sie eine Instanz des Quell Readers.
2.  Listet die möglichen Ausgabeformate auf.
3.  Legen Sie das tatsächliche Ausgabeformat für jeden Stream fest.
4.  Verarbeiten von Daten aus der Quelle.

Im restlichen Teil dieses Themas werden diese Schritte ausführlich beschrieben.

-   [Erstellen des Quell Readers](#creating-the-source-reader)
-   [Auflisten von Ausgabeformaten](#enumerating-output-formats)
-   [Festlegen von Ausgabeformaten](#setting-output-formats)
-   [Verarbeiten von Mediendaten](#using-the-source-reader-to-process-media-data)
-   [Ableiten der Daten Pipeline](#draining-the-data-pipeline)
-   [Die Datei Dauer wird erhalten.](#getting-the-file-duration)
-   [Diejenigen](#seeking)
-   [Wiedergabe Rate](#playback-rate)
-   [Hardware Beschleunigung](#hardware-acceleration)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-source-reader"></a>Erstellen des Quell Readers

Rufen Sie eine der folgenden Funktionen auf, um eine Instanz des Quell Readers zu erstellen:



| Funktion                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Nimmt eine URL als Eingabe an. Diese Funktion verwendet den [quellresolver](source-resolver.md) , um eine Medienquelle aus der URL zu erstellen.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Nimmt einen Zeiger auf einen Bytestream. Diese Funktion verwendet auch den quellresolver, um die Medienquelle zu erstellen.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Nimmt einen Zeiger auf eine Medienquelle an, die bereits erstellt wurde. Diese Funktion ist nützlich für Medienquellen, die der quellresolver nicht erstellen kann, z. b. Geräte Erfassungsgeräte oder benutzerdefinierte Medienquellen.<br/> |



 

Verwenden Sie in der Regel [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)für Mediendateien. Verwenden Sie für Geräte wie z. b. Webcams [**mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Weitere Informationen zu Erfassungs Geräten in Microsoft Media Foundation finden Sie unter [Audio-/Video-Erfassung](audio-video-capture.md).)

Jede dieser Funktionen verwendet einen optionalen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der verwendet wird, um verschiedene Optionen für den Quell Leser festzulegen, wie in den Referenz Themen für diese Funktionen beschrieben. Legen Sie diesen Parameter auf **null** fest, um das Standardverhalten zu erhalten. Jede Funktion gibt einen [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Zeiger als Ausgabeparameter zurück. Sie müssen die Funktion **CoInitialize (ex)** und [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) aufrufen, bevor Sie eine dieser Funktionen aufrufen.

Der folgende Code erstellt den Quell Leser aus einer URL.


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>Auflisten von Ausgabeformaten

Jede Medienquelle hat mindestens einen Datenstrom. Eine Videodatei könnte z. b. einen Videostream und einen Audiostream enthalten. Das Format der einzelnen Datenströme wird mit einem Medientyp beschrieben, der von der [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle dargestellt wird. Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md). Sie müssen den Medientyp überprüfen, um das Format der Daten zu verstehen, die Sie vom Quell Leser erhalten.

Anfänglich hat jeder Stream ein Standardformat, das Sie durch Aufrufen der [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) -Methode finden können:

Für jeden Stream bietet die Medienquelle eine Liste möglicher Medientypen für diesen Stream. Die Anzahl der Typen hängt von der Quelle ab. Wenn die Quelle eine Mediendatei darstellt, ist in der Regel nur ein Typ pro Stream vorhanden. Auf der anderen Seite kann eine Webcam möglicherweise Videos in verschiedenen Formaten streamen. In diesem Fall kann die Anwendung das zu verwendende Format aus der Liste der Medientypen auswählen.

Um einen der Medientypen für einen Stream abzurufen, müssen Sie die [**imfsourcereader:: getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) -Methode aufrufen. Diese Methode nimmt zwei Index Parameter an: den Index des Streams und einen Index in die Liste der Medientypen für den Datenstrom. Um alle Typen für einen Stream aufzulisten, erhöhen Sie den Listen Index, während Sie die Datenstrom-Index Konstante beibehalten. Wenn der Listen Index außerhalb des gültigen Bereichs liegt, gibt **getnativemediatype** den **\_ Typ MF E \_ nicht \_ mehr \_** zurück.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



Um die Medientypen für jeden Stream aufzulisten, erhöhen Sie den streamindex. Wenn der Stream-Index außerhalb des gültigen Bereichs liegt, gibt [**getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) den Wert " **MF \_ E \_ invalidstreamnumber**" zurück.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Festlegen von Ausgabeformaten

Um das Ausgabeformat zu ändern, müssen Sie die [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) -Methode aufrufen. Diese Methode nimmt den streamindex und einen Medientyp an:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Der Medientyp hängt davon ab, ob ein Decoder eingefügt werden soll.

-   Um Daten direkt aus der Quelle zu erhalten, ohne Sie zu decodieren, verwenden Sie einen der Typen, die von [**getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype)zurückgegeben werden.
-   Um den Stream zu decodieren, erstellen Sie einen neuen Medientyp, der das gewünschte unkomprimierte Format beschreibt.

Erstellen Sie im Fall des Decoders den Medientyp wie folgt:

1.  Rufen Sie [**mfkreatemediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) auf, um einen neuen Medientyp zu erstellen.
2.  Legen Sie das Attribut " [**MF- \_ \_ \_ Haupttyp**](mf-mt-major-type-attribute.md) " auf "Audiodatei oder Video" fest.
3.  Legen Sie das Attribut " [**MF \_ MT \_ Untertyp**](mf-mt-subtype-attribute.md) " fest, um den Untertyp des Decodierungs Formats anzugeben. (Siehe [audiountertyp-GUIDs](audio-subtype-guids.md) und [Video Untertyp-GUIDs](video-subtype-guids.md).)
4.  [**Imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)aufrufen.

Der Quell Leser lädt den Decoder automatisch. Um die vollständigen Details des decodierten Formats abzurufen, müssen Sie [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) nach dem Aufrufen von [**setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) aufrufen.

Der folgende Code konfiguriert den Videostream für RGB-32 und den Audiostream für PCM-Audiodaten.


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>Verarbeiten von Mediendaten

Um Mediendaten aus der Quelle abzurufen, nennen Sie die [**imfsourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode, wie im folgenden Code gezeigt.


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



Der erste Parameter ist der Index des Streams, für den Sie Daten erhalten möchten. Sie können auch den **MF- \_ Quell \_ Leser beliebige Daten \_ \_ Ströme** angeben, um die nächsten verfügbaren Daten aus einem beliebigen Stream zu erhalten. Der zweite Parameter enthält optionale Flags. eine Liste der folgenden Informationen finden Sie unter [**\_ \_ \_ Kontroll \_ Flag für das MF-Quell Lese**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) Programm. Der dritte Parameter empfängt den Index des Datenstroms, der die Daten tatsächlich erzeugt. Sie benötigen diese Informationen, wenn Sie den ersten Parameter auf den **MF- \_ Quell \_ Leser \_ Any \_ Stream** festlegen. Der vierte Parameter empfängt Statusflags und zeigt verschiedene Ereignisse an, die beim Lesen der Daten auftreten können, z. b. das Formatieren von Änderungen im Stream. Eine Liste der Statusflags finden Sie unter Flag für das [**MF- \_ \_ quelllesegerät \_**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Wenn die Medienquelle Daten für den angeforderten Datenstrom liefern kann, empfängt der letzte Parameter von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle eines Medien Beispiel Objekts. Verwenden Sie das Medien Beispiel für Folgendes:

-   Einen Zeiger auf die Mediendaten erhalten.
-   Die Präsentationszeit und die Stichproben Dauer erhalten.
-   Erhalten Sie Attribute, die das Interlacing, die Feld Dominanz und andere Aspekte des Beispiels beschreiben.

Der Inhalt der Mediendaten hängt vom Format des Streams ab. Bei einem unkomprimierten Videostream enthält jedes Medien Beispiel einen einzelnen Videoframe. Bei einem unkomprimierten Audiodatenstrom enthält jedes Medien Beispiel eine Sequenz von Audioframes.

Die Methode "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " kann " **S \_ OK** " zurückgeben und aber kein Medien Beispiel im *psample* -Parameter zurückgeben. Wenn Sie z. b. das Ende der Datei erreichen, legt " **infosample** " das " **MF \_ Source \_ readerf \_ EndOfStream** "-Flag in " *dwFlags* " fest und legt *psample* auf **null** fest. In diesem Fall gibt die Methode "read **Sample** " den Wert " **S \_ OK** " zurück, da kein Fehler aufgetreten ist, obwohl der *psample* -Parameter auf **null** festgelegt ist. Überprüfen Sie daher vor der Dereferenzierung immer den Wert von *psample* .

Der folgende Code zeigt, wie Sie " [**infosample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " in einer Schleife aufzurufen und die von der-Methode zurückgegebenen Informationen überprüfen, bis das Ende der Mediendatei erreicht ist.


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>Ableiten der Daten Pipeline

Während der Datenverarbeitung kann ein Decoder oder eine andere Transformation Eingabe Beispiele Puffern. In der folgenden Abbildung Ruft die Anwendung " [**lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " auf und empfängt ein Beispiel mit einer Präsentationszeit von *T1*. Der Decoder hält Beispiele für *T2* und *T3*.

![eine Abbildung, die die Pufferung in einem Decoder anzeigt.](images/sourcereader02.png)

Beim nächsten Aufrufe von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)" kann der Quell Leser *T4* an den Decoder übergeben und *T2* an die Anwendung zurückgeben.

Wenn Sie alle im Decoder gepufferten Beispiele decodieren möchten, ohne neue Beispiele an den Decoder zu übergeben, legen Sie das **\_ \_ \_ controlf \_** -ablaufflag des MF-Quell Readers im *dwcontrolflags* -Parameter von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)" fest. Fahren Sie mit der Durchführung der Schritte in einer Schleife fort, bis in "read **Sample** " ein **null** -Beispiel Abhängig davon, wie der Decoder Beispiele puffert, kann dies sofort oder nach mehreren Aufrufen von "read **Sample**" vorkommen.

## <a name="getting-the-file-duration"></a>Die Datei Dauer wird erhalten.

Um die Dauer einer Mediendatei abzurufen, nennen Sie die [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) -Methode, und fordern Sie das [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut an, wie im folgenden Code gezeigt.


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



Die hier gezeigte Funktion Ruft die Dauer in 100-Nanosekunden-Einheiten ab. Dividieren Sie durch 10 Millionen, um die Dauer in Sekunden zu erhalten.

## <a name="seeking"></a>Diejenigen

Eine Medienquelle, die Daten aus einer lokalen Datei abruft, kann in der Regel nach beliebigen Positionen in der Datei suchen. Erfassungsgeräte wie z. b. Webcams können im Allgemeinen nicht suchen, da die Daten Live sind. Eine Quelle, die Daten über ein Netzwerk streamt, kann je nach netzwerkstreamingprotokoll suchen.

Um herauszufinden, ob eine Medienquelle suchen kann, wenden Sie [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) an, und fordern Sie das [MF- \_ Quell \_ Leser \_ MediaSource \_](mf-source-reader-mediasource-characteristics.md) -Attribut Attribut an, wie im folgenden Code gezeigt:


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



Diese Funktion Ruft einen Satz von funktionsflags aus der Quelle ab. Diese Flags sind in der Enumeration " [**mfmediasource- \_ Merkmale**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) " definiert. Zwei Flags beziehen sich auf die Suche:



| Flag                                                                                                                                      | Beschreibung                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**mfmediasource \_ kann \_ Suchen**<br/>                 | Die Quelle kann suchen.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**mfmediasource \_ hat \_ langsame \_ Suche**<br/> | Die Suche kann viel Zeit in Anspruch nehmen. Beispielsweise muss die Quelle möglicherweise die gesamte Datei herunterladen, bevor Sie suchen kann. (Es gibt keine strengen Kriterien, damit eine Quelle dieses Flag zurückgibt.)<br/> |



 

Die folgenden Code Tests für das **mfmediasource-Flag können das Flag \_ \_ Suchen** .


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



Um zu suchen, nennen Sie die [**imfsourcereader:: setcurrentposition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) -Methode, wie im folgenden Code gezeigt.


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Der erste Parameter gibt das Zeitformat an, das Sie verwenden, um die Suchposition anzugeben. Alle Medienquellen in Media Foundation müssen 100-Nanosecond-Einheiten unterstützen, die durch den Wert **GUID \_ null** angegeben werden. Der zweite Parameter ist ein **PROPVARIANT** -Wert, der die Suchposition enthält. Bei 100-Nanosecond-Zeiteinheiten ist der Datentyp **Longlong**.

Beachten Sie, dass nicht jede Medienquelle eine Frame genaue Suche bereitstellt. Die Genauigkeit der Suche hängt von mehreren Faktoren ab, z. b. dem Keyframe-Intervall, von der Angabe, ob die Mediendatei einen Index enthält, und davon, ob die Daten eine Konstante oder eine Variable Bitrate enthalten. Daher gibt es keine Garantie, dass der Zeitstempel im nächsten Beispiel genau mit der angeforderten Position übereinstimmt, nachdem Sie eine Position in einer Datei gesucht haben. Im Allgemeinen ist die tatsächliche Position nicht später als die angeforderte Position, sodass Sie die Beispiele verwerfen können, bis Sie den gewünschten Punkt im Stream erreichen.

## <a name="playback-rate"></a>Wiedergabe Rate

Obwohl Sie die Wiedergabe Rate mithilfe des Quell Readers festlegen können, ist dies aus den folgenden Gründen in der Regel nicht sehr nützlich:

-   Der Quell Reader unterstützt die umgekehrte Wiedergabe auch dann nicht, wenn die Medienquelle dies tut.
-   Die Anwendung steuert die Präsentations Zeiten, sodass die Anwendung schnelles oder langsames spielen implementieren kann, ohne die Rate der Quelle festzulegen.
-   Einige Medienquellen unterstützen den Modus " *dünn* ", bei dem die Quelle weniger Stichproben liefert – in der Regel nur die Keyframes. Wenn Sie jedoch nicht Keyframes löschen möchten, können Sie die einzelnen Beispiele für das [ \_ Cleanpoint-Attribut "mfsampleextension](mfsampleextension-cleanpoint-attribute.md) " überprüfen.

Um die Wiedergabe Rate mithilfe des Quell Readers festzulegen, müssen Sie die [**imfsourcereader:: getserviceforstream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) -Methode aufrufen, um die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -und [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstellen aus der Medienquelle abzurufen.

## <a name="hardware-acceleration"></a>Hardwarebeschleunigung

Der Quell Leser ist mit Microsoft DirectX Video Acceleration (DXVA) 2,0 für Hardware beschleunigter Video-Decodierung kompatibel. Um DXVA mit dem Quell Leser zu verwenden, führen Sie die folgenden Schritte aus.

1.  Erstellen Sie ein Microsoft Direct3D-Gerät.
2.  Rufen Sie die [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) -Funktion zum Erstellen des Direct3D-Geräte-Managers auf. Diese Funktion erhält einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle.
3.  Aufrufen der [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) -Methode mit einem Zeiger auf das Direct3D-Gerät.
4.  Erstellen Sie einen Attribut Speicher, indem Sie die [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) -Funktion aufrufen.
5.  Erstellen Sie den Quell Reader. Übergeben Sie den Attribut Speicher im *pattributes* -Parameter der Erstellungs Funktion.

Wenn Sie ein Direct3D-Gerät bereitstellen, ordnet der Quell Leser Videobeispiele zu, die mit der DXVA-Videoprozessor-API kompatibel sind. Sie können die DXVA-Videoverarbeitung verwenden, um Hardware Deinterlacing oder Video Mischung auszuführen. Weitere Informationen finden Sie unter [DXVA Video Processing](dxva-video-processing.md). Wenn der Decoder außerdem DXVA 2,0 unterstützt, wird das Direct3D-Gerät verwendet, um eine hardwarebeschleunigte Decodierung durchzuführen.

> [!IMPORTANT]
> Ab Windows 8 kann [**imsdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anstelle von [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)verwendet werden. Für Windows Store-Apps müssen Sie **IMF dxgidevicemanager** verwenden. Weitere Informationen finden Sie in den [Video-APIs Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quell Leser](source-reader.md)
</dt> </dl>

 

 





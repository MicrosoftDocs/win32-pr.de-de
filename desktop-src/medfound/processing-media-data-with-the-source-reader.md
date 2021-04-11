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
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="4e9fd-103">Verwenden des Quell Readers zum Verarbeiten von Mediendaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="4e9fd-104">In diesem Thema wird beschrieben, wie Sie den [Quell Leser](source-reader.md) zum Verarbeiten von Mediendaten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="4e9fd-105">Führen Sie die folgenden grundlegenden Schritte aus, um den Quell Leser zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="4e9fd-106">Erstellen Sie eine Instanz des Quell Readers.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="4e9fd-107">Listet die möglichen Ausgabeformate auf.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="4e9fd-108">Legen Sie das tatsächliche Ausgabeformat für jeden Stream fest.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="4e9fd-109">Verarbeiten von Daten aus der Quelle.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-109">Process data from the source.</span></span>

<span data-ttu-id="4e9fd-110">Im restlichen Teil dieses Themas werden diese Schritte ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="4e9fd-111">Erstellen des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="4e9fd-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="4e9fd-112">Auflisten von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="4e9fd-113">Festlegen von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="4e9fd-114">Verarbeiten von Mediendaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="4e9fd-115">Ableiten der Daten Pipeline</span><span class="sxs-lookup"><span data-stu-id="4e9fd-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="4e9fd-116">Die Datei Dauer wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="4e9fd-117">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="4e9fd-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="4e9fd-118">Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="4e9fd-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="4e9fd-119">Hardware Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="4e9fd-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="4e9fd-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e9fd-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="4e9fd-121">Erstellen des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="4e9fd-121">Creating the Source Reader</span></span>

<span data-ttu-id="4e9fd-122">Rufen Sie eine der folgenden Funktionen auf, um eine Instanz des Quell Readers zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="4e9fd-123">Funktion</span><span class="sxs-lookup"><span data-stu-id="4e9fd-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="4e9fd-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e9fd-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9fd-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="4e9fd-126">Nimmt eine URL als Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-126">Takes a URL as input.</span></span> <span data-ttu-id="4e9fd-127">Diese Funktion verwendet den [quellresolver](source-resolver.md) , um eine Medienquelle aus der URL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="4e9fd-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="4e9fd-129">Nimmt einen Zeiger auf einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="4e9fd-130">Diese Funktion verwendet auch den quellresolver, um die Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="4e9fd-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="4e9fd-132">Nimmt einen Zeiger auf eine Medienquelle an, die bereits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="4e9fd-133">Diese Funktion ist nützlich für Medienquellen, die der quellresolver nicht erstellen kann, z. b. Geräte Erfassungsgeräte oder benutzerdefinierte Medienquellen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="4e9fd-134">Verwenden Sie in der Regel [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)für Mediendateien.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="4e9fd-135">Verwenden Sie für Geräte wie z. b. Webcams [**mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="4e9fd-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="4e9fd-136">(Weitere Informationen zu Erfassungs Geräten in Microsoft Media Foundation finden Sie unter [Audio-/Video-Erfassung](audio-video-capture.md).)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="4e9fd-137">Jede dieser Funktionen verwendet einen optionalen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der verwendet wird, um verschiedene Optionen für den Quell Leser festzulegen, wie in den Referenz Themen für diese Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="4e9fd-138">Legen Sie diesen Parameter auf **null** fest, um das Standardverhalten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="4e9fd-139">Jede Funktion gibt einen [**IMF sourcereader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) -Zeiger als Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="4e9fd-140">Sie müssen die Funktion **CoInitialize (ex)** und [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) aufrufen, bevor Sie eine dieser Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="4e9fd-141">Der folgende Code erstellt den Quell Leser aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-141">The following code creates the Source Reader from a URL.</span></span>


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



## <a name="enumerating-output-formats"></a><span data-ttu-id="4e9fd-142">Auflisten von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-142">Enumerating Output Formats</span></span>

<span data-ttu-id="4e9fd-143">Jede Medienquelle hat mindestens einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-143">Every media source has at least one stream.</span></span> <span data-ttu-id="4e9fd-144">Eine Videodatei könnte z. b. einen Videostream und einen Audiostream enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="4e9fd-145">Das Format der einzelnen Datenströme wird mit einem Medientyp beschrieben, der von der [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="4e9fd-146">Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="4e9fd-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="4e9fd-147">Sie müssen den Medientyp überprüfen, um das Format der Daten zu verstehen, die Sie vom Quell Leser erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="4e9fd-148">Anfänglich hat jeder Stream ein Standardformat, das Sie durch Aufrufen der [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) -Methode finden können:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="4e9fd-149">Für jeden Stream bietet die Medienquelle eine Liste möglicher Medientypen für diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="4e9fd-150">Die Anzahl der Typen hängt von der Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-150">The number of types depends on the source.</span></span> <span data-ttu-id="4e9fd-151">Wenn die Quelle eine Mediendatei darstellt, ist in der Regel nur ein Typ pro Stream vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="4e9fd-152">Auf der anderen Seite kann eine Webcam möglicherweise Videos in verschiedenen Formaten streamen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="4e9fd-153">In diesem Fall kann die Anwendung das zu verwendende Format aus der Liste der Medientypen auswählen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="4e9fd-154">Um einen der Medientypen für einen Stream abzurufen, müssen Sie die [**imfsourcereader:: getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="4e9fd-155">Diese Methode nimmt zwei Index Parameter an: den Index des Streams und einen Index in die Liste der Medientypen für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="4e9fd-156">Um alle Typen für einen Stream aufzulisten, erhöhen Sie den Listen Index, während Sie die Datenstrom-Index Konstante beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="4e9fd-157">Wenn der Listen Index außerhalb des gültigen Bereichs liegt, gibt **getnativemediatype** den **\_ Typ MF E \_ nicht \_ mehr \_** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


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



<span data-ttu-id="4e9fd-158">Um die Medientypen für jeden Stream aufzulisten, erhöhen Sie den streamindex.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="4e9fd-159">Wenn der Stream-Index außerhalb des gültigen Bereichs liegt, gibt [**getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) den Wert " **MF \_ E \_ invalidstreamnumber**" zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


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



## <a name="setting-output-formats"></a><span data-ttu-id="4e9fd-160">Festlegen von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-160">Setting Output Formats</span></span>

<span data-ttu-id="4e9fd-161">Um das Ausgabeformat zu ändern, müssen Sie die [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="4e9fd-162">Diese Methode nimmt den streamindex und einen Medientyp an:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="4e9fd-163">Der Medientyp hängt davon ab, ob ein Decoder eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="4e9fd-164">Um Daten direkt aus der Quelle zu erhalten, ohne Sie zu decodieren, verwenden Sie einen der Typen, die von [**getnativemediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="4e9fd-165">Um den Stream zu decodieren, erstellen Sie einen neuen Medientyp, der das gewünschte unkomprimierte Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="4e9fd-166">Erstellen Sie im Fall des Decoders den Medientyp wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="4e9fd-167">Rufen Sie [**mfkreatemediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) auf, um einen neuen Medientyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="4e9fd-168">Legen Sie das Attribut " [**MF- \_ \_ \_ Haupttyp**](mf-mt-major-type-attribute.md) " auf "Audiodatei oder Video" fest.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="4e9fd-169">Legen Sie das Attribut " [**MF \_ MT \_ Untertyp**](mf-mt-subtype-attribute.md) " fest, um den Untertyp des Decodierungs Formats anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="4e9fd-170">(Siehe [audiountertyp-GUIDs](audio-subtype-guids.md) und [Video Untertyp-GUIDs](video-subtype-guids.md).)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="4e9fd-171">[**Imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="4e9fd-172">Der Quell Leser lädt den Decoder automatisch.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="4e9fd-173">Um die vollständigen Details des decodierten Formats abzurufen, müssen Sie [**imfsourcereader:: getcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) nach dem Aufrufen von [**setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="4e9fd-174">Der folgende Code konfiguriert den Videostream für RGB-32 und den Audiostream für PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


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



## <a name="processing-media-data"></a><span data-ttu-id="4e9fd-175">Verarbeiten von Mediendaten</span><span class="sxs-lookup"><span data-stu-id="4e9fd-175">Processing Media Data</span></span>

<span data-ttu-id="4e9fd-176">Um Mediendaten aus der Quelle abzurufen, nennen Sie die [**imfsourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


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



<span data-ttu-id="4e9fd-177">Der erste Parameter ist der Index des Streams, für den Sie Daten erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="4e9fd-178">Sie können auch den **MF- \_ Quell \_ Leser beliebige Daten \_ \_ Ströme** angeben, um die nächsten verfügbaren Daten aus einem beliebigen Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="4e9fd-179">Der zweite Parameter enthält optionale Flags. eine Liste der folgenden Informationen finden Sie unter [**\_ \_ \_ Kontroll \_ Flag für das MF-Quell Lese**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) Programm.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="4e9fd-180">Der dritte Parameter empfängt den Index des Datenstroms, der die Daten tatsächlich erzeugt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="4e9fd-181">Sie benötigen diese Informationen, wenn Sie den ersten Parameter auf den **MF- \_ Quell \_ Leser \_ Any \_ Stream** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="4e9fd-182">Der vierte Parameter empfängt Statusflags und zeigt verschiedene Ereignisse an, die beim Lesen der Daten auftreten können, z. b. das Formatieren von Änderungen im Stream.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="4e9fd-183">Eine Liste der Statusflags finden Sie unter Flag für das [**MF- \_ \_ quelllesegerät \_**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="4e9fd-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="4e9fd-184">Wenn die Medienquelle Daten für den angeforderten Datenstrom liefern kann, empfängt der letzte Parameter von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle eines Medien Beispiel Objekts.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="4e9fd-185">Verwenden Sie das Medien Beispiel für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-185">Use the media sample to:</span></span>

-   <span data-ttu-id="4e9fd-186">Einen Zeiger auf die Mediendaten erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="4e9fd-187">Die Präsentationszeit und die Stichproben Dauer erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="4e9fd-188">Erhalten Sie Attribute, die das Interlacing, die Feld Dominanz und andere Aspekte des Beispiels beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="4e9fd-189">Der Inhalt der Mediendaten hängt vom Format des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="4e9fd-190">Bei einem unkomprimierten Videostream enthält jedes Medien Beispiel einen einzelnen Videoframe.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="4e9fd-191">Bei einem unkomprimierten Audiodatenstrom enthält jedes Medien Beispiel eine Sequenz von Audioframes.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="4e9fd-192">Die Methode "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " kann " **S \_ OK** " zurückgeben und aber kein Medien Beispiel im *psample* -Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="4e9fd-193">Wenn Sie z. b. das Ende der Datei erreichen, legt " **infosample** " das " **MF \_ Source \_ readerf \_ EndOfStream** "-Flag in " *dwFlags* " fest und legt *psample* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="4e9fd-194">In diesem Fall gibt die Methode "read **Sample** " den Wert " **S \_ OK** " zurück, da kein Fehler aufgetreten ist, obwohl der *psample* -Parameter auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="4e9fd-195">Überprüfen Sie daher vor der Dereferenzierung immer den Wert von *psample* .</span><span class="sxs-lookup"><span data-stu-id="4e9fd-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="4e9fd-196">Der folgende Code zeigt, wie Sie " [**infosample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " in einer Schleife aufzurufen und die von der-Methode zurückgegebenen Informationen überprüfen, bis das Ende der Mediendatei erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


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



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="4e9fd-197">Ableiten der Daten Pipeline</span><span class="sxs-lookup"><span data-stu-id="4e9fd-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="4e9fd-198">Während der Datenverarbeitung kann ein Decoder oder eine andere Transformation Eingabe Beispiele Puffern.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="4e9fd-199">In der folgenden Abbildung Ruft die Anwendung " [**lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " auf und empfängt ein Beispiel mit einer Präsentationszeit von *T1*.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="4e9fd-200">Der Decoder hält Beispiele für *T2* und *T3*.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![eine Abbildung, die die Pufferung in einem Decoder anzeigt.](images/sourcereader02.png)

<span data-ttu-id="4e9fd-202">Beim nächsten Aufrufe von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)" kann der Quell Leser *T4* an den Decoder übergeben und *T2* an die Anwendung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="4e9fd-203">Wenn Sie alle im Decoder gepufferten Beispiele decodieren möchten, ohne neue Beispiele an den Decoder zu übergeben, legen Sie das **\_ \_ \_ controlf \_** -ablaufflag des MF-Quell Readers im *dwcontrolflags* -Parameter von "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)" fest.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="4e9fd-204">Fahren Sie mit der Durchführung der Schritte in einer Schleife fort, bis in "read **Sample** " ein **null** -Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e9fd-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="4e9fd-205">Abhängig davon, wie der Decoder Beispiele puffert, kann dies sofort oder nach mehreren Aufrufen von "read **Sample**" vorkommen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="4e9fd-206">Die Datei Dauer wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-206">Getting the File Duration</span></span>

<span data-ttu-id="4e9fd-207">Um die Dauer einer Mediendatei abzurufen, nennen Sie die [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) -Methode, und fordern Sie das [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut an, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


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



<span data-ttu-id="4e9fd-208">Die hier gezeigte Funktion Ruft die Dauer in 100-Nanosekunden-Einheiten ab.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="4e9fd-209">Dividieren Sie durch 10 Millionen, um die Dauer in Sekunden zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="4e9fd-210">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="4e9fd-210">Seeking</span></span>

<span data-ttu-id="4e9fd-211">Eine Medienquelle, die Daten aus einer lokalen Datei abruft, kann in der Regel nach beliebigen Positionen in der Datei suchen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="4e9fd-212">Erfassungsgeräte wie z. b. Webcams können im Allgemeinen nicht suchen, da die Daten Live sind.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="4e9fd-213">Eine Quelle, die Daten über ein Netzwerk streamt, kann je nach netzwerkstreamingprotokoll suchen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="4e9fd-214">Um herauszufinden, ob eine Medienquelle suchen kann, wenden Sie [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) an, und fordern Sie das [MF- \_ Quell \_ Leser \_ MediaSource \_](mf-source-reader-mediasource-characteristics.md) -Attribut Attribut an, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


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



<span data-ttu-id="4e9fd-215">Diese Funktion Ruft einen Satz von funktionsflags aus der Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="4e9fd-216">Diese Flags sind in der Enumeration " [**mfmediasource- \_ Merkmale**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) " definiert.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="4e9fd-217">Zwei Flags beziehen sich auf die Suche:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="4e9fd-218">Flag</span><span class="sxs-lookup"><span data-stu-id="4e9fd-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="4e9fd-219">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e9fd-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9fd-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**mfmediasource \_ kann \_ Suchen**</span><span class="sxs-lookup"><span data-stu-id="4e9fd-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="4e9fd-221">Die Quelle kann suchen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="4e9fd-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**mfmediasource \_ hat \_ langsame \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="4e9fd-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="4e9fd-223">Die Suche kann viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="4e9fd-224">Beispielsweise muss die Quelle möglicherweise die gesamte Datei herunterladen, bevor Sie suchen kann.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="4e9fd-225">(Es gibt keine strengen Kriterien, damit eine Quelle dieses Flag zurückgibt.)</span><span class="sxs-lookup"><span data-stu-id="4e9fd-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="4e9fd-226">Die folgenden Code Tests für das **mfmediasource-Flag können das Flag \_ \_ Suchen** .</span><span class="sxs-lookup"><span data-stu-id="4e9fd-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


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



<span data-ttu-id="4e9fd-227">Um zu suchen, nennen Sie die [**imfsourcereader:: setcurrentposition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) -Methode, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


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



<span data-ttu-id="4e9fd-228">Der erste Parameter gibt das Zeitformat an, das Sie verwenden, um die Suchposition anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="4e9fd-229">Alle Medienquellen in Media Foundation müssen 100-Nanosecond-Einheiten unterstützen, die durch den Wert **GUID \_ null** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="4e9fd-230">Der zweite Parameter ist ein **PROPVARIANT** -Wert, der die Suchposition enthält.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="4e9fd-231">Bei 100-Nanosecond-Zeiteinheiten ist der Datentyp **Longlong**.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="4e9fd-232">Beachten Sie, dass nicht jede Medienquelle eine Frame genaue Suche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="4e9fd-233">Die Genauigkeit der Suche hängt von mehreren Faktoren ab, z. b. dem Keyframe-Intervall, von der Angabe, ob die Mediendatei einen Index enthält, und davon, ob die Daten eine Konstante oder eine Variable Bitrate enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="4e9fd-234">Daher gibt es keine Garantie, dass der Zeitstempel im nächsten Beispiel genau mit der angeforderten Position übereinstimmt, nachdem Sie eine Position in einer Datei gesucht haben.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="4e9fd-235">Im Allgemeinen ist die tatsächliche Position nicht später als die angeforderte Position, sodass Sie die Beispiele verwerfen können, bis Sie den gewünschten Punkt im Stream erreichen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="4e9fd-236">Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="4e9fd-236">Playback Rate</span></span>

<span data-ttu-id="4e9fd-237">Obwohl Sie die Wiedergabe Rate mithilfe des Quell Readers festlegen können, ist dies aus den folgenden Gründen in der Regel nicht sehr nützlich:</span><span class="sxs-lookup"><span data-stu-id="4e9fd-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="4e9fd-238">Der Quell Reader unterstützt die umgekehrte Wiedergabe auch dann nicht, wenn die Medienquelle dies tut.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="4e9fd-239">Die Anwendung steuert die Präsentations Zeiten, sodass die Anwendung schnelles oder langsames spielen implementieren kann, ohne die Rate der Quelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="4e9fd-240">Einige Medienquellen unterstützen den Modus " *dünn* ", bei dem die Quelle weniger Stichproben liefert – in der Regel nur die Keyframes.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="4e9fd-241">Wenn Sie jedoch nicht Keyframes löschen möchten, können Sie die einzelnen Beispiele für das [ \_ Cleanpoint-Attribut "mfsampleextension](mfsampleextension-cleanpoint-attribute.md) " überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="4e9fd-242">Um die Wiedergabe Rate mithilfe des Quell Readers festzulegen, müssen Sie die [**imfsourcereader:: getserviceforstream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) -Methode aufrufen, um die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -und [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstellen aus der Medienquelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="4e9fd-243">Hardwarebeschleunigung</span><span class="sxs-lookup"><span data-stu-id="4e9fd-243">Hardware Acceleration</span></span>

<span data-ttu-id="4e9fd-244">Der Quell Leser ist mit Microsoft DirectX Video Acceleration (DXVA) 2,0 für Hardware beschleunigter Video-Decodierung kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="4e9fd-245">Um DXVA mit dem Quell Leser zu verwenden, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="4e9fd-246">Erstellen Sie ein Microsoft Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="4e9fd-247">Rufen Sie die [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) -Funktion zum Erstellen des Direct3D-Geräte-Managers auf.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="4e9fd-248">Diese Funktion erhält einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="4e9fd-249">Aufrufen der [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) -Methode mit einem Zeiger auf das Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="4e9fd-250">Erstellen Sie einen Attribut Speicher, indem Sie die [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="4e9fd-251">Erstellen Sie den Quell Reader.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-251">Create the Source Reader.</span></span> <span data-ttu-id="4e9fd-252">Übergeben Sie den Attribut Speicher im *pattributes* -Parameter der Erstellungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="4e9fd-253">Wenn Sie ein Direct3D-Gerät bereitstellen, ordnet der Quell Leser Videobeispiele zu, die mit der DXVA-Videoprozessor-API kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="4e9fd-254">Sie können die DXVA-Videoverarbeitung verwenden, um Hardware Deinterlacing oder Video Mischung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="4e9fd-255">Weitere Informationen finden Sie unter [DXVA Video Processing](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="4e9fd-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="4e9fd-256">Wenn der Decoder außerdem DXVA 2,0 unterstützt, wird das Direct3D-Gerät verwendet, um eine hardwarebeschleunigte Decodierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e9fd-257">Ab Windows 8 kann [**imsdxgidevicemanager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) anstelle von [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="4e9fd-258">Für Windows Store-Apps müssen Sie **IMF dxgidevicemanager** verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="4e9fd-259">Weitere Informationen finden Sie in den [Video-APIs Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="4e9fd-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4e9fd-260">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e9fd-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e9fd-261">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="4e9fd-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 





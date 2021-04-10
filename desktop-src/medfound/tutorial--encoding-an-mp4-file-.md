---
description: In diesem Tutorial wird gezeigt, wie Sie die transcode-API verwenden, um eine MP4-Datei mit H. 264 für den Videostream und AAC für den Audiostream zu codieren.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: Codieren einer MP4-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215409"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="3cbbc-103">Tutorial: Codieren einer MP4-Datei</span><span class="sxs-lookup"><span data-stu-id="3cbbc-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="3cbbc-104">In diesem Tutorial wird gezeigt, wie Sie die [transcode-API](transcode-api.md) verwenden, um eine MP4-Datei mit H. 264 für den Videostream und AAC für den Audiostream zu codieren.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="3cbbc-105">Header und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="3cbbc-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="3cbbc-106">Definieren der Codierungs profile</span><span class="sxs-lookup"><span data-stu-id="3cbbc-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="3cbbc-107">Schreiben der wmain-Funktion</span><span class="sxs-lookup"><span data-stu-id="3cbbc-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="3cbbc-108">Codieren der Datei</span><span class="sxs-lookup"><span data-stu-id="3cbbc-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="3cbbc-109">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="3cbbc-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="3cbbc-110">Quell Dauer erhalten</span><span class="sxs-lookup"><span data-stu-id="3cbbc-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="3cbbc-111">Erstellen des transcode-Profils</span><span class="sxs-lookup"><span data-stu-id="3cbbc-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="3cbbc-112">Ausführen der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="3cbbc-113">Hilfsprogramm für Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="3cbbc-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cbbc-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="3cbbc-115">Header und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="3cbbc-115">Headers and Library Files</span></span>

<span data-ttu-id="3cbbc-116">Fügen Sie die folgenden Header Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="3cbbc-117">Verknüpfen Sie die folgenden Bibliotheksdateien.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="3cbbc-118">Definieren der Codierungs profile</span><span class="sxs-lookup"><span data-stu-id="3cbbc-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="3cbbc-119">Ein Codierungs Ansatz besteht darin, eine Liste von Ziel Codierungs Profilen zu definieren, die im Voraus bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="3cbbc-120">Für dieses Tutorial verwenden wir einen relativ einfachen Ansatz und speichern eine Liste von Codierungs Formaten für H. 264-Video und AAC-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="3cbbc-121">Bei h. 264 sind die wichtigsten Format Attribute das H. 264-Profil, die Framerate, die Frame Größe und die codierte Bitrate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="3cbbc-122">Das folgende Array enthält eine Liste mit H. 264-Codierungs Formaten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-122">The following array contains a list of H.264 encoding formats.</span></span>


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



<span data-ttu-id="3cbbc-123">H. 264-Profile werden mithilfe der [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) -Enumeration angegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="3cbbc-124">Sie können auch die H. 264-Ebene angeben, aber der Microsoft Media Foundation [**h. 264-Video Encoder**](h-264-video-encoder.md) kann die richtige Ebene für einen bestimmten Videostream ableiten. Daher wird empfohlen, die ausgewählte Ebene des Encoders nicht zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="3cbbc-125">Beim Zeilen Sprung Inhalt würden Sie auch den damit-Modus angeben (siehe [Video-Interlacing](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="3cbbc-126">Bei AAC-Audiodaten sind die wichtigsten Format Attribute die audiobeispielrate, die Anzahl der Kanäle, die Anzahl der Bits pro Sample und die codierte Bitrate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="3cbbc-127">Optional können Sie die Anzeige der AAC-audioprofilebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="3cbbc-128">Weitere Informationen finden Sie unter [**AAC-Encoder**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="3cbbc-129">Das folgende Array enthält eine Liste mit AAC-Codierungs Formaten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-129">The following array contains a list of AAC encoding formats.</span></span>


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> <span data-ttu-id="3cbbc-130">Die `H264ProfileInfo` hier definierten-und- `AACProfileInfo` Strukturen sind nicht Teil der Media Foundation-API.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="3cbbc-131">Schreiben der wmain-Funktion</span><span class="sxs-lookup"><span data-stu-id="3cbbc-131">Write the wmain Function</span></span>

<span data-ttu-id="3cbbc-132">Der folgende Code zeigt den Einstiegspunkt für die Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-132">The following code shows the entry point for the console application.</span></span>


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



<span data-ttu-id="3cbbc-133">Die `wmain` Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="3cbbc-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="3cbbc-134">Ruft die [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion auf, um die com-Bibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="3cbbc-135">Ruft die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion auf, um Media Foundation zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="3cbbc-136">Ruft die Anwendungs definierte `EncodeFile` Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="3cbbc-137">Diese Funktion versieht die Eingabedatei in die Ausgabedatei und wird im nächsten Abschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="3cbbc-138">Ruft die [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) -Funktion auf, um Media Foundation herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="3cbbc-139">Um die Initialisierung der com-Bibliothek aufzurufen, können Sie die Funktion " [**count Initialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) "</span><span class="sxs-lookup"><span data-stu-id="3cbbc-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="3cbbc-140">Codieren der Datei</span><span class="sxs-lookup"><span data-stu-id="3cbbc-140">Encode the File</span></span>

<span data-ttu-id="3cbbc-141">Der folgende Code zeigt die- `EncodeFile` Funktion, die die Transcodierung ausführt.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="3cbbc-142">Diese Funktion besteht größtenteils aus Aufrufen von anderen Anwendungs definierten Funktionen, die weiter unten in diesem Thema angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="3cbbc-143">Die- `EncodeFile` Funktion führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="3cbbc-144">Erstellt eine Medienquelle für die Eingabedatei, wobei die URL oder der Dateipfad der Eingabedatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="3cbbc-145">(Informationen hierzu finden Sie [unter Erstellen der Medienquelle](#create-the-media-source).)</span><span class="sxs-lookup"><span data-stu-id="3cbbc-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="3cbbc-146">Ruft die Dauer der Eingabedatei ab.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-146">Gets the duration of the input file.</span></span> <span data-ttu-id="3cbbc-147">(Weitere Informationen finden [Sie unter Ermitteln der Quell Dauer](#get-the-source-duration).)</span><span class="sxs-lookup"><span data-stu-id="3cbbc-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="3cbbc-148">Erstellen Sie das transcodieren-Profil.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-148">Create the transcode profile.</span></span> <span data-ttu-id="3cbbc-149">(Weitere Informationen finden Sie [unter Erstellen des transcode-Profils](#create-the-transcode-profile).)</span><span class="sxs-lookup"><span data-stu-id="3cbbc-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="3cbbc-150">Rufen Sie [**mfkreatetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) auf, um die partielle transcodetopologie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="3cbbc-151">Erstellen Sie ein Hilfsobjekt, das die Medien Sitzung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="3cbbc-152">(Weitere Informationen finden Sie unter Media Session Helper).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="3cbbc-153">Führen Sie die Codierungs Sitzung aus, und warten Sie, bis Sie beendet ist</span><span class="sxs-lookup"><span data-stu-id="3cbbc-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="3cbbc-154">(Siehe [Ausführen der Codierungs Sitzung](#run-the-encoding-session).)</span><span class="sxs-lookup"><span data-stu-id="3cbbc-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="3cbbc-155">Wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Medienquelle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="3cbbc-156">Releaseschnittstellenzeiger.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-156">Release interface pointers.</span></span> <span data-ttu-id="3cbbc-157">Dieser Code verwendet die [saferelease](saferelease.md) -Funktion zum Freigeben von Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="3cbbc-158">Eine andere Möglichkeit ist die Verwendung einer intelligenten com-Zeiger Klasse, z. b. **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="3cbbc-159">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="3cbbc-159">Create the Media Source</span></span>

<span data-ttu-id="3cbbc-160">Die Medienquelle ist das Objekt, das die Eingabedatei liest und analysiert.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="3cbbc-161">Um die Medienquelle zu erstellen, übergeben Sie die URL der Eingabedatei an den [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="3cbbc-162">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-162">The following code shows how to do this.</span></span>


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="3cbbc-163">Weitere Informationen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="3cbbc-164">Quell Dauer erhalten</span><span class="sxs-lookup"><span data-stu-id="3cbbc-164">Get the Source Duration</span></span>

<span data-ttu-id="3cbbc-165">Obwohl es nicht erforderlich ist, ist es hilfreich, die Medienquelle für die Dauer der Eingabedatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="3cbbc-166">Dieser Wert kann zum Nachverfolgen des Codierungs Fortschritts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="3cbbc-167">Die Dauer wird im [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut des Präsentations Deskriptors gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="3cbbc-168">Rufen Sie den Präsentations Deskriptor ab, indem Sie [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a><span data-ttu-id="3cbbc-169">Erstellen des transcode-Profils</span><span class="sxs-lookup"><span data-stu-id="3cbbc-169">Create the Transcode Profile</span></span>

<span data-ttu-id="3cbbc-170">Im transcodieren-Profil werden die Codierungs Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="3cbbc-171">Weitere Informationen zum Erstellen eines transcodieren-Profils finden [Sie unter Verwenden der transcodieren-API](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="3cbbc-172">Führen Sie die folgenden Schritte aus, um das Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="3cbbc-173">Rufen Sie [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf, um das leere Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="3cbbc-174">Erstellen Sie einen Medientyp für den AAC-Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="3cbbc-175">Fügen Sie Sie dem Profil hinzu, indem Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="3cbbc-176">Erstellen Sie einen Medientyp für den H. 264-Videostream.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="3cbbc-177">Fügen Sie Sie dem Profil hinzu, indem Sie [**imftranscodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="3cbbc-178">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher für die Attribute auf Container Ebene zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="3cbbc-179">Legen Sie das Attribut " [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="3cbbc-180">Dies ist das einzige erforderliche Attribut auf Container Ebene.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="3cbbc-181">Legen Sie für die Ausgabe von MP4-Dateien dieses Attribut auf **mftranscodecontainertype \_ MPEG4** fest.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="3cbbc-182">Wenn Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) aufrufen, legen Sie die Attribute auf Container Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="3cbbc-183">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-183">The following code shows these steps.</span></span>


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



<span data-ttu-id="3cbbc-184">Um die Attribute für den H. 264-Videostream anzugeben, erstellen Sie einen Attribut Speicher und legen die folgenden Attribute fest:</span><span class="sxs-lookup"><span data-stu-id="3cbbc-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="3cbbc-185">Attribut</span><span class="sxs-lookup"><span data-stu-id="3cbbc-185">Attribute</span></span>                                                       | <span data-ttu-id="3cbbc-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="3cbbc-187">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="3cbbc-188">Legen Sie auf **mfvideoformat \_ H264** fest.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="3cbbc-189">**MF- \_ MT- \_ MPEG2- \_ Profil**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="3cbbc-190">H. 264-Profil.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="3cbbc-191">**MF- \_ MT- \_ Frame \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="3cbbc-192">Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-192">Frame size.</span></span>                     |
| [<span data-ttu-id="3cbbc-193">**MF- \_ MT- \_ Frame \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="3cbbc-194">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="3cbbc-195">**MF-mittlere mittlere \_ \_ \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="3cbbc-196">Codierte Bitrate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="3cbbc-197">Um die Attribute für den AAC-Audiostream anzugeben, erstellen Sie einen Attribut Speicher und legen die folgenden Attribute fest:</span><span class="sxs-lookup"><span data-stu-id="3cbbc-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="3cbbc-198">Attribut</span><span class="sxs-lookup"><span data-stu-id="3cbbc-198">Attribute</span></span>                                                                                      | <span data-ttu-id="3cbbc-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="3cbbc-200">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="3cbbc-201">Auf **mfaudioformat- \_ AAC** festlegen</span><span class="sxs-lookup"><span data-stu-id="3cbbc-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="3cbbc-202">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="3cbbc-203">Audiobeispielrate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="3cbbc-204">**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="3cbbc-205">Bits pro Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="3cbbc-206">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="3cbbc-207">Anzahl der Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="3cbbc-208">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="3cbbc-209">Codierte Bitrate.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="3cbbc-210">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="3cbbc-211">Auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="3cbbc-212">Anzeige der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene \_</span><span class="sxs-lookup"><span data-stu-id="3cbbc-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="3cbbc-213">Anzeige der AAC-Profil Ebene (optional).</span><span class="sxs-lookup"><span data-stu-id="3cbbc-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="3cbbc-214">Mit dem folgenden Code werden die Videodaten Strom Attribute erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-214">The following code creates the video stream attributes.</span></span>


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="3cbbc-215">Mit dem folgenden Code werden die audiostreamattribute erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-215">The following code creates the audio stream attributes.</span></span>


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="3cbbc-216">Beachten Sie, dass die transcodieren-API keinen echten Medientyp erfordert, obwohl Sie Medientyp Attribute verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="3cbbc-217">Insbesondere das [**MF MT- \_ \_ \_ Haupttyp**](mf-mt-major-type-attribute.md) Attribut ist nicht erforderlich, da die [**setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) -Methode und die [**setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) -Methode den Haupttyp implizieren.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="3cbbc-218">Es ist jedoch auch gültig, einen tatsächlichen Medientyp an diese Methoden zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="3cbbc-219">(Die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle erbt [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span><span class="sxs-lookup"><span data-stu-id="3cbbc-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="3cbbc-220">Ausführen der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-220">Run the Encoding Session</span></span>

<span data-ttu-id="3cbbc-221">Der folgende Code führt die Codierungs Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-221">The following code runs the encoding session.</span></span> <span data-ttu-id="3cbbc-222">Dabei wird die Hilfsprogrammklasse für Medien Sitzungen verwendet, die im nächsten Abschnitt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a><span data-ttu-id="3cbbc-223">Hilfsprogramm für Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-223">Media Session Helper</span></span>

<span data-ttu-id="3cbbc-224">Die [Medien Sitzung](media-session.md) wird vollständig im Abschnitt [Media Foundation-Architektur](media-foundation-architecture.md) dieser Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="3cbbc-225">Die Medien Sitzung verwendet ein asynchrones Ereignis Modell.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="3cbbc-226">In einer GUI-Anwendung sollten Sie auf Sitzungs Ereignisse reagieren, ohne den UI-Thread zu blockieren, um auf das nächste Ereignis zu warten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="3cbbc-227">Im Tutorial zum Wiedergeben [ungeschützter Mediendateien](how-to-play-unprotected-media-files.md) wird gezeigt, wie dies in einer Wiedergabe Anwendung durchzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="3cbbc-228">Bei der Codierung ist das Prinzip identisch, aber es sind weniger Ereignisse relevant:</span><span class="sxs-lookup"><span data-stu-id="3cbbc-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="3cbbc-229">Ereignis</span><span class="sxs-lookup"><span data-stu-id="3cbbc-229">Event</span></span>                                  | <span data-ttu-id="3cbbc-230">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cbbc-231">Mesessionend</span><span class="sxs-lookup"><span data-stu-id="3cbbc-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="3cbbc-232">Wird ausgelöst, wenn die Codierung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="3cbbc-233">Mesessionclosed</span><span class="sxs-lookup"><span data-stu-id="3cbbc-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="3cbbc-234">Wird ausgelöst, wenn die [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) -Methode abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="3cbbc-235">Nachdem dieses Ereignis ausgelöst wurde, kann die Medien Sitzung sicher heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="3cbbc-236">Bei einer Konsolenanwendung ist es sinnvoll, Ereignisse zu blockieren und auf Ereignisse zu warten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="3cbbc-237">Abhängig von der Quelldatei und den Codierungs Einstellungen kann es eine Weile dauern, bis die Codierung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="3cbbc-238">Statusaktualisierungen können wie folgt angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="3cbbc-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="3cbbc-239">Aufrufen von [**imfmediasession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) zum Abrufen der Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="3cbbc-240">Fragen Sie die Uhr nach der [**IMF presentationclock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="3cbbc-241">[**Imfpresentationclock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) aufrufen, um die aktuelle Position zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="3cbbc-242">Die Position wird in Zeiteinheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-242">The position is given in units of time.</span></span> <span data-ttu-id="3cbbc-243">Verwenden Sie den Wert, um den Prozentsatz der abgeschlossenen Werte zu erhalten `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="3cbbc-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="3cbbc-244">Hier ist die Deklaration der- `CSession` Klasse.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-244">Here is the declaration of the `CSession` class.</span></span>


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



<span data-ttu-id="3cbbc-245">Der folgende Code zeigt die komplette Implementierung der- `CSession` Klasse.</span><span class="sxs-lookup"><span data-stu-id="3cbbc-245">The following code shows the complete implementation of the `CSession` class.</span></span>


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3cbbc-246">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cbbc-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbbc-247">**AAC-Encoder**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="3cbbc-248">**H. 264-Video Encoder**</span><span class="sxs-lookup"><span data-stu-id="3cbbc-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="3cbbc-249">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3cbbc-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="3cbbc-250">Medientypen</span><span class="sxs-lookup"><span data-stu-id="3cbbc-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="3cbbc-251">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="3cbbc-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 

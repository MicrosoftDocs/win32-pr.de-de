---
title: Das Format der Datei wird ermittelt.
description: Das Format der Datei wird ermittelt.
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media Device Manager, Dateiformate
- Device Manager, Dateiformate
- Programmier Handbuch, Dateiformate
- Desktop Anwendungen, Dateiformate
- Erstellen von Windows Media Device Manager-Anwendungen, Dateiformaten
- Schreiben von Dateien auf Geräte, Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709702"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="cc9b4-109">Das Format der Datei wird ermittelt.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-109">Discovering a File's Format</span></span>

<span data-ttu-id="cc9b4-110">Vor dem Senden einer Datei an das Gerät muss eine Anwendung bestimmen, ob das Gerät dieses Dateiformat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="cc9b4-111">Es kann komplex sein, das Format einer Datei zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="cc9b4-112">Die einfachste Möglichkeit besteht darin, eine Liste von Dateierweiterungen zu erstellen, die bestimmten WMDM \_ Formatcode-Enumerationswerten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="cc9b4-113">Bei diesem System gibt es jedoch einige Probleme: ein einzelnes Format kann mehrere Erweiterungen aufweisen (z. b. jpg, jpe und JPEG für JPEG-Bilder).</span><span class="sxs-lookup"><span data-stu-id="cc9b4-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="cc9b4-114">Außerdem kann die gleiche Dateierweiterung von verschiedenen Programmen für unterschiedliche Formate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="cc9b4-115">Um die Einschränkungen einer strikten Zuordnung zu überwinden, empfiehlt es sich, eine Anwendung zu überprüfen, ob das Format mit der Erweiterung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="cc9b4-116">Das DirectShow SDK stellt Tools bereit, die es einer Anwendung ermöglichen, eine begrenzte Anzahl von Details zu den meisten Medien Dateitypen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="cc9b4-117">Das SDK für den Windows Media-Format macht eine große Anzahl von Details verfügbar, aber nur Informationen zu den ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="cc9b4-118">Da für alle Dateitypen der Format Code nach Möglichkeit überprüft werden sollte, ist es daher am besten, DirectShow zu verwenden, um den grundlegenden Formatierungs Code zu ermitteln oder zu überprüfen. Außerdem können Sie mit dem Windows Media-Format SDK alle zusätzlichen Metadaten ermitteln, die für ASF-Dateien erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="cc9b4-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="cc9b4-119">DirectShow kann auch verwendet werden, um grundlegende Metadaten für nicht--ASF-Dateien zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="cc9b4-120">Im folgenden finden Sie eine Möglichkeit, ein Dateiformat mithilfe der Erweiterungs Zuordnung und DirectShow zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="cc9b4-121">Vergleichen Sie zunächst die Dateinamenerweiterung mit einer Liste bekannter Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="cc9b4-122">Achten Sie darauf, dass die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="cc9b4-123">Wenn die Erweiterung nicht zugeordnet ist, legen Sie das Format auf WMDM- \_ Formatcode nicht \_ definiert fest.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="cc9b4-124">Wenn der Format Code nicht gefunden wurde (oder Sie überprüfen möchten, ob es sich bei einer Datei um eine Mediendatei handelt), können Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc9b4-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="cc9b4-125">Erstellen Sie mithilfe von **cokreateinstance**(CLSID mediadet) ein DirectShow-Medien Erkennungs Objekt \_ , und rufen Sie die **imediadet** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="cc9b4-126">Öffnen Sie die Datei durch Aufrufen von **imediadet::p UT \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="cc9b4-127">Bei diesem Befehl tritt ein Fehler auf, wenn die Datei geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="cc9b4-128">Rufen Sie den Medientyp des Standardstreams ab, indem Sie **imediadet:: get \_ streammediatype** aufrufen, der einen **am- \_ \_ Medientyp** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="cc9b4-129">Rufen Sie die Anzahl der Streams durch Aufrufen von **imediadet:: get \_ outputstreams** ab.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="cc9b4-130">Wenn nur ein Stream und Audiodaten vorhanden sind, lautet der Dateityp WMDM \_ Formatcode \_ undefinedaudio.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="cc9b4-131">Wenn nur ein Stream und ein Video vorhanden sind, lautet der Dateityp WMDM \_ Formatcode \_ undefinedvideo.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="cc9b4-132">Wenn nur ein Stream vorhanden ist und ein Video und die Bitrate NULL ist, lautet der Dateityp WMDM \_ Formatcode \_ windowsimageformat.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="cc9b4-133">Außerdem können Sie versuchen, Audiodateien oder Video Codecs aus den aus **get \_ streammediatype** abgerufenen **videoinfoheader** -oder **WaveFormatEx** -Membern zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="cc9b4-134">Die folgende C++-Funktion veranschaulicht den Datei Erweiterungs Abgleich und die Verwendung von DirectShow, um unbekannte Dateien zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="cc9b4-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a><span data-ttu-id="cc9b4-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc9b4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc9b4-136">**Schreiben von Dateien auf das Gerät**</span><span class="sxs-lookup"><span data-stu-id="cc9b4-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 





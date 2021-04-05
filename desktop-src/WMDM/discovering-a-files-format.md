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
# <a name="discovering-a-files-format"></a>Das Format der Datei wird ermittelt.

Vor dem Senden einer Datei an das Gerät muss eine Anwendung bestimmen, ob das Gerät dieses Dateiformat unterstützt.

Es kann komplex sein, das Format einer Datei zu ermitteln. Die einfachste Möglichkeit besteht darin, eine Liste von Dateierweiterungen zu erstellen, die bestimmten WMDM \_ Formatcode-Enumerationswerten zugeordnet sind. Bei diesem System gibt es jedoch einige Probleme: ein einzelnes Format kann mehrere Erweiterungen aufweisen (z. b. jpg, jpe und JPEG für JPEG-Bilder). Außerdem kann die gleiche Dateierweiterung von verschiedenen Programmen für unterschiedliche Formate verwendet werden.

Um die Einschränkungen einer strikten Zuordnung zu überwinden, empfiehlt es sich, eine Anwendung zu überprüfen, ob das Format mit der Erweiterung übereinstimmt. Das DirectShow SDK stellt Tools bereit, die es einer Anwendung ermöglichen, eine begrenzte Anzahl von Details zu den meisten Medien Dateitypen zu ermitteln. Das SDK für den Windows Media-Format macht eine große Anzahl von Details verfügbar, aber nur Informationen zu den ASF-Dateien. Da für alle Dateitypen der Format Code nach Möglichkeit überprüft werden sollte, ist es daher am besten, DirectShow zu verwenden, um den grundlegenden Formatierungs Code zu ermitteln oder zu überprüfen. Außerdem können Sie mit dem Windows Media-Format SDK alle zusätzlichen Metadaten ermitteln, die für ASF-Dateien erforderlich sind DirectShow kann auch verwendet werden, um grundlegende Metadaten für nicht--ASF-Dateien zu ermitteln.

Im folgenden finden Sie eine Möglichkeit, ein Dateiformat mithilfe der Erweiterungs Zuordnung und DirectShow zu ermitteln.

Vergleichen Sie zunächst die Dateinamenerweiterung mit einer Liste bekannter Erweiterungen. Achten Sie darauf, dass die Groß-/Kleinschreibung nicht beachtet wird. Wenn die Erweiterung nicht zugeordnet ist, legen Sie das Format auf WMDM- \_ Formatcode nicht \_ definiert fest.

-   Wenn der Format Code nicht gefunden wurde (oder Sie überprüfen möchten, ob es sich bei einer Datei um eine Mediendatei handelt), können Sie die folgenden Schritte ausführen:
    1.  Erstellen Sie mithilfe von **cokreateinstance**(CLSID mediadet) ein DirectShow-Medien Erkennungs Objekt \_ , und rufen Sie die **imediadet** -Schnittstelle ab.
    2.  Öffnen Sie die Datei durch Aufrufen von **imediadet::p UT \_ filename**. Bei diesem Befehl tritt ein Fehler auf, wenn die Datei geschützt ist.
    3.  Rufen Sie den Medientyp des Standardstreams ab, indem Sie **imediadet:: get \_ streammediatype** aufrufen, der einen **am- \_ \_ Medientyp** zurückgibt.
    4.  Rufen Sie die Anzahl der Streams durch Aufrufen von **imediadet:: get \_ outputstreams** ab.
        -   Wenn nur ein Stream und Audiodaten vorhanden sind, lautet der Dateityp WMDM \_ Formatcode \_ undefinedaudio.
        -   Wenn nur ein Stream und ein Video vorhanden sind, lautet der Dateityp WMDM \_ Formatcode \_ undefinedvideo.
        -   Wenn nur ein Stream vorhanden ist und ein Video und die Bitrate NULL ist, lautet der Dateityp WMDM \_ Formatcode \_ windowsimageformat.

Außerdem können Sie versuchen, Audiodateien oder Video Codecs aus den aus **get \_ streammediatype** abgerufenen **videoinfoheader** -oder **WaveFormatEx** -Membern zu vergleichen.

Die folgende C++-Funktion veranschaulicht den Datei Erweiterungs Abgleich und die Verwendung von DirectShow, um unbekannte Dateien zu analysieren.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 





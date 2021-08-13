---
title: Ermitteln des Formats einer Datei
description: Ermitteln des Formats einer Datei
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Medien Geräte-Manager, Dateiformate
- Geräte-Manager, Dateiformate
- Programmierhandbuch, Dateiformate
- Desktopanwendungen, Dateiformate
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Dateiformaten
- Schreiben von Dateien auf Geräte, Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585329"
---
# <a name="discovering-a-files-format"></a>Ermitteln des Formats einer Datei

Vor dem Senden einer Datei an das Gerät sollte eine Anwendung bestimmen, ob das Gerät dieses Dateiformat unterstützt.

Das Ermitteln des Formats einer Datei kann komplex sein. Die einfachste Möglichkeit besteht darin, eine Liste von Dateierweiterungen zu erstellen, die bestimmten WMDM \_ FORMATCODE-Enumerationswerten zugeordnet sind. Es gibt jedoch einige Probleme mit diesem System: Ein einzelnes Format kann mehrere Erweiterungen aufweisen (z. B. .jpg, JPE und JPEG für JPEG-Bilder). Außerdem kann dieselbe Dateierweiterung von verschiedenen Programmen für verschiedene Formate verwendet werden.

Um die Einschränkungen einer strengen Zuordnung zu umgehen, empfiehlt es sich, dass eine Anwendung überprüft, ob das Format der Erweiterung entspricht. Das DirectShow SDK bietet Tools, mit denen eine Anwendung einen begrenzten Satz von Details zu den meisten Mediendateitypen ermitteln kann. Das Windows Media Format SDK macht eine große Anzahl von Details verfügbar, jedoch nur zu ASF-Dateien. Da bei allen Dateitypen nach Möglichkeit ihr Formatcode überprüft werden sollte, sollten Sie directShow verwenden, um den grundlegenden Formatcode zu ermitteln oder zu überprüfen, und das Windows Media Format SDK verwenden, um alle zusätzlichen Metadaten zu ermitteln, die für ASF-Dateien gewünscht sind. DirectShow kann auch verwendet werden, um grundlegende Metadaten für Nicht-ASF-Dateien zu ermitteln.

Im Folgenden finden Sie eine Möglichkeit, ein Dateiformat mithilfe von Erweiterungszuordnung und DirectShow zu ermitteln.

Vergleichen Sie zunächst die Dateinamenerweiterung mit einer Liste bekannter Erweiterungen. Achten Sie darauf, dass die Groß-/Kleinschreibung des Vergleichs nicht beachtet wird. Wenn die Erweiterung nicht zugeordnet ist, legen Sie das Format auf WMDM \_ FORMATCODE \_ UNDEFINED fest.

-   Wenn der Formatcode nicht gefunden wurde (oder Sie überprüfen möchten, ob es sich bei einer Datei um eine Mediendatei handelt), können Sie die folgenden Schritte ausführen:
    1.  Erstellen Sie ein DirectShow-Medienerkennungsobjekt mithilfe von **CoCreateInstance**(CLSID \_ MediaDet), und ruft Sie die **IMediaDet-Schnittstelle** ab.
    2.  Öffnen Sie die Datei, indem Sie **IMediaDet::p ut \_ Filename** aufrufen. Dieser Aufruf schlägt fehl, wenn die Datei geschützt ist.
    3.  Rufen Sie den Medientyp des Standardstreams ab, indem **Sie IMediaDet::get \_ StreamMediaType** aufrufen, der einen **AM MEDIA \_ \_ TYPE** zurückgibt.
    4.  Rufen Sie **IMediaDet::get \_ OutputStreams** auf, um die Anzahl der Streams abzurufen.
        -   Wenn es nur einen Stream gibt und es sich um Audiodaten handelt, lautet der Dateityp WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO.
        -   Wenn nur ein Stream vorhanden ist und es sich um ein Video handelt, lautet der Dateityp WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO.
        -   Wenn es nur einen Stream gibt und es sich um video handelt und die Bitrate 0 (null) ist, lautet der Dateityp WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

Sie können auch versuchen, Audio- oder Videocodecs von den **VIDEOINFOHEADER-** oder **WAVEFORMATEX-Membern** abzugleichen, die von **get \_ StreamMediaType** abgerufen wurden.

Die folgende C++-Funktion veranschaulicht den Abgleich von Dateierweiterungen und die Verwendung von DirectShow, um zu versuchen, unbekannte Dateien zu analysieren.


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

 

 





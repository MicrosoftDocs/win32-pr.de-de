---
description: 'Schritt 3: Implementieren der Frame-Grabbing Funktion'
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: 'Schritt 3: Implementieren der Frame-Grabbing Funktion'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75410c48765e9437cd328a220ccbecf2c207bdaae5242a9e41060bc13fa02eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904094"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Schritt 3: Implementieren der Frame-Grabbing Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Dieses Thema ist Schritt 3 von [Grabbing a Poster Frame](grabbing-a-poster-frame.md).

Der nächste Schritt besteht in der Implementierung der GetBitmap-Funktion, die media detector verwendet, um einen Posterrahmen zu greifen. Führen Sie in dieser Funktion die folgenden Schritte aus:

1.  Erstellen Sie die Medienerkennung.
2.  Geben Sie eine Mediendatei an.
3.  Untersuchen Sie jeden Stream in der Datei. Wenn es sich um einen Videostream handelt, erhalten Sie die nativen Dimensionen des Videos.
4.  Beziehen Sie einen Posterrahmen, und geben Sie dabei die Suchzeit und die Zieldimension an.

Erstellen Sie das Media Detector-Objekt, indem [**Sie CoCreateInstance aufrufen:**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Geben Sie mithilfe der [**IMediaDet::p ut \_ Filename-Methode einen Dateinamen**](imediadet-put-filename.md) an. Diese Methode akzeptiert einen **BSTR-Parameter.**


```C++
hr = pDet->put_Filename(bstrFilename);
```



Sie können die Anzahl der Streams erhalten und jeden Stream durchschleifen, um den Medientyp zu überprüfen. Die [**IMediaDet::get \_ OutputStreams-Methode**](imediadet-get-outputstreams.md) ruft die Anzahl der Streams ab, und die [**IMediaDet::p ut \_ CurrentStream-Methode**](imediadet-put-currentstream.md) gibt an, welcher Stream untersucht werden soll. Beenden Sie die Schleife im ersten Videostream.


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



Wenn kein Videostream gefunden wurde, wird die Funktion beendet.

Im vorherigen Code gibt die [**IMediaDet::get \_ StreamType-Methode**](imediadet-get-streamtype.md) nur die Haupttyp-GUID zurück. Dies ist praktisch, wenn Sie den vollständigen Medientyp nicht untersuchen müssen. Um die Videodimensionen zu erhalten, ist es jedoch erforderlich, den Formatblock zu untersuchen, damit der vollständige Medientyp benötigt wird. Sie können dies abrufen, indem Sie die [**Methode IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md) aufrufen, die eine [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) auffüllt. Die Medienerkennung konvertiert alle Videostreams mit einem [**VIDEOINFOHEADER-Formatblock**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in ein unkomprimiertes Format.


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



Die [**methode \_ get StreamMediaType**](imediadet-get-streammediatype.md) ordnet den Formatblock zu, den der Aufrufer freigibt. In diesem Beispiel wird die [**FreeMediaType-Funktion**](freemediatype.md) aus der Basisklassenbibliothek verwendet.

Jetzt können Sie den Posterrahmen erhalten. Rufen Sie zuerst die [**IMediaDet::GetBitmapBits-Methode**](imediadet-getbitmapbits.md) mit einem **NULL-Zeiger** für den Puffer auf:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Dieser Aufruf gibt die erforderliche Puffergröße im *lSize-Parameter* zurück. Der erste Parameter gibt die Zu suchzeit des Streams an. In diesem Beispiel wird die Zeit 0 (null) verwendet. Für die Breite und Höhe werden in diesem Beispiel die zuvor erhaltenen nativen Videodimensionen verwendet. Wenn Sie andere Werte angeben, streckt die Medienerkennung die Bitmap, um eine Übereinstimmung zu erhalten.

Wenn die Methode erfolgreich ist, ordnen Sie den Puffer zu, und rufen [**Sie GetBitmapBits erneut**](imediadet-getbitmapbits.md) auf:


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



Hier ist die vollständige Funktion mit etwas besserer Fehlerbehandlung.


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



Weiter: [Schritt 4: Zeichnen der Bitmap im Clientbereich](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Greifen eines Posterrahmens](grabbing-a-poster-frame.md)
</dt> </dl>

 

 

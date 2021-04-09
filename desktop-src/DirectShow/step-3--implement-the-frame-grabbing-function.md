---
description: Schritt 3 Implementieren der Frame-Grabbing-Funktion
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Schritt 3 Implementieren der Frame-Grabbing-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867088"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Schritt 3: Implementieren der Frame-Grabbing-Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Dieses Thema ist Schritt 3 zum Durchlaufen [eines Poster Frame](grabbing-a-poster-frame.md).

Der nächste Schritt ist die Implementierung der getbitmap-Funktion, die mithilfe des Medien Detektors einen Poster-Frame verwendet. Führen Sie in dieser Funktion die folgenden Schritte aus:

1.  Erstellen Sie den Medien Detektor.
2.  Geben Sie eine Mediendatei an.
3.  Untersuchen Sie jeden Stream in der Datei. Wenn es sich um einen Videostream handelt, erhalten Sie die systemeigenen Dimensionen des Videos.
4.  Rufen Sie einen Poster-Frame ab, der die Suchzeit und die Ziel Dimension angibt.

Erstellen Sie das Medien Erkennungs Objekt, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen:


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Geben Sie einen Dateinamen an, und verwenden Sie dabei die [**imediadet::p UT \_ -Datei**](imediadet-put-filename.md) namens Methode. Diese Methode nimmt einen **BSTR** -Parameter an.


```C++
hr = pDet->put_Filename(bstrFilename);
```



Holen Sie sich die Anzahl der Streams, und durchlaufen Sie jeden Stream, indem Sie den Medientyp überprüfen. Die [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) -Methode ruft die Anzahl der Streams ab, und die [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md) -Methode gibt an, welcher Stream untersucht werden soll. Beenden Sie die Schleife für den ersten Videostream.


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

Im vorherigen Code gibt die [**imediadet:: get \_ Streamtype**](imediadet-get-streamtype.md) -Methode nur die GUID des Haupt Typs zurück. Dies ist praktisch, wenn Sie den gesamten Medientyp nicht überprüfen müssen. Um die Video Dimensionen zu erhalten, ist es jedoch notwendig, den Format Block zu untersuchen, sodass der vollständige Medientyp erforderlich ist. Sie können dies abrufen, indem Sie die [**imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode aufrufen, die eine [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur füllt. Der Medien Detektor konvertiert alle Videodaten Ströme mit einem [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Block in ein unkomprimiertes Format.


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



Die [**get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode ordnet den Format Block zu, der vom Aufrufer freigegeben werden muss. In diesem Beispiel wird die Funktion " [**fremediatype**](freemediatype.md) " aus der Basisklassen Bibliothek verwendet.

Nun können Sie den Poster-Frame erhalten. Aufrufen Sie zuerst die [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode mit einem **null** -Zeiger für den Puffer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Dieser Rückruf gibt die erforderliche Puffergröße im *LSIZE* -Parameter zurück. Der erste Parameter gibt die streamzeit an, nach der gesucht werden soll. in diesem Beispiel wird die Zeit NULL verwendet. Für Breite und Höhe verwendet dieses Beispiel die systemeigenen Video Dimensionen, die Sie zuvor erhalten haben. Wenn Sie andere Werte angeben, wird die Bitmap vom Medien Detektor entsprechend gestreckt.

Wenn die Methode erfolgreich ist, weisen Sie den Puffer zu, und wiederholen Sie dann [**getbitmapbits**](imediadet-getbitmapbits.md) :


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



Hier finden Sie die gesamte Funktion, mit einer etwas besseren Fehlerbehandlung.


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



Weiter: [Schritt 4: Zeichnen der Bitmap im Client Bereich](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ein Poster-Frame wird gepackt.](grabbing-a-poster-frame.md)
</dt> </dl>

 

 

---
description: Streamformat
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Streamformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ed1ac4501a2d8f081c12fef75baf15aaebd442fc182a116db1038c2a73523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903990"
---
# <a name="stream-format"></a>Streamformat

Sowohl der MSDV- als auch der UVC-Treiber können zwei DV-Formate ausgeben: überlappende Audiovideos oder nur Video. Verschachteltes Audiovideo ist das ursprüngliche Format des Geräts. Das format "Nur Video" enthält die gleichen Daten, aber die Beispiele sind so gekennzeichnet, dass sie keine Audiodaten enthalten. Das Nur-Video-Format ist hauptsächlich für die Kompatibilität mit Anwendungen verfügbar, die Video für Windows verwenden. Weitere Informationen finden Sie unter [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).

**MSDV-Treiber**

Der MSDV-Treiber verfügt über zwei Ausgabepins. Der erste Ausgabepin sendet verschachtelte Daten, und der zweite Ausgabepin sendet Nur-Video-Daten. Es kann jeweils nur ein Ausgabepin verbunden werden. Um ein Format auszuwählen, verbinden Sie den entsprechenden Ausgabepin. Sie können die [**IAMStreamConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) auf dem Ausgabepin verwenden, um das Format zu ermitteln.

**UVC-Treiber**

Im Gegensatz zum MSDV-Treiber stellt der UVC-Treiber beide Formate über denselben Pin bereit. Das Standardformat ist nur video. Um das Format auszuwählen, verwenden Sie die **IAMStreamConfig-Schnittstelle** auf dem Ausgabepin. Rufen Sie die **GetStreamCaps-Methode** auf, um die Medientypen auf dem Ausgabepin aufzuzählen. Wenn der Haupttyp für jeden Medientyp mit dem gewünschten Format übereinstimmt, rufen **Sie SetFormat auf,** und übergeben Sie diesen Medientyp.



| Format                      | Haupttyp             |
|-----------------------------|------------------------|
| Verschachtelte Audio- und Videoinhalte | MEDIATYPE \_ Interleaved |
| Nur Video                  | \_MEDIATYPE-Video       |



 

Die folgende Funktion legt das Format basierend auf der Haupttyp-GUID fest.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



Der MSDV-Treiber unterstützt auch **IAMStreamConfig,** sodass Sie Code schreiben können, der für beide Gerätetypen funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




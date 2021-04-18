---
description: Streamformat
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Streamformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350821"
---
# <a name="stream-format"></a>Streamformat

Sowohl der msdv-als auch der UVC-Treiber können zwei DV-Formate ausgeben: überlappende Audiovideo oder nur Video. Interleaved Audiovideo ist das ursprüngliche Format des Geräts. Das nur-Text-Format enthält dieselben Daten, die Beispiele sind jedoch so gekennzeichnet, dass Sie keine Audiodaten aufweisen. Das nur-Video-Format besteht hauptsächlich aus der Kompatibilität mit Anwendungen, die Video für Windows verwenden. Weitere Informationen finden Sie unter [Type-1 vs. Type-2 DV AVI files](type-1-vs--type-2-dv-avi-files.md).

**Msdv-Treiber**

Der msdv-Treiber verfügt über zwei Ausgabe Pins. Mit dem ersten Ausgabepin werden überlappende Daten gesendet, und mit dem zweiten Ausgabepin werden nur Videodaten gesendet. Es kann jeweils nur eine Ausgabe-PIN verbunden werden. Um ein Format auszuwählen, verbinden Sie die entsprechende Ausgabe-PIN. Sie können die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle in der Ausgabe-PIN verwenden, um das Format zu suchen.

**UVC-Treiber**

Im Gegensatz zum msdv-Treiber liefert der UVC-Treiber beide Formate von derselben PIN. Das Standardformat ist nur Video. Um das Format auszuwählen, verwenden Sie die **iamstreamconfig** -Schnittstelle in der Ausgabe-PIN. Ruft die **getstreamcaps** -Methode auf, um die Medientypen in der Ausgabe-PIN aufzuzählen. Wenn der Haupttyp mit dem gewünschten Format übereinstimmt, müssen Sie für jeden Medientyp **SetFormat** aufrufen und diesen Medientyp übergeben.



| Format                      | Haupttyp             |
|-----------------------------|------------------------|
| Verschachtelte Audiodaten und Videos | Überlappende \_ mediaType |
| Nur Video                  | MediaType- \_ Video       |



 

Mit der folgenden Funktion wird das Format basierend auf der GUID des Haupt Typs festgelegt.


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



Der msdv-Treiber unterstützt auch **iamstreamconfig**, sodass Sie Code schreiben können, der für beide Gerätetypen funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




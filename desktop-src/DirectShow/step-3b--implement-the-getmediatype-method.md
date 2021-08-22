---
description: Schritt 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Schritt 3B. Implementieren der GetMediaType-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386c16e3166f910e8221d139af519363d1b49279a412603e0cfddfa41773ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583110"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Schritt 3B. Implementieren der GetMediaType-Methode

Dies ist Schritt 3B des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

> [!Note]  
> Dieser Schritt ist für Filter, die von **CTransInPlaceFilter** ableiten, nicht erforderlich.

 

Die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) gibt einen der bevorzugten Ausgabetypen des Filters zurück, auf den von der Indexnummer verwiesen wird. Diese Methode wird nur aufgerufen, wenn der Eingabepin des Filters bereits verbunden ist. Daher können Sie den Medientyp aus der Upstreamverbindung verwenden, um die bevorzugten Ausgabetypen zu bestimmen.

Ein Encoder bietet in der Regel einen einzelnen bevorzugten Typ, der das Zielformat darstellt. Decoder unterstützen in der Regel eine Reihe von Ausgabeformaten und bieten sie in absteigender Qualität oder Effizienz an. Die Liste kann z. B. UYAFFIN, Y211, RGB-24, RGB-565, RGB-555 und RGB-8 in dieser Reihenfolge sein. Effektfilter erfordern möglicherweise eine genaue Übereinstimmung zwischen dem Ausgabeformat und dem Eingabeformat.

Im folgenden Beispiel wird ein einzelner Ausgabetyp zurückgegeben, der durch Ändern des Eingabetyps erstellt wird, um die RLE8-Komprimierung anzugeben:


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



In diesem Beispiel ruft die -Methode [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) auf, um den Eingabetyp vom Eingabepin zu erhalten. Anschließend werden einige Felder geändert, um das Komprimierungsformat wie folgt anzugeben:

-   Sie weist eine neue Untertyp-GUID zu, die mithilfe der [**FOURCCMap-Klasse**](fourccmap.md) aus dem FOURCC-Code "MRLE" erstellt wird.
-   Sie ruft die [**CMediaType::SetVariableSize-Methode**](cmediatype-setvariablesize.md) auf, die das **Flag bFixedSizeSamples** auf **FALSE** und das **lSampleSize-Member** auf 0 (null) festgibt, was Stichproben variabler Größe angibt.
-   Sie ruft die [**CMediaType::SetTemporalCompression-Methode**](cmediatype-settemporalcompression.md) mit dem Wert **FALSE** auf, der angibt, dass jeder Frame ein Keyframe ist. (Dieses Feld ist nur informationell, sodass Sie es problemlos ignorieren können.)
-   Es legt das **Feld biCompression** auf BI \_ RLE8 fest.
-   Das Feld **biSizeImage** wird auf die Bildgröße festgelegt.

Weiter: [Schritt 3C. Implementieren der CheckTransform-Methode](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




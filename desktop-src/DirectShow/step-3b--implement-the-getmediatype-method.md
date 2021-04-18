---
description: Schritt 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Schritt 3B. Implementieren der getmediatype-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530500"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Schritt 3B. Implementieren der getmediatype-Methode

Dies ist Schritt 3B des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

> [!Note]  
> Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.

 

Die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode gibt einen der bevorzugten Ausgabetypen des Filters zurück, auf den von der Indexnummer verwiesen wird. Diese Methode wird nie aufgerufen, es sei denn, die Eingabe-PIN des Filters ist bereits verbunden. Daher können Sie den Medientyp aus der Upstream-Verbindung verwenden, um die bevorzugten Ausgabetypen zu bestimmen.

Ein Encoder bietet in der Regel einen einzelnen bevorzugten Typ, der das Zielformat darstellt. Decoderer unterstützen in der Regel einen Bereich von Ausgabeformaten und bieten Sie in der Reihenfolge absteigender Qualität oder Effizienz an. Die Liste kann beispielsweise "UYVY", "Y211", "RGB-24", "RGB-565", "RGB-555" und "RGB-8" in dieser Reihenfolge sein. Effektfilter erfordern möglicherweise eine genaue Entsprechung zwischen dem Ausgabeformat und dem Eingabeformat.

Im folgenden Beispiel wird ein einzelner Ausgabetyp zurückgegeben, der durch Ändern des Eingabe Typs zum Angeben der RLE8-Komprimierung erstellt wird:


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



In diesem Beispiel ruft die-Methode [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) auf, um den Eingabetyp aus der Eingabe-PIN zu erhalten. Anschließend werden einige der Felder wie folgt geändert, um das Komprimierungs Format anzugeben:

-   Er weist eine neue Untertyp-GUID zu, die aus dem FourCC-Code ' mrle ' mithilfe der [**fourccmap**](fourccmap.md) -Klasse erstellt wird.
-   Er ruft die [**cmediatype:: setvariablesize**](cmediatype-setvariablesize.md) -Methode auf, die das **bfixedsizesamples** -Flag auf **false** und das **lsamplesize** -Element auf 0 (null) festlegt. Dies deutet auf Stichproben variabler Größe hin.
-   Sie ruft die [**cmediatype:: settemporalcompression**](cmediatype-settemporalcompression.md) -Methode mit dem Wert **false** auf, der angibt, dass jeder Frame ein Keyframe ist. (Dieses Feld dient nur zu Informationszwecken, sodass Sie es problemlos ignorieren können.)
-   Das Feld **bicompression** wird auf BI RLE8 festgelegt \_ .
-   Dadurch wird das **bisizeimage** -Feld auf die Bildgröße festgelegt.

Als nächstes: [Schritt 3C. implementieren Sie die checktransform-Methode](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




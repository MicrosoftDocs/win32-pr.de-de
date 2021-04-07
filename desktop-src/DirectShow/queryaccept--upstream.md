---
description: Queryaccept (Upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: Queryaccept (Upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747096"
---
# <a name="queryaccept-upstream"></a>Queryaccept (Upstream)

Dieser Mechanismus ermöglicht es einer Eingabe-PIN, eine Formatänderung an Ihren upstreampeer vorzuschlagen. Der downstreamfilter muss einen Medientyp an das Beispiel anfügen, den der Upstream-Filter beim nächsten Aufrufen von [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)erhält. Zu diesem Zweck muss der Downstream-Filter jedoch eine benutzerdefinierte Zuweisung für die Verbindung bereitstellen. Diese Zuweisung muss eine private Methode implementieren, mit der der Downstream-Filter den Medientyp im nächsten Beispiel festlegen kann.

Dabei werden die folgenden Schritte ausgeführt:

1.  Der Downstream-Filter überprüft, ob die PIN-Verbindung die benutzerdefinierte Zuweisung des Filters verwendet. Wenn der upstreamfilter die Zuweisung besitzt, kann der Downstream-Filter das Format nicht ändern.
2.  Der Downstream-Filter ruft [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für die upstreamausgabepin auf (siehe Abbildung, Schritt A).
3.  Wenn `QueryAccept` S OK zurückgibt \_ , ruft der Downstream-Filter die private-Methode für seine Zuweisung auf, um den Medientyp festzulegen. Innerhalb dieser privaten Methode ruft die Zuweisung [**imediasample:: setmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) beim nächsten verfügbaren Beispiel (B) auf.
4.  Der upstreamfilter ruft **GetBuffer** auf, um ein neues Beispiel (C) und [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) zum erhalten des Medientyps (D) zu erhalten.
5.  Wenn der upstreamfilter das Beispiel liefert, sollte der Medientyp an dieses Beispiel angefügt werden. Auf diese Weise kann der Downstream-Filter bestätigen, dass sich der Medientyp geändert hat (E).

Wenn der upstreamfilter die Formatänderung annimmt, muss er auch in der Lage sein, zurück zum ursprünglichen Medientyp zu wechseln, wie im folgenden Diagramm dargestellt.

![queryaccept (Upstream)](images/dynformat4.png)

Die wichtigsten Beispiele für diese Art von Formatänderung betreffen die DirectShow-Videorenderer.

-   Der ursprüngliche [Videorendererfilter](video-renderer-filter.md) kann während des Streamings zwischen RGB-und YUV-Typen wechseln. Wenn der Filter eine Verbindung herstellt, ist ein RGB-Format erforderlich, das den aktuellen Anzeigeeinstellungen entspricht. Dadurch wird sichergestellt, dass GDI auf GDI zurückgegriffen werden kann, wenn dies erforderlich ist. Nachdem das Streaming begonnen hat, fordert der Videorenderer eine Formatänderung an einen YUV-Typ an, wenn DirectDraw verfügbar ist. Zu einem späteren Zeitpunkt wechselt Sie möglicherweise zurück zu RGB, wenn die DirectDraw-Oberfläche aus irgendeinem Grund verloren geht.
-   Der neuere Filter für Video Mischungs Renderer (VMR) stellt eine Verbindung mit einem beliebigen Format her, das von der Grafikhardware unterstützt wird, einschließlich YUV-Typen. Allerdings kann die Grafikhardware den Schritt der zugrunde liegenden DirectDraw-Oberfläche ändern, um die Leistung zu optimieren. Der VMR-Filter verwendet, `QueryAccept` um den neuen Stride zu melden, der im **biwidth** -Member der **BITMAPINFOHEADER** -Struktur angegeben wird. Die Quell-und Ziel Rechtecke in der **videoinfoheader** -oder **VIDEOINFOHEADER2** -Struktur identifizieren die Region, in der das Video decodiert werden soll.

**Implementierungs Hinweis**

Es ist unwahrscheinlich, dass Sie einen Filter schreiben, bei dem upstreamformatänderungen angefordert werden müssen, da dies hauptsächlich eine Funktion von Videorenderer ist. Wenn Sie jedoch einen Video Transformations Filter oder einen Video Decoder schreiben, muss der Filter ordnungsgemäß auf Anforderungen vom Videorenderer Antworten.

Ein direkter Filter, der zwischen dem Videorenderer und dem Decoder liegt, sollte alle `QueryAccept` Aufrufe mit Upstream bestehen. Speichern Sie die neuen Formatierungsinformationen, wenn Sie ankommen.

Ein Kopier-und Transformations Filter (d. h. ein nicht-transdirekter Filter) sollte eines der folgenden Verhaltensweisen implementieren:

-   Übergeben Sie die Formatänderungen Upstream, und speichern Sie die neuen Formatierungsinformationen, wenn Sie ankommen. Der Filter muss eine benutzerdefinierte Zuweisung verwenden, damit er das Format an das upstreambeispiel anfügen kann.
-   Führen Sie die Formatkonvertierung innerhalb des Filters aus. Dies ist wahrscheinlich einfacher als das übertragen der Format Änderungs upstreamdatei. Möglicherweise ist Sie jedoch weniger effizient als das Decodieren des Decoders in das richtige Format.
-   Als letztes Mittel sollten Sie die Formatänderung einfach ablehnen. (Weitere Informationen finden Sie im Quellcode für die [**ctransinplaceoutputpin:: checkmediatype**](ctransinplaceoutputpin-checkmediatype.md) -Methode in der DirectShow-Basisklassen Bibliothek.) Das Ablehnen einer Formatänderung kann jedoch die Leistung beeinträchtigen, da der Videorenderer verhindert, dass das effizienteste Format verwendet wird.

Der folgende Pseudo Code zeigt, wie Sie einen von **ctransformfilter** abgeleiteten Kopier-und Transformations Filter implementieren können, der zwischen YUV-und RGB-Ausgabetypen wechseln kann. In diesem Beispiel wird davon ausgegangen, dass der Filter die Konvertierung selbst durchführt, anstatt die Formatänderung Upstream zu übergeben.


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 




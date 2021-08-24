---
description: QueryAccept (Upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (Upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65133e132a0e1c2e6880009eda8b56fde9bf77a8bc7d68a850a6f8963604aecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747575"
---
# <a name="queryaccept-upstream"></a>QueryAccept (Upstream)

Mit diesem Mechanismus kann ein Eingabepin eine Formatänderung an seinen Upstream-Peer vorschlagen. Der Downstreamfilter muss einen Medientyp an das Beispiel anfügen, das der Upstreamfilter beim nächsten Aufruf von [**IMemAllocator::GetBuffer abruft.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) Hierzu muss der Downstreamfilter jedoch eine benutzerdefinierte Zuweisung für die Verbindung bereitstellen. Diese Zuweisung muss eine private Methode implementieren, mit der der Downstreamfilter den Medientyp für das nächste Beispiel festlegen kann.

Dabei werden die folgenden Schritte ausgeführt:

1.  Der Downstreamfilter überprüft, ob die Pinverbindung die benutzerdefinierte Zuweisung des Filters verwendet. Wenn der Upstreamfilter die Zuweisung besitzt, kann der Downstreamfilter das Format nicht ändern.
2.  Der Downstreamfilter ruft [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Upstreamausgabepin auf (siehe Abbildung, Schritt A).
3.  Wenn S OK zurückgibt, ruft der Downstreamfilter die private Methode für seine Zuweisung `QueryAccept` \_ auf, um den Medientyp zu festlegen. Innerhalb dieser privaten Methode ruft die Zuweisung im nächsten verfügbaren Beispiel (B) [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) auf.
4.  Der Upstreamfilter ruft **GetBuffer auf,** um ein neues Beispiel (C) und [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) zu erhalten, um den Medientyp (D) zu erhalten.
5.  Wenn der Upstreamfilter das Beispiel liefert, sollte der Medientyp an dieses Beispiel angefügt werden. Auf diese Weise kann der Downstreamfilter bestätigen, dass sich der Medientyp geändert hat (E).

Wenn der Upstreamfilter die Formatänderung akzeptiert, muss er auch wieder zum ursprünglichen Medientyp wechseln können, wie im folgenden Diagramm dargestellt.

![queryaccept (upstream)](images/dynformat4.png)

Die wichtigsten Beispiele für diese Art von Formatänderung sind die DirectShow-Videorenderer.

-   Der ursprüngliche [Videorendererfilter](video-renderer-filter.md) kann während des Streamings zwischen RGB- und YUV-Typen wechseln. Wenn der Filter eine Verbindung herstellt, ist ein RGB-Format erforderlich, das den aktuellen Anzeigeeinstellungen entspricht. Dadurch wird sichergestellt, dass bei Bedarf auf GDI zurückverwendt werden kann. Wenn DirectDraw verfügbar ist, fordert der Videorenderer nach Beginn des Streamings eine Formatänderung in einen YUV-Typ an. Später kann es zu RGB zurückwechseln, wenn die DirectDraw-Oberfläche aus irgendeinem Grund verloren geht.
-   Der neuere VmR-Filter (Video Mixing Renderer) stellt eine Verbindung mit einem beliebigen Format, das von der Grafikhardware unterstützt wird, einschließlich YUV-Typen, sicher. Die Grafikhardware kann jedoch den Schritt der zugrunde liegenden DirectDraw-Oberfläche ändern, um die Leistung zu optimieren. Der VMR-Filter verwendet , um den neuen Schritt zu melden, der `QueryAccept` im **biWidth-Element** der **BITMAPINFOHEADER-Struktur angegeben** ist. Die Quell- und Zielrechtecke in der **VIDEOINFOHEADER-** oder **VIDEOINFOHEADER2-Struktur** identifizieren den Bereich, in dem das Video decodiert werden soll.

**Implementierungshinweis**

Es ist unwahrscheinlich, dass Sie einen Filter schreiben, der Upstreamformatänderungen anfordern muss, da dies hauptsächlich ein Feature von Videorenderern ist. Wenn Sie jedoch einen Videotransformationsfilter oder einen Videodecoder schreiben, muss Ihr Filter ordnungsgemäß auf Anforderungen vom Videorenderer reagieren.

Ein Trans-in-Place-Filter, der sich zwischen dem Videorenderer und dem Decoder befindet, sollte alle Aufrufe `QueryAccept` upstream übergeben. Store die neuen Formatinformationen, wenn sie eintreffen.

Ein Kopiertransformationsfilter (d. h. ein nicht trans-in-place-Filter) sollte eines der folgenden Verhaltensweisen implementieren:

-   Übergeben Sie Formatänderungen upstream, und speichern Sie die neuen Formatinformationen, wenn sie eintreffen. Ihr Filter muss eine benutzerdefinierte Zuweisung verwenden, damit er das Format an das Upstreambeispiel anfügen kann.
-   Führen Sie die Formatkonvertierung innerhalb des Filters aus. Dies ist wahrscheinlich einfacher, als die Formatänderung upstream zu übergeben. Es kann jedoch weniger effizient sein, als den Decoderfilter in das richtige Format decodieren zu lassen.
-   Als letztes Mittel lehnen Sie einfach die Formatänderung ab. (Weitere Informationen finden Sie im Quellcode für die [**CTransInPlaceOutputPin::CheckMediaType-Methode**](ctransinplaceoutputpin-checkmediatype.md) in der DirectShow-Basisklassenbibliothek.) Das Ablehnen einer Formatänderung kann jedoch die Leistung beeinträchtigen, da sie verhindert, dass der Videorenderer das effizienteste Format verwendet.

Der folgende Pseudocode zeigt, wie Sie einen Kopiertransformationsfilter (abgeleitet von **CTransformFilter)** implementieren können, der zwischen YUV- und RGB-Ausgabetypen wechseln kann. In diesem Beispiel wird davon ausgegangen, dass der Filter die Konvertierung selbst übernimmt, anstatt die Formatänderung upstream zu übergeben.


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



 

 




---
description: In diesem Thema wird beschrieben, wie Sie einen Vorschaupin für einen DirectShow-Erfassungsfilter implementieren.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementieren eines Vorschaupins (optional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de47b86df70500c83c794fe1074dc927622d571e78ef6175b944702277da492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015558"
---
# <a name="implementing-a-preview-pin-optional"></a>Implementieren eines Vorschaupins (optional)

In diesem Thema wird beschrieben, wie Sie einen Vorschaupin für einen DirectShow-Erfassungsfilter implementieren.

Wenn Ihr Filter über einen Vorschaupin verfügt, muss der Pin der Vorschau eine Kopie der vom Aufnahmepin übermittelten Daten senden. Nur wenn Daten vom Vorschaupin gesendet werden, werden durch den Aufnahmepin keine Frames entfernt. Der Aufnahmepin hat immer Priorität vor dem Vorschaupin.

Der Aufnahmepin und der Vorschaupin müssen Daten im gleichen Format senden. Daher müssen sie eine Verbindung mithilfe identischer Medientypen herstellen. Wenn der Erfassungspin zuerst eine Verbindung herstellt, sollte der Vorschaupin denselben Medientyp bieten und alle anderen Typen ablehnen. Wenn der Vorschaupin zuerst eine Verbindung herstellt und der Erfassungspin eine Verbindung mit einem anderen Medientyp herstellt, sollte der Vorschaupin die Verbindung mit dem neuen Medientyp wiederherstellen. Wenn der Filter, der dem Vorschaupin nachgeschaltet ist, den neuen Typ ablehnt, sollte der Erfassungspin auch den Typ ablehnen. Verwenden Sie [**die IPin::QueryAccept-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) um den Filter downstream vom Vorschaupin abfragt, und verwenden Sie die [**IFilterGraph::Reconnect-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) um die Verbindung mit dem Pin wiederherzustellen. Diese Regeln gelten auch, wenn der Filter Graph Manager erneut eine Verbindung mit dem Erfassungspin herstellen kann.

Das folgende Beispiel zeigt eine Gliederung dieses Prozesses:


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionsweise von Verbinden](how-filters-connect.md)
</dt> <dt>

[Schreiben von Erfassungsfiltern](writing-capture-filters.md)
</dt> </dl>

 

 




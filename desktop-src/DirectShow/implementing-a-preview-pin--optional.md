---
description: In diesem Thema wird beschrieben, wie eine Vorschau-PIN für einen DirectShow-Erfassungs Filter implementiert wird.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementieren einer Vorschau-PIN (optional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392741"
---
# <a name="implementing-a-preview-pin-optional"></a>Implementieren einer Vorschau-PIN (optional)

In diesem Thema wird beschrieben, wie eine Vorschau-PIN für einen DirectShow-Erfassungs Filter implementiert wird.

Wenn Ihr Filter über eine Vorschau-Pin verfügt, muss die Vorschau-Pin eine Kopie der von der Erfassungs-Pin übermittelten Daten senden. Wenn Sie Daten nur aus der Vorschau-Pin senden, bewirkt dies nicht, dass die Erfassungs-Pin Frames ablöscht. Die Erfassungs-Pin hat immer Vorrang vor der Vorschau-PIN.

Die Erfassungs-PIN und die Vorschau-PIN müssen Daten im gleichen Format senden. Daher müssen Sie mit identischen Medientypen eine Verbindung herstellen. Wenn die Erfassungs-Pin zuerst eine Verbindung herstellt, sollte die Vorschau-Pin denselben Medientyp anbieten und alle anderen Typen ablehnen. Wenn die Vorschau-Pin zuerst eine Verbindung herstellt und die Erfassungs-Pin eine Verbindung mit einem anderen Medientyp herstellt, sollte die Vorschau-PIN mit dem neuen Medientyp erneut eine Verbindung herstellen. Wenn der von der Vorschau-Pin nachgelagerte Filter den neuen Typ ablehnt, sollte die Erfassungs-Pin ebenfalls den Typ ablehnen. Verwenden Sie die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode, um den Filter nach unten über die Vorschau-Pin abzufragen, und verwenden Sie die [**ifiltergraph:: Verbindung**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) -Methode, um die PIN erneut zu verbinden. Diese Regeln gelten auch, wenn der Filter Graph-Manager die Erfassungs-PIN erneut verbindet.

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

[Herstellen der Verbindung von Filtern](how-filters-connect.md)
</dt> <dt>

[Schreiben von Erfassungs Filtern](writing-capture-filters.md)
</dt> </dl>

 

 




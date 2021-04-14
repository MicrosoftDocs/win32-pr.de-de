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
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="3205b-103">Implementieren einer Vorschau-PIN (optional)</span><span class="sxs-lookup"><span data-stu-id="3205b-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="3205b-104">In diesem Thema wird beschrieben, wie eine Vorschau-PIN für einen DirectShow-Erfassungs Filter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3205b-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="3205b-105">Wenn Ihr Filter über eine Vorschau-Pin verfügt, muss die Vorschau-Pin eine Kopie der von der Erfassungs-Pin übermittelten Daten senden.</span><span class="sxs-lookup"><span data-stu-id="3205b-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="3205b-106">Wenn Sie Daten nur aus der Vorschau-Pin senden, bewirkt dies nicht, dass die Erfassungs-Pin Frames ablöscht.</span><span class="sxs-lookup"><span data-stu-id="3205b-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="3205b-107">Die Erfassungs-Pin hat immer Vorrang vor der Vorschau-PIN.</span><span class="sxs-lookup"><span data-stu-id="3205b-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="3205b-108">Die Erfassungs-PIN und die Vorschau-PIN müssen Daten im gleichen Format senden.</span><span class="sxs-lookup"><span data-stu-id="3205b-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="3205b-109">Daher müssen Sie mit identischen Medientypen eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="3205b-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="3205b-110">Wenn die Erfassungs-Pin zuerst eine Verbindung herstellt, sollte die Vorschau-Pin denselben Medientyp anbieten und alle anderen Typen ablehnen.</span><span class="sxs-lookup"><span data-stu-id="3205b-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="3205b-111">Wenn die Vorschau-Pin zuerst eine Verbindung herstellt und die Erfassungs-Pin eine Verbindung mit einem anderen Medientyp herstellt, sollte die Vorschau-PIN mit dem neuen Medientyp erneut eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="3205b-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="3205b-112">Wenn der von der Vorschau-Pin nachgelagerte Filter den neuen Typ ablehnt, sollte die Erfassungs-Pin ebenfalls den Typ ablehnen.</span><span class="sxs-lookup"><span data-stu-id="3205b-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="3205b-113">Verwenden Sie die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode, um den Filter nach unten über die Vorschau-Pin abzufragen, und verwenden Sie die [**ifiltergraph:: Verbindung**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) -Methode, um die PIN erneut zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="3205b-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="3205b-114">Diese Regeln gelten auch, wenn der Filter Graph-Manager die Erfassungs-PIN erneut verbindet.</span><span class="sxs-lookup"><span data-stu-id="3205b-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="3205b-115">Das folgende Beispiel zeigt eine Gliederung dieses Prozesses:</span><span class="sxs-lookup"><span data-stu-id="3205b-115">The following example shows an outline of this process:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3205b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3205b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3205b-117">Herstellen der Verbindung von Filtern</span><span class="sxs-lookup"><span data-stu-id="3205b-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="3205b-118">Schreiben von Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="3205b-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 




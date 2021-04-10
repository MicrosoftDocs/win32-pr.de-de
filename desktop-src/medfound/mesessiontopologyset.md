---
description: 'Wird ausgelöst, nachdem die imfmediasession:: settopology-Methode asynchron abgeschlossen wurde. Die Medien Sitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie zur Wiedergabe in die Warteschlange eingereiht wurde.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Mesessiontopologyset-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959300"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="8b67d-104">Mesessiontopologyset-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8b67d-104">MESessionTopologySet event</span></span>

<span data-ttu-id="8b67d-105">Wird ausgelöst, nachdem die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode asynchron abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8b67d-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="8b67d-106">Die Medien Sitzung löst dieses Ereignis aus, nachdem die Topologie in eine vollständige Topologie aufgelöst und die Topologie zur Wiedergabe in die Warteschlange eingereiht wurde.</span><span class="sxs-lookup"><span data-stu-id="8b67d-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="8b67d-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="8b67d-107">Event values</span></span>

<span data-ttu-id="8b67d-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="8b67d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8b67d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8b67d-109">VARTYPE</span></span>                | <span data-ttu-id="8b67d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b67d-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b67d-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="8b67d-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="8b67d-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="8b67d-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="8b67d-113">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="8b67d-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="8b67d-114">Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der vollständigen Topologie.</span><span class="sxs-lookup"><span data-stu-id="8b67d-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="8b67d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b67d-115">Examples</span></span>

<span data-ttu-id="8b67d-116">Im folgenden Beispiel wird der [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Zeiger von einem mesessiontopologyset-Ereignis abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b67d-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="8b67d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b67d-117">Requirements</span></span>



| <span data-ttu-id="8b67d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b67d-118">Requirement</span></span> | <span data-ttu-id="8b67d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8b67d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b67d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b67d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b67d-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b67d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b67d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b67d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b67d-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b67d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b67d-124">Header</span><span class="sxs-lookup"><span data-stu-id="8b67d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b67d-125"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b67d-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b67d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b67d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b67d-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b67d-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





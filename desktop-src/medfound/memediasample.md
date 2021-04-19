---
description: 'Wird gesendet, wenn ein Mediendaten Strom ein neues Beispiel als Reaktion auf einen imfmediastream:: requestsample-Rückruf liefert.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Memediasample-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106369930"
---
# <a name="memediasample-event"></a><span data-ttu-id="aeb82-103">Memediasample-Ereignis</span><span class="sxs-lookup"><span data-stu-id="aeb82-103">MEMediaSample event</span></span>

<span data-ttu-id="aeb82-104">Wird gesendet, wenn ein Mediendaten Strom ein neues Beispiel als Reaktion auf einen [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)-Rückruf liefert.</span><span class="sxs-lookup"><span data-stu-id="aeb82-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="aeb82-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="aeb82-105">Event values</span></span>

<span data-ttu-id="aeb82-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="aeb82-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="aeb82-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="aeb82-107">VARTYPE</span></span>                | <span data-ttu-id="aeb82-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aeb82-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb82-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="aeb82-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="aeb82-110">Ein Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="aeb82-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="aeb82-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aeb82-111">Requirements</span></span>



| <span data-ttu-id="aeb82-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aeb82-112">Requirement</span></span> | <span data-ttu-id="aeb82-113">Wert</span><span class="sxs-lookup"><span data-stu-id="aeb82-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb82-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aeb82-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb82-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aeb82-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aeb82-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aeb82-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb82-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aeb82-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aeb82-118">Header</span><span class="sxs-lookup"><span data-stu-id="aeb82-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb82-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aeb82-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb82-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeb82-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb82-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aeb82-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="aeb82-122">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="aeb82-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 





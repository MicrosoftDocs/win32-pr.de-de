---
description: Signalisiert, dass eine Medienquelle die Pufferung der Daten beendet hat.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Mebufferingbeendete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344299"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="d9854-103">Mebufferingbeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d9854-103">MEBufferingStopped event</span></span>

<span data-ttu-id="d9854-104">Signalisiert, dass eine Medienquelle die Pufferung der Daten beendet hat.</span><span class="sxs-lookup"><span data-stu-id="d9854-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="d9854-105">Eine Medienquelle sendet diese Nachricht, wenn Sie das Puffern von Daten nach dem Senden des [mebufferingstarted](mebufferingstarted.md) -Ereignisses stoppt.</span><span class="sxs-lookup"><span data-stu-id="d9854-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="d9854-106">Bytestreams, die die [**IMF bytestreambufferate**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) -Schnittstelle implementieren, senden ebenfalls dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d9854-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="d9854-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="d9854-107">Event values</span></span>

<span data-ttu-id="d9854-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="d9854-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d9854-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d9854-109">VARTYPE</span></span>              | <span data-ttu-id="d9854-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9854-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d9854-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="d9854-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d9854-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="d9854-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d9854-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9854-113">Remarks</span></span>

<span data-ttu-id="d9854-114">Wenn die Medien Sitzung dieses Ereignis empfängt, wird die Präsentations Uhr neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d9854-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="d9854-115">Die Medien Sitzung leitet das Ereignis auch an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="d9854-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9854-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9854-116">Requirements</span></span>



| <span data-ttu-id="d9854-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9854-117">Requirement</span></span> | <span data-ttu-id="d9854-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d9854-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9854-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9854-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9854-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9854-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9854-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9854-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9854-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9854-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9854-123">Header</span><span class="sxs-lookup"><span data-stu-id="d9854-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9854-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9854-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9854-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9854-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9854-126">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9854-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





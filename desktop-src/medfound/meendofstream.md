---
description: Wird von einem Mediendaten Strom ausgelöst, wenn der Stream endet.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Meendofstream-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863619"
---
# <a name="meendofstream-event"></a><span data-ttu-id="5ea13-103">Meendof Stream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5ea13-103">MEEndOfStream event</span></span>

<span data-ttu-id="5ea13-104">Wird von einem Mediendaten Strom ausgelöst, wenn der Stream endet.</span><span class="sxs-lookup"><span data-stu-id="5ea13-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="5ea13-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="5ea13-105">Event values</span></span>

<span data-ttu-id="5ea13-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="5ea13-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5ea13-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5ea13-107">VARTYPE</span></span>              | <span data-ttu-id="5ea13-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ea13-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5ea13-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="5ea13-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5ea13-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="5ea13-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5ea13-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ea13-111">Remarks</span></span>

<span data-ttu-id="5ea13-112">Wenn die [Medien Sitzung](media-session.md) das meendosstream-Ereignis empfängt, wird [**IMF streamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) auf der entsprechenden Medien Senke mit dem Markertyp " **MF streamsink \_ Marker \_ endossegment** " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ea13-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea13-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ea13-113">Requirements</span></span>



| <span data-ttu-id="5ea13-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ea13-114">Requirement</span></span> | <span data-ttu-id="5ea13-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5ea13-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea13-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ea13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea13-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ea13-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ea13-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ea13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea13-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ea13-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ea13-120">Header</span><span class="sxs-lookup"><span data-stu-id="5ea13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea13-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea13-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea13-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea13-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ea13-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





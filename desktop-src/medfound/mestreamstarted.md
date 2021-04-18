---
description: Wird von einem Medienstrom ausgelöst, wenn die Quelle startet, ohne zu suchen. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das mesourcestarted-Ereignis auslöst.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Mestreamstarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368203"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="b6894-104">Mestreamstarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b6894-104">MEStreamStarted event</span></span>

<span data-ttu-id="b6894-105">Wird von einem Medienstrom ausgelöst, wenn die Quelle startet, ohne zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b6894-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="b6894-106">Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das [mesourcestarted](mesourcestarted.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="b6894-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="b6894-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="b6894-107">Event values</span></span>

<span data-ttu-id="b6894-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="b6894-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b6894-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b6894-109">VARTYPE</span></span>              | <span data-ttu-id="b6894-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6894-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6894-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="b6894-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b6894-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="b6894-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="b6894-113">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="b6894-113">VT\_I8</span></span><br/>    | <span data-ttu-id="b6894-114">Die Startzeit in 100-Nanosecond-Einheiten in Relation zu den Zeitstempeln der Stichproben.</span><span class="sxs-lookup"><span data-stu-id="b6894-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b6894-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6894-115">Requirements</span></span>



| <span data-ttu-id="b6894-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6894-116">Requirement</span></span> | <span data-ttu-id="b6894-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b6894-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6894-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6894-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6894-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6894-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6894-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6894-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6894-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6894-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6894-122">Header</span><span class="sxs-lookup"><span data-stu-id="b6894-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6894-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6894-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6894-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6894-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6894-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6894-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





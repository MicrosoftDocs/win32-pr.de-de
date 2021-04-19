---
description: 'Wird ausgelöst, wenn eine Medienquelle eine neue Position ansucht. Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wurde und die Anwendung imfmediasource:: Start mit einer Startzeit aufruft, die nicht der aktuellen Position entspricht.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Mesourceseeked-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346988"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="a773a-104">Mesourceseeked-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a773a-104">MESourceSeeked event</span></span>

<span data-ttu-id="a773a-105">Wird ausgelöst, wenn eine Medienquelle eine neue Position ansucht.</span><span class="sxs-lookup"><span data-stu-id="a773a-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="a773a-106">Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wurde und die Anwendung [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) mit einer Startzeit aufruft, die nicht der aktuellen Position entspricht.</span><span class="sxs-lookup"><span data-stu-id="a773a-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="a773a-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="a773a-107">Event values</span></span>

<span data-ttu-id="a773a-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="a773a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a773a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a773a-109">VARTYPE</span></span>           | <span data-ttu-id="a773a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a773a-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a773a-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="a773a-111">VT\_I8</span></span><br/> | <span data-ttu-id="a773a-112">Die neue Startposition in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="a773a-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a773a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a773a-113">Requirements</span></span>



| <span data-ttu-id="a773a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a773a-114">Requirement</span></span> | <span data-ttu-id="a773a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a773a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a773a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a773a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a773a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a773a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a773a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a773a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a773a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a773a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a773a-120">Header</span><span class="sxs-lookup"><span data-stu-id="a773a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a773a-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a773a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a773a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a773a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a773a-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a773a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





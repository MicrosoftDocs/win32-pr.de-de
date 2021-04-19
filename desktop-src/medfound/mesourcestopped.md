---
description: 'Wird von einer Medienquelle ausgelöst, wenn die imfmediasource:: beenden-Methode asynchron abgeschlossen wird.'
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Mesourcestjects-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348443"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="f46a8-103">Mesourcestpt-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f46a8-103">MESourceStopped event</span></span>

<span data-ttu-id="f46a8-104">Wird von einer Medienquelle ausgelöst, wenn die [**imfmediasource:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f46a8-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="f46a8-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="f46a8-105">Event values</span></span>

<span data-ttu-id="f46a8-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="f46a8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f46a8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f46a8-107">VARTYPE</span></span>              | <span data-ttu-id="f46a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f46a8-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f46a8-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="f46a8-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f46a8-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f46a8-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f46a8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f46a8-111">Requirements</span></span>



| <span data-ttu-id="f46a8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f46a8-112">Requirement</span></span> | <span data-ttu-id="f46a8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f46a8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46a8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f46a8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f46a8-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f46a8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f46a8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f46a8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f46a8-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f46a8-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f46a8-118">Header</span><span class="sxs-lookup"><span data-stu-id="f46a8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f46a8-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f46a8-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f46a8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f46a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46a8-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f46a8-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





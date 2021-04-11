---
description: Wird ausgelöst, wenn die imfmediasession::P ause-Methode asynchron abgeschlossen wird.
ms.assetid: 72546082-83ec-4481-a24f-e82bd6c88859
title: Mesessionangeh Ed-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3e8ef60426f83203cfffae3a75febfdf7032d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130737"
---
# <a name="mesessionpaused-event"></a><span data-ttu-id="ae0b3-103">Mesessionpaused-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ae0b3-103">MESessionPaused event</span></span>

<span data-ttu-id="ae0b3-104">Wird ausgelöst, wenn die [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ae0b3-104">Raised when the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ae0b3-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ae0b3-105">Event values</span></span>

<span data-ttu-id="ae0b3-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ae0b3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ae0b3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ae0b3-107">VARTYPE</span></span>              | <span data-ttu-id="ae0b3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae0b3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ae0b3-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="ae0b3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ae0b3-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ae0b3-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ae0b3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae0b3-111">Requirements</span></span>



| <span data-ttu-id="ae0b3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae0b3-112">Requirement</span></span> | <span data-ttu-id="ae0b3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ae0b3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0b3-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae0b3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae0b3-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae0b3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae0b3-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae0b3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae0b3-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae0b3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae0b3-118">Header</span><span class="sxs-lookup"><span data-stu-id="ae0b3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae0b3-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae0b3-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae0b3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae0b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae0b3-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae0b3-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





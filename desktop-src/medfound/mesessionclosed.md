---
description: 'Wird ausgelöst, wenn die imfmediasession:: Close-Methode asynchron abgeschlossen wird.'
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: Mesessionclosed-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343781"
---
# <a name="mesessionclosed-event"></a><span data-ttu-id="eff1f-103">Mesessionclosed-Ereignis</span><span class="sxs-lookup"><span data-stu-id="eff1f-103">MESessionClosed event</span></span>

<span data-ttu-id="eff1f-104">Wird ausgelöst, wenn die [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="eff1f-104">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="eff1f-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="eff1f-105">Event values</span></span>

<span data-ttu-id="eff1f-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="eff1f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="eff1f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="eff1f-107">VARTYPE</span></span>              | <span data-ttu-id="eff1f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eff1f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="eff1f-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="eff1f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="eff1f-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="eff1f-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="eff1f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eff1f-111">Requirements</span></span>



| <span data-ttu-id="eff1f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eff1f-112">Requirement</span></span> | <span data-ttu-id="eff1f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="eff1f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff1f-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eff1f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eff1f-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eff1f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eff1f-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eff1f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eff1f-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eff1f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eff1f-118">Header</span><span class="sxs-lookup"><span data-stu-id="eff1f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="eff1f-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eff1f-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eff1f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eff1f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff1f-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eff1f-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





---
description: Wird ausgelöst, wenn die Lizenz Erfassung beendet ist. Weitere Informationen finden Sie unter "melicenabacquisitionstart".
ms.assetid: f577131b-887a-4912-8278-1165a801c2b3
title: Melicenmenacquisitionabgeschlossene-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 545fa012f974637f5d268a7d8257daaf9b393f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353199"
---
# <a name="melicenseacquisitioncompleted-event"></a><span data-ttu-id="5d8fa-104">Melicenmenacquisitionabgeschlossene-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5d8fa-104">MELicenseAcquisitionCompleted event</span></span>

<span data-ttu-id="5d8fa-105">Wird ausgelöst, wenn die Lizenz Erfassung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="5d8fa-105">Raised when license acquisition is complete.</span></span> <span data-ttu-id="5d8fa-106">Weitere Informationen finden Sie unter " [melicenabacquisitionstart](melicenseacquisitionstart.md)".</span><span class="sxs-lookup"><span data-stu-id="5d8fa-106">For more information, see [MELicenseAcquisitionStart](melicenseacquisitionstart.md).</span></span>

## <a name="event-values"></a><span data-ttu-id="5d8fa-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="5d8fa-107">Event values</span></span>

<span data-ttu-id="5d8fa-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="5d8fa-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5d8fa-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5d8fa-109">VARTYPE</span></span>              | <span data-ttu-id="5d8fa-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d8fa-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5d8fa-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="5d8fa-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5d8fa-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="5d8fa-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5d8fa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d8fa-113">Requirements</span></span>



| <span data-ttu-id="5d8fa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d8fa-114">Requirement</span></span> | <span data-ttu-id="5d8fa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5d8fa-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8fa-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d8fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8fa-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d8fa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5d8fa-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d8fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8fa-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d8fa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d8fa-120">Header</span><span class="sxs-lookup"><span data-stu-id="5d8fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d8fa-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d8fa-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d8fa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d8fa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8fa-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d8fa-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





---
description: 'Wird ausgelöst, wenn die imfmediasession:: beenden-Methode asynchron abgeschlossen wird.'
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: Mesessionbeendete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349429"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="a8252-103">Mesessionbeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a8252-103">MESessionStopped event</span></span>

<span data-ttu-id="a8252-104">Wird ausgelöst, wenn die [**imfmediasession:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a8252-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="a8252-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="a8252-105">Event values</span></span>

<span data-ttu-id="a8252-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="a8252-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a8252-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a8252-107">VARTYPE</span></span>              | <span data-ttu-id="a8252-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8252-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a8252-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="a8252-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a8252-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="a8252-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a8252-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8252-111">Requirements</span></span>



| <span data-ttu-id="a8252-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8252-112">Requirement</span></span> | <span data-ttu-id="a8252-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a8252-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8252-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8252-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a8252-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8252-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8252-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8252-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a8252-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8252-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8252-118">Header</span><span class="sxs-lookup"><span data-stu-id="a8252-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8252-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8252-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8252-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8252-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8252-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8252-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





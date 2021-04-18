---
description: 'Wird von einem Mediendaten Strom ausgelöst, wenn die imfmediasource:: beenden-Methode asynchron abgeschlossen wird.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Mestreambeendeten-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358581"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="39a2b-103">Mestreambeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="39a2b-103">MEStreamStopped event</span></span>

<span data-ttu-id="39a2b-104">Wird von einem Mediendaten Strom ausgelöst, wenn die [**imfmediasource:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="39a2b-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="39a2b-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="39a2b-105">Event values</span></span>

<span data-ttu-id="39a2b-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="39a2b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="39a2b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="39a2b-107">VARTYPE</span></span>              | <span data-ttu-id="39a2b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39a2b-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="39a2b-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="39a2b-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="39a2b-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="39a2b-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="39a2b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39a2b-111">Remarks</span></span>

<span data-ttu-id="39a2b-112">Jeder aktive Stream in der Präsentation sendet dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="39a2b-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a2b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39a2b-113">Requirements</span></span>



| <span data-ttu-id="39a2b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39a2b-114">Requirement</span></span> | <span data-ttu-id="39a2b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39a2b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a2b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39a2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39a2b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39a2b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39a2b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39a2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39a2b-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39a2b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39a2b-120">Header</span><span class="sxs-lookup"><span data-stu-id="39a2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a2b-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39a2b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a2b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39a2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a2b-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39a2b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





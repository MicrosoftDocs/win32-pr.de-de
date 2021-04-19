---
description: Wird von der Netzwerkquelle ausgelöst, wenn das Öffnen einer URL abgeschlossen ist.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Meconnectend-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355531"
---
# <a name="meconnectend-event"></a><span data-ttu-id="94305-103">Meconnectend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="94305-103">MEConnectEnd event</span></span>

<span data-ttu-id="94305-104">Wird von der Netzwerkquelle ausgelöst, wenn das Öffnen einer URL abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="94305-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="94305-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="94305-105">Event values</span></span>

<span data-ttu-id="94305-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="94305-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="94305-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="94305-107">VARTYPE</span></span>              | <span data-ttu-id="94305-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94305-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="94305-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="94305-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="94305-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="94305-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="94305-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94305-111">Remarks</span></span>

<span data-ttu-id="94305-112">Die Netzwerkquelle sendet dieses Ereignis direkt über die [**imfsourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode der Anwendung an die Anwendung, nicht über die übliche [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="94305-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="94305-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94305-113">Requirements</span></span>



| <span data-ttu-id="94305-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94305-114">Requirement</span></span> | <span data-ttu-id="94305-115">Wert</span><span class="sxs-lookup"><span data-stu-id="94305-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94305-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94305-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94305-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94305-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94305-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94305-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94305-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94305-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94305-120">Header</span><span class="sxs-lookup"><span data-stu-id="94305-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="94305-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94305-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94305-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94305-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94305-123">**IMF sourceopenmonitor**</span><span class="sxs-lookup"><span data-stu-id="94305-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="94305-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94305-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





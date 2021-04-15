---
description: Wird von der Netzwerkquelle ausgelöst, wenn mit dem Öffnen einer URL begonnen wird.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Meconnectstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e45d723a62854c34ba7b297e462d03fed97a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527431"
---
# <a name="meconnectstart-event"></a><span data-ttu-id="344f7-103">Meconnectstart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="344f7-103">MEConnectStart event</span></span>

<span data-ttu-id="344f7-104">Wird von der Netzwerkquelle ausgelöst, wenn mit dem Öffnen einer URL begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="344f7-104">Raised by the network source when it starts opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="344f7-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="344f7-105">Event values</span></span>

<span data-ttu-id="344f7-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="344f7-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="344f7-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="344f7-107">VARTYPE</span></span>              | <span data-ttu-id="344f7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="344f7-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="344f7-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="344f7-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="344f7-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="344f7-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="344f7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="344f7-111">Remarks</span></span>

<span data-ttu-id="344f7-112">Die Netzwerkquelle sendet dieses Ereignis direkt über die [**imfsourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode der Anwendung an die Anwendung, nicht über die übliche [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="344f7-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="344f7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="344f7-113">Requirements</span></span>



| <span data-ttu-id="344f7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="344f7-114">Requirement</span></span> | <span data-ttu-id="344f7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="344f7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="344f7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="344f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="344f7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="344f7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="344f7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="344f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="344f7-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="344f7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="344f7-120">Header</span><span class="sxs-lookup"><span data-stu-id="344f7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="344f7-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="344f7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="344f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344f7-123">**IMF sourceopenmonitor**</span><span class="sxs-lookup"><span data-stu-id="344f7-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="344f7-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="344f7-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





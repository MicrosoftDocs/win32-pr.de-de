---
description: Ein Filter fordert an, dass das Diagramm neu gestartet wird.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353793"
---
# <a name="ec_need_restart"></a><span data-ttu-id="eaf0e-103">EC \_ muss \_ neu gestartet werden</span><span class="sxs-lookup"><span data-stu-id="eaf0e-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="eaf0e-104">Ein Filter fordert an, dass das Diagramm neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaf0e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaf0e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf0e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="eaf0e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="eaf0e-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="eaf0e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="eaf0e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="eaf0e-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="eaf0e-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="eaf0e-110">Default Action</span></span>

<span data-ttu-id="eaf0e-111">Der Filter Graph-Manager hält das Diagramm an und startet es neu.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="eaf0e-112">Das Ereignis wird nicht an die Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf0e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaf0e-113">Remarks</span></span>

<span data-ttu-id="eaf0e-114">Wenn ein Filter eine Stichprobe in der Mitte eines Streams ablehnt, hält die Upstream-Pin keine Stichproben mehr an.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="eaf0e-115">Der Filter kann den Stream neu starten, indem dieses Ereignis gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="eaf0e-116">Beispielsweise verliert der audiorenderer möglicherweise den Zugriff auf das Audiogerät, da ein Videofenster den Fokus verliert.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="eaf0e-117">An diesem Punkt beginnt der audiorenderer mit dem ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="eaf0e-118">Wenn der Zugriff auf das Audiogerät wiedererlangt wird, sendet er dieses Ereignis, um den Audiodatenstrom neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="eaf0e-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf0e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaf0e-119">Requirements</span></span>



| <span data-ttu-id="eaf0e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaf0e-120">Requirement</span></span> | <span data-ttu-id="eaf0e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="eaf0e-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf0e-122">Header</span><span class="sxs-lookup"><span data-stu-id="eaf0e-122">Header</span></span><br/> | <dl> <span data-ttu-id="eaf0e-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf0e-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaf0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf0e-125">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="eaf0e-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="eaf0e-126">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="eaf0e-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Der Benutzer hat die Wiedergabe beendet.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361931"
---
# <a name="ec_userabort"></a><span data-ttu-id="dfb53-103">EC \_ userabort</span><span class="sxs-lookup"><span data-stu-id="dfb53-103">EC\_USERABORT</span></span>

<span data-ttu-id="dfb53-104">Der Benutzer hat die Wiedergabe beendet.</span><span class="sxs-lookup"><span data-stu-id="dfb53-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfb53-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfb53-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb53-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="dfb53-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dfb53-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="dfb53-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="dfb53-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="dfb53-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dfb53-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="dfb53-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="dfb53-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="dfb53-110">Default Action</span></span>

<span data-ttu-id="dfb53-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dfb53-111">None.</span></span> <span data-ttu-id="dfb53-112">Die Anwendung muss entscheiden, ob das Diagramm angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfb53-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb53-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfb53-113">Remarks</span></span>

<span data-ttu-id="dfb53-114">Dieser Ereignis Code signalisiert, dass der Benutzer die normale Graph-Wiedergabe beendet hat.</span><span class="sxs-lookup"><span data-stu-id="dfb53-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="dfb53-115">Beispielsweise senden Videorenderer dieses Ereignis, wenn der Benutzer das Videofenster schließt.</span><span class="sxs-lookup"><span data-stu-id="dfb53-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="dfb53-116">Nach dem Senden dieses Ereignisses sollte der Filter alle Beispiele ablehnen und keine [**EC \_ Repaint**](ec-repaint.md) -Ereignisse senden, bis der Filter beendet und zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="dfb53-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb53-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfb53-117">Requirements</span></span>



| <span data-ttu-id="dfb53-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfb53-118">Requirement</span></span> | <span data-ttu-id="dfb53-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dfb53-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb53-120">Header</span><span class="sxs-lookup"><span data-stu-id="dfb53-120">Header</span></span><br/> | <dl> <span data-ttu-id="dfb53-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb53-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb53-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfb53-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb53-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="dfb53-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="dfb53-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="dfb53-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





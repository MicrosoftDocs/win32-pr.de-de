---
description: Signalisiert, dass eine Medienquelle den Versuch, eine erneute Verbindung mit dem Server herzustellen, abgeschlossen hat.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Mereconnectend-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528268"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="7c694-103">Mereconnectend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7c694-103">MEReconnectEnd event</span></span>

<span data-ttu-id="7c694-104">Signalisiert, dass eine Medienquelle den Versuch, eine erneute Verbindung mit dem Server herzustellen, abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="7c694-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="7c694-105">Ausgelöst durch eine Medienquelle am Ende eines erneuten Verbindungsversuchs.</span><span class="sxs-lookup"><span data-stu-id="7c694-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="7c694-106">Die Netzwerkquelle löst dieses Ereignis aus, wenn es erneut eine Verbindung mit dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="7c694-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="7c694-107">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="7c694-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="7c694-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="7c694-108">Event values</span></span>

<span data-ttu-id="7c694-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="7c694-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7c694-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7c694-110">VARTYPE</span></span>              | <span data-ttu-id="7c694-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c694-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7c694-112">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="7c694-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7c694-113">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="7c694-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7c694-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c694-114">Requirements</span></span>



| <span data-ttu-id="7c694-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c694-115">Requirement</span></span> | <span data-ttu-id="7c694-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7c694-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c694-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c694-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c694-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c694-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c694-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c694-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c694-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c694-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c694-121">Header</span><span class="sxs-lookup"><span data-stu-id="7c694-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c694-122"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c694-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c694-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c694-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c694-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c694-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





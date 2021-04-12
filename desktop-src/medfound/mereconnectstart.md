---
description: Signalisiert, dass eine Medienquelle versucht, eine erneute Verbindung mit dem Server herzustellen.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Mereconnectstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130741"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="4568c-103">Mereconnectstart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="4568c-103">MEReconnectStart event</span></span>

<span data-ttu-id="4568c-104">Signalisiert, dass eine Medienquelle versucht, eine erneute Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4568c-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="4568c-105">Ausgelöst durch eine Medienquelle zu Beginn eines erneuten Verbindungsversuchs.</span><span class="sxs-lookup"><span data-stu-id="4568c-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="4568c-106">Die Netzwerkquelle löst dieses Ereignis aus, wenn versucht wird, erneut eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4568c-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="4568c-107">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="4568c-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="4568c-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="4568c-108">Event values</span></span>

<span data-ttu-id="4568c-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="4568c-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4568c-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4568c-110">VARTYPE</span></span>              | <span data-ttu-id="4568c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4568c-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4568c-112">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="4568c-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4568c-113">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="4568c-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4568c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4568c-114">Requirements</span></span>



| <span data-ttu-id="4568c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4568c-115">Requirement</span></span> | <span data-ttu-id="4568c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4568c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4568c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4568c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4568c-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4568c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4568c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4568c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4568c-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4568c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4568c-121">Header</span><span class="sxs-lookup"><span data-stu-id="4568c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4568c-122"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4568c-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4568c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4568c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4568c-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4568c-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





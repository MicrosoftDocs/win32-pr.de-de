---
description: Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358738"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="4ac87-103">EC- \_ loadstatus</span><span class="sxs-lookup"><span data-stu-id="4ac87-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="4ac87-104">Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.</span><span class="sxs-lookup"><span data-stu-id="4ac87-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ac87-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac87-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac87-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4ac87-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4ac87-107">Statuscode.</span><span class="sxs-lookup"><span data-stu-id="4ac87-107">Status code.</span></span> <span data-ttu-id="4ac87-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="4ac87-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4ac87-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4ac87-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4ac87-110">Keinen.</span><span class="sxs-lookup"><span data-stu-id="4ac87-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4ac87-111">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="4ac87-111">Default Action</span></span>

<span data-ttu-id="4ac87-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ac87-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac87-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ac87-113">Remarks</span></span>

<span data-ttu-id="4ac87-114">Der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter und der ältere [Windows Media-Quell](windows-media-source-filter.md) Filter Senden dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4ac87-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="4ac87-115">Der erste Ereignis Parameter hat einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4ac87-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="4ac87-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4ac87-116">Value</span></span>                        | <span data-ttu-id="4ac87-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ac87-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="4ac87-118">AM \_ loadstatus \_ geschlossen</span><span class="sxs-lookup"><span data-stu-id="4ac87-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="4ac87-119">Der Quell Filter hat die Datei geschlossen.</span><span class="sxs-lookup"><span data-stu-id="4ac87-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="4ac87-120">AM \_ loadstatus- \_ Verbindung</span><span class="sxs-lookup"><span data-stu-id="4ac87-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="4ac87-121">Der Quell Filter stellt eine Verbindung mit dem Server her.</span><span class="sxs-lookup"><span data-stu-id="4ac87-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="4ac87-122">AM \_ loadstatus \_ loadingdescr</span><span class="sxs-lookup"><span data-stu-id="4ac87-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="4ac87-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac87-123">Not used.</span></span>                                      |
| <span data-ttu-id="4ac87-124">AM \_ loadstatus \_ loadingmcast</span><span class="sxs-lookup"><span data-stu-id="4ac87-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="4ac87-125">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="4ac87-125">Not used</span></span>                                       |
| <span data-ttu-id="4ac87-126">AM \_ loadstatus \_ Suchen</span><span class="sxs-lookup"><span data-stu-id="4ac87-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="4ac87-127">Der Quell Filter sucht die angeforderten Daten.</span><span class="sxs-lookup"><span data-stu-id="4ac87-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="4ac87-128">AM \_ loadstatus \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="4ac87-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="4ac87-129">Der Quell Filter hat die Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4ac87-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="4ac87-130">AM \_ loadstatus \_ Öffnen</span><span class="sxs-lookup"><span data-stu-id="4ac87-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="4ac87-131">Der Quell Filter öffnet die Datei.</span><span class="sxs-lookup"><span data-stu-id="4ac87-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="4ac87-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ac87-132">Requirements</span></span>



| <span data-ttu-id="4ac87-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ac87-133">Requirement</span></span> | <span data-ttu-id="4ac87-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4ac87-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac87-135">Header</span><span class="sxs-lookup"><span data-stu-id="4ac87-135">Header</span></span><br/> | <dl> <span data-ttu-id="4ac87-136"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac87-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac87-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ac87-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac87-138">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="4ac87-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4ac87-139">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ac87-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





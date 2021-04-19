---
description: Wird gesendet, wenn eine Anwendung den WM-ASF-Writer-Filter zum Indizieren Windows Media Video Dateien verwendet.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356470"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="6ef84-103">EC_WMT_INDEX_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="6ef84-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="6ef84-104">Wird gesendet, wenn eine Anwendung den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter zum Indizieren Windows Media Video Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ef84-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ef84-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ef84-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef84-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6ef84-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6ef84-107">Kann eine der folgenden **WMT- \_ Status** Meldungen sein.</span><span class="sxs-lookup"><span data-stu-id="6ef84-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="6ef84-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef84-108">Value</span></span>                | <span data-ttu-id="6ef84-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ef84-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="6ef84-110">WMT \_ gestartet</span><span class="sxs-lookup"><span data-stu-id="6ef84-110">WMT\_STARTED</span></span>         | <span data-ttu-id="6ef84-111">Die Indizierung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="6ef84-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="6ef84-112">WMT \_ geschlossen</span><span class="sxs-lookup"><span data-stu-id="6ef84-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="6ef84-113">Die Indizierung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ef84-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="6ef84-114">WMT- \_ Index \_ Fortschritt</span><span class="sxs-lookup"><span data-stu-id="6ef84-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="6ef84-115">Die Indizierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ef84-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6ef84-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6ef84-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6ef84-117">Wenn *lParam1* WMT \_ Closed oder WMT \_ gestartet ist, dann ist *lParam2* gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6ef84-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="6ef84-118">Wenn *lParam1* den WMT- \_ Index Status \_ hat, ist *lParam2* ein **DWORD** , das den aktuellen Status als Prozentsatz der gesamten Downloadgröße angibt.</span><span class="sxs-lookup"><span data-stu-id="6ef84-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ef84-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ef84-119">Requirements</span></span>



| <span data-ttu-id="6ef84-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ef84-120">Requirement</span></span> | <span data-ttu-id="6ef84-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef84-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef84-122">Header</span><span class="sxs-lookup"><span data-stu-id="6ef84-122">Header</span></span><br/> | <dl> <span data-ttu-id="6ef84-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef84-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef84-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ef84-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef84-125">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="6ef84-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6ef84-126">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6ef84-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





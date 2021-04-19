---
description: Gibt die Zeitspanne an, die eine Komponente zum Verarbeiten der einzelnen Stichproben einnimmt.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353792"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="cd5df-103">EC- \_ Verarbeitungs \_ Latenz</span><span class="sxs-lookup"><span data-stu-id="cd5df-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="cd5df-104">Gibt die Zeitspanne an, die eine Komponente zum Verarbeiten der einzelnen Stichproben einnimmt.</span><span class="sxs-lookup"><span data-stu-id="cd5df-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd5df-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd5df-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd5df-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cd5df-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cd5df-107">(Konstante **Referenz \_ Zeit** \* ) die Zeitspanne für die Verarbeitung der einzelnen Stichproben in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="cd5df-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="cd5df-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cd5df-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cd5df-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="cd5df-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cd5df-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="cd5df-110">Default Action</span></span>

<span data-ttu-id="cd5df-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd5df-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd5df-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd5df-112">Remarks</span></span>

<span data-ttu-id="cd5df-113">Ein Präsentator für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR) kann diese Nachricht an den EVR senden, um den EVR über die Verarbeitungs Wartezeit des Presenter zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="cd5df-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd5df-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd5df-114">Requirements</span></span>



| <span data-ttu-id="cd5df-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd5df-115">Requirement</span></span> | <span data-ttu-id="cd5df-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5df-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5df-117">Header</span><span class="sxs-lookup"><span data-stu-id="cd5df-117">Header</span></span><br/> | <dl> <span data-ttu-id="cd5df-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd5df-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd5df-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd5df-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd5df-120">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="cd5df-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cd5df-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cd5df-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





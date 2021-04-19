---
description: Ein Plug & Play Gerät wurde entfernt oder wieder verfügbar.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367737"
---
# <a name="ec_device_lost"></a><span data-ttu-id="e5671-103">EC- \_ Gerät \_ verloren</span><span class="sxs-lookup"><span data-stu-id="e5671-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="e5671-104">Ein Plug & Play Gerät wurde entfernt oder wieder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5671-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5671-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5671-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5671-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e5671-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e5671-107">(**IUnknown** \* ) Ein Zeiger auf die **IUnknown** -Schnittstelle des Filters, der das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5671-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="e5671-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e5671-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e5671-109">0 (null), wenn das Gerät entfernt wurde, oder 1, wenn das Gerät wieder verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e5671-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e5671-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="e5671-110">Default Action</span></span>

<span data-ttu-id="e5671-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5671-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5671-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5671-112">Remarks</span></span>

<span data-ttu-id="e5671-113">Wenn das Gerät wieder verfügbar wird, ist der vorherige Status des Geräte Filters nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="e5671-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="e5671-114">Die Anwendung muss das Diagramm neu erstellen, damit das Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5671-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5671-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5671-115">Requirements</span></span>



| <span data-ttu-id="e5671-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5671-116">Requirement</span></span> | <span data-ttu-id="e5671-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e5671-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5671-118">Header</span><span class="sxs-lookup"><span data-stu-id="e5671-118">Header</span></span><br/> | <dl> <span data-ttu-id="e5671-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5671-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5671-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5671-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5671-121">Benachrichtigung zum Entfernen von Geräten</span><span class="sxs-lookup"><span data-stu-id="e5671-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="e5671-122">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="e5671-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e5671-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5671-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Signalisiert den Anfang aller weiterhin (PGC, Cell oder vobu).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368324"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="d9f30-103">EC- \_ DVD \_ weiterhin \_ on</span><span class="sxs-lookup"><span data-stu-id="d9f30-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="d9f30-104">Signalisiert den Anfang aller weiterhin (PGC, Cell oder vobu).</span><span class="sxs-lookup"><span data-stu-id="d9f30-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="d9f30-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9f30-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f30-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d9f30-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d9f30-107">Boolescher Wert (**boolescher** Wert), der angibt, ob Schaltflächen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d9f30-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="d9f30-108">NULL (0) gibt an, dass Schaltflächen verfügbar sind, sodass die [**IDvdControl2:: stilloff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) -Methode nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d9f30-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="d9f30-109">Eins (1) gibt an, dass keine Schaltflächen verfügbar sind, sodass **IDvdControl2:: stilloff** funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d9f30-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="d9f30-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d9f30-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d9f30-111">**DWORD** -Wert, der die Anzahl der Sekunden angibt, die noch zuletzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9f30-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="d9f30-112">0xFFFFFFFF gibt immer noch unendlich an, was bedeutet, bis der Benutzer auf eine Schaltfläche drückt, oder bis die Anwendung [**IDvdControl2:: stilloff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)aufruft.</span><span class="sxs-lookup"><span data-stu-id="d9f30-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9f30-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9f30-113">Remarks</span></span>

<span data-ttu-id="d9f30-114">Alle Kombinationen von Schaltflächen und sind immer noch möglich (Schaltflächen auf, bei denen immer noch angezeigt wird, Schaltflächen mit "nach unten", Schaltfläche "weiter", Schaltfläche "aus" und "nach</span><span class="sxs-lookup"><span data-stu-id="d9f30-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="d9f30-115">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d9f30-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f30-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9f30-116">Requirements</span></span>



| <span data-ttu-id="d9f30-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9f30-117">Requirement</span></span> | <span data-ttu-id="d9f30-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d9f30-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f30-119">Header</span><span class="sxs-lookup"><span data-stu-id="d9f30-119">Header</span></span><br/> | <dl> <span data-ttu-id="d9f30-120"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f30-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f30-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9f30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f30-122">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d9f30-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d9f30-123">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="d9f30-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d9f30-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9f30-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





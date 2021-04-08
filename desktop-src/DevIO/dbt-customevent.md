---
description: Das System sendet das DBT \_ CustomEvent-Geräte Ereignis, wenn ein Treiber definiertes benutzerdefiniertes Ereignis aufgetreten ist.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748361"
---
# <a name="dbt_customevent-event"></a><span data-ttu-id="e4b60-103">DBT \_ CustomEvent-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e4b60-103">DBT\_CUSTOMEVENT event</span></span>

<span data-ttu-id="e4b60-104">Das System sendet das DBT \_ CustomEvent-Geräte Ereignis, wenn ein Treiber definiertes benutzerdefiniertes Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e4b60-104">The system sends the DBT\_CUSTOMEVENT device event when a driver-defined custom event has occurred.</span></span>

<span data-ttu-id="e4b60-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ CustomEvent und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4b60-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CUSTOMEVENT and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="e4b60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b60-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e4b60-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b60-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="e4b60-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="e4b60-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="e4b60-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b60-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4b60-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e4b60-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4b60-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b60-112">Legen Sie auf DBT \_ CustomEvent fest.</span><span class="sxs-lookup"><span data-stu-id="e4b60-112">Set to DBT\_CUSTOMEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e4b60-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4b60-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b60-114">Ein Zeiger auf eine-Struktur, die das Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4b60-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="e4b60-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e4b60-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="e4b60-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e4b60-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b60-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4b60-117">Return value</span></span>

<span data-ttu-id="e4b60-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4b60-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b60-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4b60-119">Requirements</span></span>



| <span data-ttu-id="e4b60-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4b60-120">Requirement</span></span> | <span data-ttu-id="e4b60-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e4b60-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e4b60-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4b60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b60-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4b60-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="e4b60-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4b60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b60-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4b60-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e4b60-126">Header</span><span class="sxs-lookup"><span data-stu-id="e4b60-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b60-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b60-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b60-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4b60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b60-129">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e4b60-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="e4b60-130">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e4b60-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="e4b60-131">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="e4b60-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="e4b60-132">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="e4b60-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





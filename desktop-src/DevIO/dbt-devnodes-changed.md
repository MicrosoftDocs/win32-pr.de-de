---
description: Das System sendet das \_ geänderte Geräte Ereignis DBT Devnodes \_ , wenn ein Gerät dem System hinzugefügt oder daraus entfernt wurde. Anwendungen, die Listen von Geräten im System verwalten, sollten Ihre Listen aktualisieren.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126788"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="93ca1-104">Geändertes DBT- \_ Devnodes- \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="93ca1-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="93ca1-105">Das System sendet das \_ geänderte Geräte Ereignis DBT Devnodes \_ , wenn ein Gerät dem System hinzugefügt oder daraus entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="93ca1-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="93ca1-106">Anwendungen, die Listen von Geräten im System verwalten, sollten Ihre Listen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="93ca1-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="93ca1-107">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ Devnodes \_ geändert und *LPARAM* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93ca1-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="93ca1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93ca1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ca1-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="93ca1-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="93ca1-110">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="93ca1-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="93ca1-111">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="93ca1-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="93ca1-112">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="93ca1-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="93ca1-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93ca1-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93ca1-114">Legen Sie fest, dass DBT \_ Devnodes \_ geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="93ca1-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="93ca1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93ca1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93ca1-116">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="93ca1-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ca1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93ca1-117">Return value</span></span>

<span data-ttu-id="93ca1-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="93ca1-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93ca1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93ca1-119">Remarks</span></span>

<span data-ttu-id="93ca1-120">Es gibt keine zusätzlichen Informationen darüber, welches Gerät dem System hinzugefügt oder daraus entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="93ca1-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="93ca1-121">Anwendungen, für die weitere Informationen erforderlich sind, sollten sich mithilfe der [**registerdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Funktion für die Geräte Benachrichtigung registrieren.</span><span class="sxs-lookup"><span data-stu-id="93ca1-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ca1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93ca1-122">Requirements</span></span>



| <span data-ttu-id="93ca1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93ca1-123">Requirement</span></span> | <span data-ttu-id="93ca1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="93ca1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="93ca1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93ca1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93ca1-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="93ca1-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="93ca1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93ca1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93ca1-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93ca1-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="93ca1-129">Header</span><span class="sxs-lookup"><span data-stu-id="93ca1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ca1-130"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ca1-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ca1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93ca1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ca1-132">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="93ca1-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="93ca1-133">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="93ca1-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="93ca1-134">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="93ca1-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="93ca1-135">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="93ca1-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





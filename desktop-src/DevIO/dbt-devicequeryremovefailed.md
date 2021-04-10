---
description: Das System überträgt das DBT \_ devicequeryremovefailed-Geräte Ereignis, wenn eine Anforderung zum Entfernen eines Geräts oder eines Mediums abgebrochen wurde.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861111"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="19f58-103">DBT \_ devicequeryremovefailed-Ereignis</span><span class="sxs-lookup"><span data-stu-id="19f58-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="19f58-104">Das System überträgt das DBT \_ devicequeryremovefailed-Geräte Ereignis, wenn eine Anforderung zum Entfernen eines Geräts oder eines Mediums abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="19f58-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="19f58-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ devicequeryremovefailed und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19f58-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="19f58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19f58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f58-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="19f58-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="19f58-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="19f58-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="19f58-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="19f58-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="19f58-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="19f58-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="19f58-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19f58-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19f58-112">Auf DBT \_ devicequeryremovefailed festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19f58-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="19f58-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19f58-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19f58-114">Ein Zeiger auf eine-Struktur, die das Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="19f58-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="19f58-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="19f58-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="19f58-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="19f58-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f58-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19f58-117">Return value</span></span>

<span data-ttu-id="19f58-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="19f58-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="19f58-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19f58-119">Examples</span></span>

<span data-ttu-id="19f58-120">Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="19f58-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19f58-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19f58-121">Requirements</span></span>



| <span data-ttu-id="19f58-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19f58-122">Requirement</span></span> | <span data-ttu-id="19f58-123">Wert</span><span class="sxs-lookup"><span data-stu-id="19f58-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19f58-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19f58-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19f58-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="19f58-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="19f58-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19f58-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19f58-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19f58-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="19f58-128">Header</span><span class="sxs-lookup"><span data-stu-id="19f58-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f58-129"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f58-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19f58-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f58-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f58-131">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="19f58-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="19f58-132">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="19f58-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="19f58-133">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="19f58-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="19f58-134">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="19f58-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





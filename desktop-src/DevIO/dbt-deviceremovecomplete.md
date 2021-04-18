---
description: Das System überträgt das DBT \_ deviceremovecomplete-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums physisch entfernt wurde.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344361"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="afe03-103">DBT \_ deviceremovecomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="afe03-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="afe03-104">Das System überträgt das DBT \_ deviceremovecomplete-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums physisch entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="afe03-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="afe03-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ deviceremovecomplete und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="afe03-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="afe03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afe03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe03-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="afe03-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="afe03-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="afe03-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="afe03-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="afe03-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="afe03-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="afe03-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="afe03-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afe03-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afe03-112">Auf DBT \_ deviceremovecomplete festgelegt</span><span class="sxs-lookup"><span data-stu-id="afe03-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="afe03-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afe03-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afe03-114">Ein Zeiger auf eine-Struktur, die das entfernte Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="afe03-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="afe03-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="afe03-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="afe03-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="afe03-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe03-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afe03-117">Return value</span></span>

<span data-ttu-id="afe03-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="afe03-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="afe03-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afe03-119">Remarks</span></span>

<span data-ttu-id="afe03-120">Das System sendet möglicherweise eine DBT \_ deviceremovecomplete-Nachricht, ohne entsprechende [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -und [DBT \_ deviceremovepend](dbt-deviceremovepending.md) -Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="afe03-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="afe03-121">In solchen Fällen müssen die Anwendungen und Treiber nach dem Verlust des Geräts so optimal wie möglich wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="afe03-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="afe03-122">Wenn Medien entfernt werden, ist der Typ des eintreffenden Geräts ein Volume (der **dbch \_ den DeviceType "** -Member ist DBT \_ \_ devypvolume), und die Änderung wirkt sich auf das Medium aus (der **dbcv- \_ Flags** -Member ist dbtf- \_ Medien).</span><span class="sxs-lookup"><span data-stu-id="afe03-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="afe03-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afe03-123">Examples</span></span>

<span data-ttu-id="afe03-124">Ein Beispiel finden Sie unter [Erkennen von Medien Einfügevorgängen oder entfernen](detecting-media-insertion-or-removal.md) oder [Verarbeiten einer Anforderung zum Entfernen eines Geräts](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="afe03-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afe03-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afe03-125">Requirements</span></span>



| <span data-ttu-id="afe03-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afe03-126">Requirement</span></span> | <span data-ttu-id="afe03-127">Wert</span><span class="sxs-lookup"><span data-stu-id="afe03-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="afe03-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afe03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="afe03-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="afe03-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="afe03-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afe03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="afe03-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afe03-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="afe03-132">Header</span><span class="sxs-lookup"><span data-stu-id="afe03-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="afe03-133"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="afe03-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe03-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afe03-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe03-135">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="afe03-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="afe03-136">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="afe03-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="afe03-137">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="afe03-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="afe03-138">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="afe03-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





---
description: Das System überträgt das DBT \_ deviceremovepend-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums entfernt wird und nicht mehr zur Verwendung verfügbar ist.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: DBT_DEVICEREMOVEPENDING-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126793"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="013e0-103">DBT \_ deviceremovepending-Ereignis</span><span class="sxs-lookup"><span data-stu-id="013e0-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="013e0-104">Das System überträgt das DBT \_ deviceremovepend-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums entfernt wird und nicht mehr zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="013e0-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="013e0-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ deviceremovepending und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="013e0-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="013e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="013e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="013e0-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="013e0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="013e0-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="013e0-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="013e0-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="013e0-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="013e0-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="013e0-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="013e0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="013e0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="013e0-112">Legen Sie auf DBT \_ deviceremovepending fest.</span><span class="sxs-lookup"><span data-stu-id="013e0-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="013e0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="013e0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="013e0-114">Ein Zeiger auf eine-Struktur, die das Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="013e0-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="013e0-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="013e0-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="013e0-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="013e0-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="013e0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="013e0-117">Return value</span></span>

<span data-ttu-id="013e0-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="013e0-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="013e0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="013e0-119">Remarks</span></span>

<span data-ttu-id="013e0-120">Das System sendet möglicherweise eine DBT \_ deviceremovepend-Nachricht, ohne eine entsprechende [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="013e0-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="013e0-121">In solchen Fällen müssen die Anwendungen und Treiber nach dem Verlust des Geräts so optimal wie möglich wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="013e0-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="013e0-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="013e0-122">Examples</span></span>

<span data-ttu-id="013e0-123">Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="013e0-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="013e0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="013e0-124">Requirements</span></span>



| <span data-ttu-id="013e0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="013e0-125">Requirement</span></span> | <span data-ttu-id="013e0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="013e0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="013e0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="013e0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="013e0-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="013e0-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="013e0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="013e0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="013e0-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="013e0-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="013e0-131">Header</span><span class="sxs-lookup"><span data-stu-id="013e0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="013e0-132"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="013e0-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="013e0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="013e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013e0-134">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="013e0-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="013e0-135">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="013e0-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="013e0-136">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="013e0-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="013e0-137">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="013e0-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





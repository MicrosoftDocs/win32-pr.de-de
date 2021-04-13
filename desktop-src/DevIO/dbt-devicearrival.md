---
description: Das System überträgt das DBT \_ devicearrival-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums eingefügt wurde und verfügbar wird.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: DBT_DEVICEARRIVAL-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483278"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="b4f16-103">DBT \_ devicearrival-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b4f16-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="b4f16-104">Das System überträgt das DBT \_ devicearrival-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums eingefügt wurde und verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="b4f16-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="b4f16-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ devicearrival und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b4f16-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="b4f16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f16-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b4f16-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f16-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="b4f16-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="b4f16-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="b4f16-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f16-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b4f16-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b4f16-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4f16-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f16-112">Legen Sie auf DBT \_ devicearrival fest.</span><span class="sxs-lookup"><span data-stu-id="b4f16-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="b4f16-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4f16-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f16-114">Ein Zeiger auf eine-Struktur, die das eingefügte Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b4f16-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="b4f16-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b4f16-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="b4f16-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b4f16-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f16-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4f16-117">Return value</span></span>

<span data-ttu-id="b4f16-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="b4f16-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4f16-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4f16-119">Remarks</span></span>

<span data-ttu-id="b4f16-120">Wenn Medien eingefügt werden, ist der Typ des eintreffenden Geräts ein Volume (der **dbch \_ den DeviceType "** -Member ist DBT \_ \_ devypvolume), und die Änderung wirkt sich auf das Medium aus (der **dbcv- \_ Flags** -Member ist dbtf- \_ Medien).</span><span class="sxs-lookup"><span data-stu-id="b4f16-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="b4f16-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4f16-121">Examples</span></span>

<span data-ttu-id="b4f16-122">Ein Beispiel finden Sie unter [Erkennen von Medien einfügen oder entfernen](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="b4f16-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f16-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4f16-123">Requirements</span></span>



| <span data-ttu-id="b4f16-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4f16-124">Requirement</span></span> | <span data-ttu-id="b4f16-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b4f16-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4f16-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4f16-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f16-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4f16-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="b4f16-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4f16-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f16-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4f16-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="b4f16-130">Header</span><span class="sxs-lookup"><span data-stu-id="b4f16-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f16-131"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f16-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f16-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4f16-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f16-133">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b4f16-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="b4f16-134">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b4f16-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="b4f16-135">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="b4f16-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="b4f16-136">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="b4f16-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





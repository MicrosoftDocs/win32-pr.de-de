---
description: Das System überträgt das DBT- \_ Geräte Ereignis "Geräte spezifisches Ereignis", wenn ein Geräte spezifisches Ereignis auftritt.
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: DBT_DEVICETYPESPECIFIC-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d7820f5769c6edd3a48b58073b55a911dae862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861108"
---
# <a name="dbt_devicetypespecific-event"></a><span data-ttu-id="a9bcd-103">DBT- \_ Ereignis vom typvicetypespecific</span><span class="sxs-lookup"><span data-stu-id="a9bcd-103">DBT\_DEVICETYPESPECIFIC event</span></span>

<span data-ttu-id="a9bcd-104">Das System überträgt das DBT- \_ Geräte Ereignis "Geräte spezifisches Ereignis", wenn ein Geräte spezifisches Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-104">The system broadcasts the DBT\_DEVICETYPESPECIFIC device event when a device-specific event occurs.</span></span>

<span data-ttu-id="a9bcd-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ devicetypespecific und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICETYPESPECIFIC and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="a9bcd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9bcd-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a9bcd-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcd-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="a9bcd-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="a9bcd-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="a9bcd-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcd-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a9bcd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9bcd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcd-112">Legen Sie auf DBT-Geräte Wert fest \_ .</span><span class="sxs-lookup"><span data-stu-id="a9bcd-112">Set to DBT\_DEVICETYPESPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="a9bcd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9bcd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcd-114">Ein Zeiger auf eine-Struktur, die das Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="a9bcd-115">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="a9bcd-116">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9bcd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9bcd-117">Return value</span></span>

<span data-ttu-id="a9bcd-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bcd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9bcd-119">Requirements</span></span>



| <span data-ttu-id="a9bcd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9bcd-120">Requirement</span></span> | <span data-ttu-id="a9bcd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a9bcd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a9bcd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9bcd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9bcd-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9bcd-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="a9bcd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9bcd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9bcd-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9bcd-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a9bcd-126">Header</span><span class="sxs-lookup"><span data-stu-id="a9bcd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9bcd-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9bcd-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9bcd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9bcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bcd-129">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a9bcd-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="a9bcd-130">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a9bcd-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="a9bcd-131">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="a9bcd-132">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





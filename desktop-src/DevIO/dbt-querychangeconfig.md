---
description: Das System überträgt das DBT \_ querychangeconfig-Geräte Ereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) anzufordern. Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523651"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="e8f48-104">DBT \_ querychangeconfig-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e8f48-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="e8f48-105">Das System überträgt das DBT \_ querychangeconfig-Geräte Ereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e8f48-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="e8f48-106">Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.</span><span class="sxs-lookup"><span data-stu-id="e8f48-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="e8f48-107">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ querychangeconfig und *LPARAM* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e8f48-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="e8f48-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8f48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8f48-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e8f48-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f48-110">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="e8f48-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="e8f48-111">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="e8f48-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f48-112">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e8f48-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8f48-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8f48-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f48-114">Legen Sie auf DBT \_ querychangeconfig fest.</span><span class="sxs-lookup"><span data-stu-id="e8f48-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="e8f48-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8f48-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f48-116">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="e8f48-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8f48-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8f48-117">Return value</span></span>

<span data-ttu-id="e8f48-118">Geben Sie **true** zurück, um die Berechtigung zum Ändern der Konfiguration zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="e8f48-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="e8f48-119">Rückgabe \_ der Broadcast Abfrage \_ ablehnen, um die Berechtigung zum Ändern der Konfiguration abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="e8f48-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f48-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8f48-120">Requirements</span></span>



| <span data-ttu-id="e8f48-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8f48-121">Requirement</span></span> | <span data-ttu-id="e8f48-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e8f48-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e8f48-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8f48-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f48-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8f48-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="e8f48-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8f48-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f48-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8f48-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e8f48-127">Header</span><span class="sxs-lookup"><span data-stu-id="e8f48-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8f48-128"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8f48-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8f48-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8f48-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f48-130">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e8f48-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="e8f48-131">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e8f48-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="e8f48-132">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="e8f48-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





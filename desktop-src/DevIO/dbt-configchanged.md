---
description: Das System überträgt das DBT \_ ConfigChanged-Geräte Ereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andocken oder abdostems geändert hat. Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem aktuellen Konfigurationsschlüssel HKEY speichert, \_ \_ sollte die Daten aktualisieren.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214152"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="5122f-104">DBT \_ ConfigChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5122f-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="5122f-105">Das System überträgt das DBT \_ ConfigChanged-Geräte Ereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andocken oder abdostems geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5122f-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="5122f-106">Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem aktuellen Konfigurationsschlüssel HKEY speichert, \_ \_ sollte die Daten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5122f-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="5122f-107">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ ConfigChanged und *LPARAM* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5122f-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="5122f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5122f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5122f-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5122f-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5122f-110">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="5122f-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-111">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="5122f-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="5122f-112">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5122f-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5122f-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5122f-114">Auf DBT \_ ConfigChanged festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5122f-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5122f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5122f-116">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="5122f-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5122f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5122f-117">Return value</span></span>

<span data-ttu-id="5122f-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="5122f-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5122f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5122f-119">Requirements</span></span>



| <span data-ttu-id="5122f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5122f-120">Requirement</span></span> | <span data-ttu-id="5122f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5122f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5122f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5122f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5122f-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5122f-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="5122f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5122f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5122f-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5122f-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5122f-126">Header</span><span class="sxs-lookup"><span data-stu-id="5122f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5122f-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5122f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5122f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5122f-129">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5122f-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="5122f-130">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5122f-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="5122f-131">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="5122f-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





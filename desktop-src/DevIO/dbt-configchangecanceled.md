---
description: Das System überträgt das DBT \_ configchangeabgeb Rochen-Geräte Ereignis, wenn eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) abgebrochen wurde.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: DBT_CONFIGCHANGECANCELED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861115"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="f67ae-103">DBT \_ configchangeabgeb Rochen-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f67ae-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="f67ae-104">Das System überträgt das DBT \_ configchangeabgeb Rochen-Geräte Ereignis, wenn eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="f67ae-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="f67ae-105">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ configchangeabgeb Rochen und *LPARAM* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f67ae-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="f67ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f67ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67ae-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f67ae-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f67ae-108">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="f67ae-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f67ae-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="f67ae-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f67ae-110">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f67ae-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f67ae-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f67ae-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f67ae-112">Legen Sie DBT \_ configchangeabgeb Rochen fest.</span><span class="sxs-lookup"><span data-stu-id="f67ae-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="f67ae-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f67ae-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f67ae-114">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="f67ae-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67ae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f67ae-115">Return value</span></span>

<span data-ttu-id="f67ae-116">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ae-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f67ae-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f67ae-117">Requirements</span></span>



| <span data-ttu-id="f67ae-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f67ae-118">Requirement</span></span> | <span data-ttu-id="f67ae-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f67ae-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f67ae-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f67ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f67ae-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f67ae-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f67ae-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f67ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f67ae-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f67ae-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f67ae-124">Header</span><span class="sxs-lookup"><span data-stu-id="f67ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f67ae-125"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f67ae-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f67ae-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f67ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67ae-127">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="f67ae-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f67ae-128">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="f67ae-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f67ae-129">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="f67ae-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





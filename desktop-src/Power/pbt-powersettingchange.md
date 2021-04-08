---
description: Das Energie Einstellungs Änderungs Ereignis wurde mit einer WM- \_ powerbroadcast-Fenster Meldung oder in einem handlerex-Benachrichtigungs Rückruf für Dienste gesendet.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: PBT_POWERSETTINGCHANGE-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865068"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="21cbd-103">PBT- \_ powersettingchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="21cbd-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="21cbd-104">Das Energie Einstellungs Änderungs Ereignis wurde mit einer [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Fenster Meldung oder in einem [**handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Benachrichtigungs Rückruf für Dienste gesendet.</span><span class="sxs-lookup"><span data-stu-id="21cbd-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="21cbd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="21cbd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cbd-106">*HWND*</span><span class="sxs-lookup"><span data-stu-id="21cbd-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="21cbd-107">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="21cbd-107">A handle to window.</span></span>

<span data-ttu-id="21cbd-108"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="21cbd-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="21cbd-109">Wert</span><span class="sxs-lookup"><span data-stu-id="21cbd-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="21cbd-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21cbd-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="21cbd-111"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="21cbd-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="21cbd-112">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="21cbd-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="21cbd-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="21cbd-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="21cbd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="21cbd-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="21cbd-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21cbd-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="21cbd-116"><dt>**PBT \_ Powersettingchange**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="21cbd-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="21cbd-117">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="21cbd-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="21cbd-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21cbd-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21cbd-119">Zeiger auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.</span><span class="sxs-lookup"><span data-stu-id="21cbd-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cbd-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21cbd-120">Return value</span></span>

<span data-ttu-id="21cbd-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="21cbd-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21cbd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21cbd-122">Requirements</span></span>



| <span data-ttu-id="21cbd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21cbd-123">Requirement</span></span> | <span data-ttu-id="21cbd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="21cbd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cbd-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21cbd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21cbd-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21cbd-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21cbd-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21cbd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21cbd-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21cbd-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21cbd-129">Header</span><span class="sxs-lookup"><span data-stu-id="21cbd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21cbd-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="21cbd-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21cbd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21cbd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cbd-132">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="21cbd-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="21cbd-133">**Handlerex**</span><span class="sxs-lookup"><span data-stu-id="21cbd-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="21cbd-134">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="21cbd-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="21cbd-135">**powerbroadcast- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="21cbd-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 


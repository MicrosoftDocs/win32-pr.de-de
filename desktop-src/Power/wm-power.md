---
description: Benachrichtigt Anwendungen, dass das System, üblicherweise ein Akku gesteuerter PC, im Begriff ist, in einen angehaltenen Modus zu wechseln.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: WM_POWER Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359036"
---
# <a name="wm_power-message"></a><span data-ttu-id="1e2eb-103">\_Power Message-WM</span><span class="sxs-lookup"><span data-stu-id="1e2eb-103">WM\_POWER message</span></span>

<span data-ttu-id="1e2eb-104">Benachrichtigt Anwendungen, dass das System, üblicherweise ein Akku gesteuerter PC, im Begriff ist, in einen angehaltenen Modus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="1e2eb-105">Die **WM- \_ Strom** Meldung ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="1e2eb-106">Sie wird nur für die Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="1e2eb-107">Anwendungen sollten die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="1e2eb-108">Ein Fenster empfängt diese Meldung über seine **WindowProc** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="1e2eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e2eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2eb-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1e2eb-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2eb-111">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="1e2eb-112">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="1e2eb-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2eb-113">Der **WM- \_ Strom** Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1e2eb-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e2eb-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2eb-115">Die Strom Ereignis Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-115">The power-event notification.</span></span> <span data-ttu-id="1e2eb-116">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1e2eb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1e2eb-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="1e2eb-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e2eb-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="1e2eb-119"><dt>**PWR \_ criticalresume**</dt></span><span class="sxs-lookup"><span data-stu-id="1e2eb-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="1e2eb-120">Gibt an, dass das System den Vorgang nach dem Wechsel in den Modus "angehalten" fortsetzt, ohne zuerst eine **PWR \_ suspendrequest** -Benachrichtigungs Meldung an die Anwendung zu senden</span><span class="sxs-lookup"><span data-stu-id="1e2eb-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="1e2eb-121">Eine Anwendung sollte alle notwendigen Wiederherstellungs Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="1e2eb-122"><dt>**PWR \_ suspendrequest**</dt></span><span class="sxs-lookup"><span data-stu-id="1e2eb-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="1e2eb-123">Gibt an, dass das System in den Modus "angehalten" versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="1e2eb-124"><dt>**PWR \_ suspendresume**</dt></span><span class="sxs-lookup"><span data-stu-id="1e2eb-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="1e2eb-125">Gibt an, dass das System den Vorgang fortsetzt, nachdem der angehaltene Modus in den normalen Zustand versetzt wurde. das System überträgt eine **PWR \_ suspendrequest** -Benachrichtigungs Meldung an die Anwendung, bevor das System angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="1e2eb-126">Eine Anwendung sollte alle notwendigen Wiederherstellungs Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1e2eb-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e2eb-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2eb-128">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2eb-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e2eb-129">Return value</span></span>

<span data-ttu-id="1e2eb-130">Der Wert, der von einer Anwendung zurückgegeben wird, hängt vom Wert des *wParam* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="1e2eb-131">Wenn " *wParam* " **PWR \_ suspendrequest** ist, kann der Rückgabewert **PWR \_ nicht** verhindern, dass das System in den Zustand "angehalten" wechselt; andernfalls ist es **PWR \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="1e2eb-132">Wenn " *wParam* " **PWR \_ suspendresume** oder **PWR \_ criticalresume** ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1e2eb-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2eb-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e2eb-133">Remarks</span></span>

<span data-ttu-id="1e2eb-134">Diese Meldung wird nur an eine Anwendung übertragen, die auf einem System ausgeführt wird, das der Spezifikation "Basic Input/Output System (FIM) für die erweiterte Energie Verwaltung (Basic Input/Output System)" entspricht.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="1e2eb-135">Die Meldung wird vom Energie Verwaltungs Treiber an jedes Fenster gesendet, das von der **EnumWindows** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="1e2eb-136">Der angehaltene Modus ist der Status, in dem die größte Menge an Energieeinsparungen auftritt, aber alle operativen Daten und Parameter bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="1e2eb-137">RAM-Inhalte (Random Access Memory) werden beibehalten, aber viele Geräte sind wahrscheinlich ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="1e2eb-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2eb-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e2eb-138">Requirements</span></span>



| <span data-ttu-id="1e2eb-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e2eb-139">Requirement</span></span> | <span data-ttu-id="1e2eb-140">Wert</span><span class="sxs-lookup"><span data-stu-id="1e2eb-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2eb-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e2eb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2eb-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e2eb-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e2eb-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e2eb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2eb-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e2eb-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e2eb-145">Header</span><span class="sxs-lookup"><span data-stu-id="1e2eb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2eb-146"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1e2eb-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2eb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e2eb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2eb-148">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="1e2eb-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 





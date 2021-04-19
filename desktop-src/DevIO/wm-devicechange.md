---
description: Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581502"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="95fa3-103">WM \_ DEVICECHANGE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95fa3-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="95fa3-104">Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.</span><span class="sxs-lookup"><span data-stu-id="95fa3-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="95fa3-105">Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95fa3-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="95fa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95fa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fa3-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="95fa3-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="95fa3-108">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="95fa3-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="95fa3-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="95fa3-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="95fa3-110">Der **WM \_ DEVICECHANGE-Bezeichner.**</span><span class="sxs-lookup"><span data-stu-id="95fa3-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="95fa3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95fa3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95fa3-112">Das aufgetretene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="95fa3-112">The event that has occurred.</span></span> <span data-ttu-id="95fa3-113">Dieser Parameter kann einer der folgenden Werte aus der Dbt.h-Headerdatei sein.</span><span class="sxs-lookup"><span data-stu-id="95fa3-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="95fa3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="95fa3-114">Value</span></span> | <span data-ttu-id="95fa3-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95fa3-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="95fa3-116">**[DBT \_ DEVNODES \_ GEÄNDERT](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="95fa3-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="95fa3-117">0x0007</span></span> | <span data-ttu-id="95fa3-118">Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="95fa3-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="95fa3-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="95fa3-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="95fa3-120">0x0017</span></span> | <span data-ttu-id="95fa3-121">Die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="95fa3-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="95fa3-122">**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="95fa3-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="95fa3-123">0x0018</span></span> | <span data-ttu-id="95fa3-124">Die aktuelle Konfiguration wurde aufgrund eines Andocks oder Abdockens geändert.</span><span class="sxs-lookup"><span data-stu-id="95fa3-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="95fa3-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="95fa3-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="95fa3-126">0x0019</span></span> | <span data-ttu-id="95fa3-127">Eine Anforderung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95fa3-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="95fa3-128">**[DBT \_ DEVICEARRARRARR](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="95fa3-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="95fa3-129">0x8000</span></span> | <span data-ttu-id="95fa3-130">Ein Gerät oder Medienteil wurde eingefügt und ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95fa3-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="95fa3-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="95fa3-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="95fa3-132">0x8001</span></span> | <span data-ttu-id="95fa3-133">Die Berechtigung zum Entfernen eines Geräts oder Medienstücks wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="95fa3-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="95fa3-134">Jede Anwendung kann diese Anforderung verweigern und die Entfernung abbrechen.</span><span class="sxs-lookup"><span data-stu-id="95fa3-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="95fa3-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="95fa3-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="95fa3-136">0x8002</span></span> | <span data-ttu-id="95fa3-137">Eine Anforderung zum Entfernen eines Geräts oder Medienstücks wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95fa3-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="95fa3-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="95fa3-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="95fa3-139">0x8003</span></span> | <span data-ttu-id="95fa3-140">Ein Gerät oder Medienteil wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="95fa3-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="95fa3-141">Kann nicht verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="95fa3-141">Cannot be denied.</span></span> |
| <span data-ttu-id="95fa3-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="95fa3-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="95fa3-143">0x8004</span></span> | <span data-ttu-id="95fa3-144">Ein Gerät oder Medienteil wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="95fa3-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="95fa3-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="95fa3-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="95fa3-146">0x8005</span></span> | <span data-ttu-id="95fa3-147">Ein gerätespezifisches Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="95fa3-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="95fa3-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="95fa3-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="95fa3-149">0x8006</span></span> | <span data-ttu-id="95fa3-150">Ein benutzerdefiniertes Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="95fa3-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="95fa3-151">**[DBT \_ USERDEFINED](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="95fa3-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="95fa3-152">0xffff</span><span class="sxs-lookup"><span data-stu-id="95fa3-152">0xFFFF</span></span> | <span data-ttu-id="95fa3-153">Die Bedeutung dieser Nachricht ist benutzerdefiniert.</span><span class="sxs-lookup"><span data-stu-id="95fa3-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="95fa3-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95fa3-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95fa3-155">Ein Zeiger auf eine -Struktur, die ereignisspezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="95fa3-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="95fa3-156">Das Format hängt vom Wert des *wParam-Parameters* ab.</span><span class="sxs-lookup"><span data-stu-id="95fa3-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="95fa3-157">Weitere Informationen finden Sie in der Dokumentation für jedes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="95fa3-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fa3-158">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95fa3-158">Return value</span></span>

<span data-ttu-id="95fa3-159">Gibt **TRUE** zurück, um die Anforderung zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="95fa3-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="95fa3-160">Geben Sie **BROADCAST \_ QUERY \_ DENY** zurück, um die Anforderung zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="95fa3-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="95fa3-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95fa3-161">Remarks</span></span>

<span data-ttu-id="95fa3-162">Für Geräte, die softwarekontrollierbare Features wie z. B. Einschleien und Sperren bieten, sendet das System in der Regel eine [DBT \_ DEVICEREMOVEPENDING-Nachricht,](dbt-deviceremovepending.md) damit Anwendungen und Gerätetreiber die Verwendung des Geräts ordnungsgemäß beenden können.</span><span class="sxs-lookup"><span data-stu-id="95fa3-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="95fa3-163">Wenn das System ein Gerät entfernt, sendet es möglicherweise keine [DBT \_ DEVICEQUERYREMOVE-Nachricht,](dbt-devicequeryremove.md) bevor dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="95fa3-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fa3-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95fa3-164">Requirements</span></span>

| <span data-ttu-id="95fa3-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95fa3-165">Requirement</span></span> | <span data-ttu-id="95fa3-166">Wert</span><span class="sxs-lookup"><span data-stu-id="95fa3-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fa3-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95fa3-167">Minimum supported client</span></span> | <span data-ttu-id="95fa3-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="95fa3-168">Windows XP</span></span> |
| <span data-ttu-id="95fa3-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95fa3-169">Minimum supported server</span></span> | <span data-ttu-id="95fa3-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95fa3-170">Windows Server 2003</span></span>|
| <span data-ttu-id="95fa3-171">Header</span><span class="sxs-lookup"><span data-stu-id="95fa3-171">Header</span></span> | <dl> <span data-ttu-id="95fa3-172"><dt>Winuser.h (einschließlich Windows.h oder Dbt.h)</dt></span><span class="sxs-lookup"><span data-stu-id="95fa3-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="95fa3-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95fa3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fa3-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="95fa3-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="95fa3-175">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="95fa3-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="95fa3-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="95fa3-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="95fa3-177">DBT \_ DEVICECONTEXTVAL</span><span class="sxs-lookup"><span data-stu-id="95fa3-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="95fa3-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="95fa3-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="95fa3-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="95fa3-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="95fa3-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="95fa3-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="95fa3-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="95fa3-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="95fa3-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="95fa3-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="95fa3-183">DBT \_ DEVNODES \_ GEÄNDERT</span><span class="sxs-lookup"><span data-stu-id="95fa3-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="95fa3-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="95fa3-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="95fa3-185">DBT \_ USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="95fa3-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

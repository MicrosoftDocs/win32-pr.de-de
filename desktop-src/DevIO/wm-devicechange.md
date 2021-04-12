---
description: Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393029"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="8792c-103">WM- \_ devicechange-Meldung</span><span class="sxs-lookup"><span data-stu-id="8792c-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="8792c-104">Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.</span><span class="sxs-lookup"><span data-stu-id="8792c-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="8792c-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8792c-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="8792c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8792c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8792c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8792c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8792c-108">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="8792c-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="8792c-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="8792c-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8792c-110">Der **WM- \_ devicechange** -Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="8792c-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8792c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8792c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8792c-112">Das Ereignis, das aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8792c-112">The event that has occurred.</span></span> <span data-ttu-id="8792c-113">Bei diesem Parameter kann es sich um einen der folgenden Werte aus der DBT. h-Header Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="8792c-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="8792c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8792c-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="8792c-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8792c-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="8792c-116"><dt>**[DBT \_ Configchangeabgeb Rochen](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="8792c-117">Eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8792c-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="8792c-118"><dt>**[DBT \_ ConfigChanged](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="8792c-119">Die aktuelle Konfiguration wurde aufgrund eines Andocken oder Abdocken geändert.</span><span class="sxs-lookup"><span data-stu-id="8792c-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="8792c-120"><dt>**[DBT \_ CustomEvent](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="8792c-121">Ein benutzerdefiniertes Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8792c-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="8792c-122"><dt>**[DBT \_ Devicearrival](dbt-devicearrival.md)**</dt> <dt>0X8000</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="8792c-123">Ein Gerät oder ein Teil des Mediums wurde eingefügt und ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8792c-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="8792c-124"><dt>**[DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="8792c-125">Die Berechtigung zum Entfernen eines Geräts oder eines Mediums wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="8792c-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="8792c-126">Jede Anwendung kann diese Anforderung verweigern und das Entfernen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="8792c-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="8792c-127"><dt>**[DBT \_ Devicequeryremovefailed](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="8792c-128">Eine Anforderung zum Entfernen eines Geräts oder eines Mediums wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8792c-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="8792c-129"><dt>**[DBT \_ Deviceremovecomplete](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="8792c-130">Ein Gerät oder ein Medium wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="8792c-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="8792c-131"><dt>**[DBT \_ Deviceremovepending](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="8792c-132">Ein Gerät oder ein Teil des Mediums wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="8792c-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="8792c-133">Kann nicht verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="8792c-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="8792c-134"><dt>**[DBT \_ Geräte-/linientypespecific](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="8792c-135">Ein Geräte spezifisches Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8792c-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="8792c-136"><dt>**[DBT \_ Devnodes \_ geändert](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="8792c-137">Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="8792c-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="8792c-138"><dt>**[DBT \_ Querychangeconfig](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="8792c-139">Die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="8792c-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="8792c-140"><dt>**[DBT \_ Benutzerdefinierter](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="8792c-141">Die Bedeutung dieser Meldung ist Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="8792c-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="8792c-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8792c-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8792c-143">Ein Zeiger auf eine-Struktur, die ereignisspezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="8792c-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="8792c-144">Das Format hängt vom Wert des *wParam* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="8792c-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="8792c-145">Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="8792c-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8792c-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8792c-146">Return value</span></span>

<span data-ttu-id="8792c-147">Gibt " **true** " zurück, um die Anforderung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="8792c-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="8792c-148">Rückgabe der **Übertragungs \_ Abfrage \_ ablehnen** , um die Anforderung zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="8792c-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="8792c-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8792c-149">Remarks</span></span>

<span data-ttu-id="8792c-150">Bei Geräten, die softwaregesteuerte Features anbieten (z. b. auswerfen und Sperren), sendet das System in der Regel eine [DBT \_ deviceremovepend](dbt-deviceremovepending.md) -Nachricht, damit Anwendungen und Gerätetreiber ihre Verwendung des Geräts ordnungsgemäß beenden können.</span><span class="sxs-lookup"><span data-stu-id="8792c-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="8792c-151">Wenn das System zwangsweise ein Gerät entfernt, sendet es möglicherweise keine [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8792c-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="8792c-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8792c-152">Requirements</span></span>



| <span data-ttu-id="8792c-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8792c-153">Requirement</span></span> | <span data-ttu-id="8792c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="8792c-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8792c-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8792c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8792c-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8792c-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="8792c-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8792c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8792c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8792c-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="8792c-159">Header</span><span class="sxs-lookup"><span data-stu-id="8792c-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8792c-160"><dt>Winuser. h (Include Windows. h oder DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8792c-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8792c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8792c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8792c-162">DBT \_ configchangeabgeb Rochen</span><span class="sxs-lookup"><span data-stu-id="8792c-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="8792c-163">DBT- \_ ConfigChanged</span><span class="sxs-lookup"><span data-stu-id="8792c-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="8792c-164">DBT \_ CustomEvent</span><span class="sxs-lookup"><span data-stu-id="8792c-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="8792c-165">DBT \_ devicearrival</span><span class="sxs-lookup"><span data-stu-id="8792c-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="8792c-166">DBT \_ DeviceQueryRemove</span><span class="sxs-lookup"><span data-stu-id="8792c-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="8792c-167">DBT \_ devicequeryremovefailed</span><span class="sxs-lookup"><span data-stu-id="8792c-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="8792c-168">DBT \_ deviceremovecomplete</span><span class="sxs-lookup"><span data-stu-id="8792c-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="8792c-169">DBT \_ deviceremovepending</span><span class="sxs-lookup"><span data-stu-id="8792c-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="8792c-170">DBT-Geräte- \_ /richtlinientypespecific</span><span class="sxs-lookup"><span data-stu-id="8792c-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="8792c-171">DBT- \_ Devnodes \_ geändert</span><span class="sxs-lookup"><span data-stu-id="8792c-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="8792c-172">DBT \_ querychangeconfig</span><span class="sxs-lookup"><span data-stu-id="8792c-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="8792c-173">DBT \_ UserDefined</span><span class="sxs-lookup"><span data-stu-id="8792c-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 

